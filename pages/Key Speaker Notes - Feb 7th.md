# Advancing the Landing of Machine Learning
Speaker: Tianxiang Zhao
Affiliation: The Pennsylvania State University
Contact Information: tkz5084@psu.edu
- ## Introduction
	- ### Introducing Structured Data
		- #### Spatial Structured Data
		  Represents both entity attributes and their interactions/relations with each other
		  
		  **Examples**: Molecular network, Internet Network
		- #### Temporal Structured Data
		  Models sequential features and optimizes long-term rewards
		  
		  **Examples**: Game playing, treatment trajectory, human-machine interaction
	- ### Weakly-Supervised Learning
	  Deep neural networks required a *ton* of labeled data for training.
	  
	  This is often in scenarios with a very low number of data points, such as users with ground truths available in user profiling. (iGait, for instance, has this issue)
	  
	  **Examples of weak supervision**:
	  * Insufficient Supervision
	  * Inaccurate Supervision
	  * Biased Supervision
	- ### Iterpretability of machine learning models
	  Interpreting what is learned by the DNN is critical for evaluation.
	  
	  The black-box nature of a DNN tends to decouple results from proper interpretation.
		- #### Post-hoc Interpretation
		  Explaining an existing model
		- #### Ad-hoc Interpretation
		  Explaining during the design process
- ## Representative Works
	- ### Unsupervised Discovery of Latent Relations
	  Node connections are procured by a large number of factors, which are often concealed behind other factors.
	  
	  Therefore, we must differentiate these latent connections explicitly.
	- ### Latent Relations behind Existence of Connections
	  Without those latent relations, DNNs take all connections uniformly with the same message propagation.
	  
	  Two nodes $N_1$ and $N_2$ could have the same $P_1$ parent node with completely different connection semantics.
	- ### Deriving Semantics
	  **Heuristics**:
	  * Unions of the original data should recover the original input
	  * Homo-edges and hetero-edges carry different semantics
	  * Captured edge semantics should be disparate
	  
	  **DisGNN**:
	  Splitting the model into channels with each having their own relation type and aggregating into a singular model produces a far more accurate final model.
	- ### Learning From Noisy Sequences
	  We may want to imitate decision-making commonly used by experts. This can boost the learning of neural agents, vastly improving their efficiency.
	  
	  It's important to note that some data is unclean. What then?
	  We must use different segments differently according, and we do this by disentangling the action policies, creating decision pools and encoding them into different skills. We do this by discovering skills between $D^{\text{clean}}\unionD^{\text{noisy}}$, then applying the best to $D^{clean}$.
	- ### Encouraging Skill Disentanglement