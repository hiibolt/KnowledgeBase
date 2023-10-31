public:: true

- ### Metadata
  Date: *October 10, 2023*
  Class: *PHYS253 - Section 1*
  Author: *John White*
  Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  In this lab, we will...
	  * Practice using a sinusoidal fit on a graph
	  * Learn how springs behave depending on the mass
	  * Calculate the error percentages between a calculated and measured value
- # Data
	- ## 50g - 6cm
	  ![50g - 6cm - PvT.png](../assets/50g_-_6cm_-_PvT_1698780651068_0.png)
	  ![50g - 6cm - VvT.png](../assets/50g_-_6cm_-_VvT_1698780669127_0.png)
	- ## 50g - 10cm
	  ![50g - 10cm - PvT.png](../assets/50g_-_10cm_-_PvT_1698780684020_0.png)
	  ![50g - 10cm - VvT.png](../assets/50g_-_10cm_-_VvT_1698780699907_0.png)
	- ## 100g - 6cm
	  ![100g - 6cm - PvT.png](../assets/100g_-_6cm_-_PvT_1698780715658_0.png)
	  ![100g - 6cm - VvT.png](../assets/100g_-_6cm_-_VvT_1698780721717_0.png)
	- ## 100g - 10cm
	  ![100g - 10cm - PvT.png](../assets/100g_-_10cm_-_PvT_1698780731910_0.png)
	  ![100g - 10cm - VvT.png](../assets/100g_-_10cm_-_VvT_1698780736799_0.png)
	- ## 150g - 6cm
	  ![150g - 6cm - PvT.png](../assets/150g_-_6cm_-_PvT_1698780750493_0.png)
	  ![150g - 6cm - VvT.png](../assets/150g_-_6cm_-_VvT_1698780754921_0.png)
	- ## 150g - 10cm
	  ![150g - 10cm - PvT.png](../assets/150g_-_10cm_-_PvT_1698780767099_0.png)
	  ![150g - 10cm - VvT.png](../assets/150g_-_10cm_-_VvT_1698780772696_0.png)
- # Results
	- ## 3.1 Graph Comparison
		- ### 3.1.1 Similarities
		  They are both sinusoidal graphs which fit perfectly with the function that the TA provided. They behave very similar to how the equations predict, albiet with some gradual decrease in amplitude, which is to be expected in an imperfect system.
		- ### 3.1.2 Differences
		  They do not have the same co-domains, the velocity has a much lower while the position is much higher due to units. They also start at difference times on the sin wave's graph.
		- ### 3.1.3 Mass Location at V = 0
		  The mass is located at either extreme of the position co-domain (peak or valley), which does line up with how the equations provided. ($$y = \sin(2\pi ft+\theta)$$ and $$v = A\omega \cos(\omega t + \theta)$$)
		- ### 3.1.4 Mass Location at $V_{max}$
		  The mass is located directly at the origin ($y = 0$), which does make sense. This is because the mass has not yet started to slow down, and the velocity is at its max right before it begins to change in direction.
	- ## 3.2 Offsets
		- ### 3.2.1 Y_0 Position vs. Mass
		  The Y_0 position is lower depending on the mass, which does make sense according to our equations and Newton's laws. Because the mass is increased, gravity has more pull against the spring, creating a lower equilibrium point.
	- ## 3.3 Data Fit
		- ### 3.3.1 Fit of Data
		  The data does fit, and is fairly consistent across all graphs. There are no objective outliers.
		- ### 3.3.2 Effect on Constants Based on Mass and A_i
			- #### Mass and A are inverse to oneanother.
			- #### A_i is relatively proportional to A.
			- #### Mass is inverse to \omega.
			- #### A_i and \omega are independent of oneanother.
			- #### Velocity and Position fits have different phase offsets.
		- ### 3.3.3 Period of Motion
		  The period of motion is entirely independent of the initial amplitude, but it is heavily impacted by the mass of the object.
		- ### 3.3.4 K Calculation
		  Depending on the mass of the object, the K constant increases drastically. I believe this is due to imperfect timing or perhaps an imperfect system.
			- ### 3.3.5 Cosine vs. Sine Fit
			  Nothing changes given my equation, it only adjusts the phase of the equation - which makes sense. It could also have flipped the amplitude had I given slightly different data, but that did not happen for me.
