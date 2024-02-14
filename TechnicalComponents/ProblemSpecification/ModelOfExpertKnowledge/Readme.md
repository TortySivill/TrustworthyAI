# Building A Model Of Expert Knowledge

### To build AI that we can trust we must make sure that it aligns with our knowledge of the world. 

AI is very good at doing it what we tell it to do, whether that be to recognise human faces or distinguish between cancerous and non-cancerous cells. However, it has no concept of common-sense. Therefore, if we do not formulate our research hypothesis correctly our AI models may end up processing a completely different objective than what we expect.
For example, imagine we have a large collection of images of cats and dogs. It so happens that all the images of cats are taken outdoors and all images of dogs are taken indoors. We then ask a machine learning model to learn the difference between cats and dogs using these images. It achieves 99% accuracy on this data. However when we present this model with a new image of a cat, this time taken indoors, the AI model misclassifies our image as a dog.
This spurious behaviour of our AI model could have been avoided if we hadn’t trained our model using pictures of dogs and cats exclusively taken in one setting, or if we had re-written our research questions ‘distinguish between dogs and cats not using the background’ .  When developing AI models we must use our common sense about the world to specify what it is we want an AI to do. 

The above problem could be recognised by the AI developer when they are pre-processing the dataset. However, this is not the case in a setting where misalignment between reality and the AI model require subject matter expertise to identify. For example, how would a machine learning engineer know if an AI was using the background to distinguish between images of cancerous and non-cancerous lesions. 
When developing AI for these applications we must 
	1. Formalise our understanding of reality and ensure the AI model aligns 
	2. Incorporate Subject Matter expertise into these formalisations 

### In this repo we introduce the concept of “Domain Models” and “Bulletproof Hypothesis Formalisation” which address the above two criteria as methods for Trustworthy AI. 

## Domain Models

Domain Models are designed by Subject Matter Experts with no required machine learning expertise. They allow a Subject Matter Expert to incorporate their expectation about how the underlying system functions into an AI model to make sure outcomes align with reality. They consist of simple logic models which take the same inputs as the AI and determine an outcome based on simple logical rules. 

For example,

If (whiskers) AND NOT (wagging tail) THEN cat 

At the model evaluation stage of the development pipeline, the AI model is evaluated and compared against the Domain Model to identify potential discrepancies with expert expectations. 

## “Bulletproof” Hypothesis Formulation

Before developing the AI Model the Subject Matter Expert must work together to design the hypothesis which the AI is designed to address. For example, “Can the AI model distinguish between images of cats and dogs” 

As we have shown above, this hypothesis is vulnerable to weaknesses, or “bullets” in the associated dataset which ultimately result in the AI model learning something different than the intended hypothesis. 

“Bulletproof” Hypothesis Formulation encourages robust hypothesis generation. Incorporating both Machine Learning Engineer and Subject Matter Expert knowledge, this method generates potential and realistic edge cases and determines whether these are covered by the current hypothesis. 

For example,  “Bulletproof” Hypothesis Formulation would generate an image of a cat taken indoors and would therefore identify that the current research hypothesis, with the associated dataset does not cover this edge case. Prompting the modification of the research question and/or data collection. 
