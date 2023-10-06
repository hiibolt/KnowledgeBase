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
	  In 2019, a man on Avianca Airlines was hit by an attendant aggressively pushing a metal drink cart, heavily injuring him and ruining his vacation. Later, in court against the flight company, his lawyer testifies against him with what he believes is strong evidence - from ChatGPT. The case is postponed, and now the lawyer is also standing trial in his own case. Why?
	- ## Credibility Statement
	  I'm a CS + Math student here, and I've built personalized AI models for both entrepreneurs and existing companies.
	- ## Central Idea + Preview Statement + Transition
	  So let's talk about what AI is, how it works, and what went wrong in that case.
- # Body
	- ### So let's define some things first.
		- #### Artificial Intelligence...
		  ...is an umbrella term that encapsulates anything with the ability to think or act like a intelligent being could. Under this umbrella, we will be talking about...
		- #### ...LLMs
		  A LLM is essentially a huge database of text that can predict the 'next most likely word' given an input.
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
		  Since the only information it has to operate is what's fed to it, these models don't have the ability to be 'creative'. Their idea of 'creativity' is a combination of every single work the model has access to, so it's not possible for them to create any 'new' concepts.
		-
	-