- # Discussion
  First, I was tasked with creating a graph of each of the data sets. I did this by splitting the data into sheets and importing with `openpyxl`.
  ```python
  data_raw = load_workbook("data.xlsx", read_only = True)
  data = [
  	{
  		"name": "50g - 6cm",
  		"weight": 50,
  		"height": 6,
  		"data": data_raw["50g6"]
  	},
  	{
  		"name": "50g - 10cm",
  		"weight": 50,
  		"height": 10,
  		"data": data_raw["50g10"]
  	},
  	{
  		"name": "100g - 6cm",
  		"weight": 100,
  		"height": 6,
  		"data": data_raw["100g6"]
  	},
  	{
  		"name": "100g - 10cm",
  		"weight": 100,
  		"height": 10,
  		"data": data_raw["100g10"]
  	},
  	{
  		"name": "150g - 6cm",
  		"weight": 150,
  		"height": 6,
  		"data": data_raw["150g6"]
  	},
  	{
  		"name": "150g - 10cm",
  		"weight": 150,
  		"height": 10,
  		"data": data_raw["150g10"]
  	}
  ]
  
  for experiment in data:
  	experiment_data = []
  ```
  I then translated the data into human-readable dicts that I could represent.
  ```python
  	for row in experiment["data"].iter_rows():
  		values = [x.value for x in row]
  		if ( values[0] != None ):
  			experiment_data.append({
  				"time": values[0],
  				"acceleration": values[3],
  				"velocity": values[2],
  				"position": values[1]
  			})
  ```
  
  Next, I plot each of the two graphs. I ignore acceleration.
  ```python
  	# Velocity vs. Time
  	plt.scatter( np.array([x["time"] for x in experiment_data]), np.array([x["velocity"] for x in experiment_data]) )
  	plt.xlabel( "Time (s)" )
  	plt.ylabel( "Velocity (cm)" )
  
  	res = fit_sin(np.array([x["time"] for x in experiment_data]), np.array([x["velocity"] for x in experiment_data]))
  	k = float((experiment["name"].split('g'))[0])  * (res["omega"] ** 2)
  	print("%(amp).4fsin(%(omega).4ft + %(phase).4f)" % res )
  
  	tt2 = np.linspace(0, experiment_data[len(experiment_data) - 1]["time"]) # x range
  	plt.plot(tt2, res["fitfunc"](tt2), "r-", label="y fit curve", linewidth=2)
  	plt.title( "%(amp).4fsin(%(omega).4ft + %(phase).4f)" % res )
  	plt.savefig( f"{experiment['name']} - VvT - k {k}.png" )
  	plt.clf()
  
  
  	# Position vs. Time
  	plt.scatter( np.array([x["time"] for x in experiment_data]), np.array([x["position"] for x in experiment_data]) )
  	plt.xlabel( "Time (s)" )
  	plt.ylabel( "Position (cm)" )
  
  	res = fit_sin(np.array([x["time"] for x in experiment_data]), np.array([x["position"] for x in experiment_data]))
  
  	tt2 = np.linspace(0, experiment_data[len(experiment_data) - 1]["time"]) # x range
  	plt.plot(tt2, res["fitfunc"](tt2), "r-", label="y fit curve", linewidth=2)
  	plt.title( "%(amp).4fsin(%(omega).4ft + %(phase).4f)" % res )
  	plt.savefig( f"{experiment['name']} - PvT.png" )
  	plt.clf()
  ```
  
  Above, I fit a sinusoidal curve with the trendline function
  ```python
  def fit_sin(tt, yy):
  	'''Fit sin to the input time sequence, and return fitting parameters "amp", "omega", "phase", "offset", "freq", "period" and "fitfunc"'''
  	tt = np.array(tt)
  	yy = np.array(yy)
  	ff = np.fft.fftfreq(len(tt), (tt[1]-tt[0]))   # assume uniform spacing
  	Fyy = abs(np.fft.fft(yy))
  	guess_freq = abs(ff[np.argmax(Fyy[1:])+1])   # excluding the zero frequency "peak", which is related to offset
  	guess_amp = np.std(yy) * 2.**0.5
  	guess_offset = np.mean(yy)
  	guess = np.array([guess_amp, 2.*np.pi*guess_freq, 0., guess_offset])
  
  	def sinfunc(t, A, w, p, c):  return A * np.sin(w*t + p) + c
  	popt, pcov = scipy.optimize.curve_fit(sinfunc, tt, yy, p0=guess)
  	A, w, p, c = popt
  	f = w/(2.*np.pi)
  	fitfunc = lambda t: A * np.sin(w*t + p) + c
  	return {"amp": A, "omega": w, "phase": p, "offset": c, "freq": f, "period": 1./f, "fitfunc": fitfunc, "maxcov": np.max(pcov), "rawres": (guess,popt,pcov)}
  ```
  
  F
-
-
- # Conclusion
  ...