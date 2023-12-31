### Metadata
Date: *October 5, 2022*
Class: *COMS100*
Author: *John White*
Professor: *Noi*
- ## Purpose
	- ### Topic
	  Artificial Intelligence - LLMs (Large Language Models)
	- ### General Purpose
	  To inform and educate on what AI, and more importantly, a LLM is.
	- ### Specific Purpose
	  To explain why LLMs cannot be used without plagarism.
- # Introduction
	- ## Attention Grabber
	  In 2019, a man on Avianca Airlines was hit by an attendant aggressively pushing a metal drink cart, heavily injuring him and ruining his vacation. Later, in court against the flight company, his lawyer testifies against him with what he believes is strong evidence - from ChatGPT. The case was postponed, and according to Forbes, now the lawyer is also standing trial in his own case. Why?
	- ## Credibility Statement
	  I'm a CS + Math student here, and I've built personalized AI models for both entrepreneurs and existing companies.
	- ## Central Idea + Preview Statement + Transition
	  So let's talk about what AI is, how it works, and what went wrong in that case.
- # Body
	- ### So let's define some things first.
		- #### Artificial Intelligence, according to Encyclopedia Britannica...
		  ...is an umbrella term that encapsulates anything with the ability to think or act like a intelligent being could. Under this umbrella, we will be talking about...
		- #### ...LLMs.
		  A LLM, according to Elastic Research, is essentially a huge database of text that can predict the 'next most likely word' given an input.
	- ## LLM inner workings
		- ### Training
		  So how is that database made? Well, first, the model is fed information. This can be books, articles, movie scripts, or in the case of ChatGPT, all of the above.
		  
		  Next the model encodes it, turning each text into a huge web of probability.
		  
		  Finally, the model can make predictions with this probability. Let's look at what a prediction actually looks like.
		- ### Prediction
		  Let's say we look at this sentence here. We've already written most of it, except for the last word. Now, WE can guess what comes next - but how does the model come to the same conclusion?
		  
		  Firstly, the model sees that it's possibly the end of a commanding sentence, and in most literature, these end in please. This is a very surface level assumption, so the model is only 23% sure.
		  
		  Second, the model sees that it's a pirate speaking via the context of 'aye' and 'pirate'. As a result, because pirates often end commanding sentences with 'matey', it has a higher confidence - 46%. 
		  
		  Finally, in addition to all other context, it sees 'crew,' and realizes that 'matey' should be plural, since in context, he is addressing the 'crew'. Because there is no further context, the model is most confident about this option - 91%.
	- # Limitations
		- ### Hallucination
		  Because it's generating the most likely next word, it's not always correct information. For instance, the model often misses context. 
		  
		  Imagine if the model in the previous example was not fed enough material with pirate-speak - it would have said please. Now, that's not necessarily wrong, but it is out of character. 
		  
		  Errors like this lead to ChatGPT generating information that never existed in the first place.
		- ### Creativity
		  Since the only information it has to operate is what's fed to it, these models don't have the ability to be 'creative'.
		  
		  Their idea of 'creativity' is a combination of every single work the model has access to, so it's not possible for them to create any 'new' concepts.
	- ## Ethics
		- ### Plagarism
		  So since no concepts are 'new', and are only based on the input material, does that mean they're stolen? 
		  
		  Yes. Much of the information that's fed to LLMs or artistic models is often used without permission, and can be considered plagiarism - just because it's taking bits and pieces from thousands of sources doesn't mean it isn't plagiarism.
- # Summary
  So with added context, it's not surprising that the lawyer was put on trial - he presented hallucinated, plagiarized, and fabricated evidence in front of a court - a jailable offence. 
  
  It was fabricated because he prompted ChatGPT with a task that produced evidence in his favor.
  it was hallucinated because the cases do not truly exist - they only do statistically.
  It was plagiarized because it was based off the works of many and not properly cited in court.
- ## Concluding Remarks
  I hope you all learned something today, and understand some of the limitations and ethics when it comes to using ChatGPT for everyday tasks.
- ### Works Cited
  * (N.d.-a). Retrieved October 5, 2023, from \https://i.pinimg.com/474x/84/41/3f/84413f6218e83bbc32f2bd7d033705f6--beverage-cart-airline-travel.jpg.
  * (N.d.-b). Retrieved October 5, 2023, from https://aimoneymastery.blogspot.com/2023/04/is-chatgpt-good-for-content-writing.html.
  * (N.d.-c). Retrieved October 5, 2023, from https://content.api.news/v3/images/bin/ef034b77e487c6d85dbb90e668aacc1e.
  * (N.d.-d). Retrieved October 5, 2023, from \http://res.cloudinary.com/dk-find-out/image/upload/q_80,w_1440/A-dreamstime_xxl_23971088_qlym7s.jpg.
  * (N.d.-e). Retrieved October 5, 2023, from \https://cdn1.vectorstock.com/i/1000x1000/11/95/thief-cartoon-with-sack-money-vector-1671195.jpg.
  * (N.d.-f). Retrieved October 5, 2023, from \https://cdn.pixabay.com/photo/2017/09/25/09/46/puzzle-2784471_960_720.png.
  * Bohannon, M. (2023, September 12). *Lawyer used Chatgpt in court-and cited fake cases. A judge is considering sanctions*. Forbes. https://www.forbes.com/sites/mollybohannon/2023/06/08/lawyer-used-chatgpt-in-court-and-cited-fake-cases-a-judge-is-considering-sanctions/
  * Encyclopædia Britannica, inc. (2023, October 5). *Artificial Intelligence*. Encyclopædia Britannica. https://www.britannica.com/technology/artificial-intelligence
  * What is a large language model?: A comprehensive llms guide*. Elastic. (n.d.). https://www.elastic.co/what-is/large-language-models*
  * What is machine learning?*. IBM. (n.d.). https://www.ibm.com/topics/machine-learning