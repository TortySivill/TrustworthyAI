## Evaluating Trustworthy Models

Thorough model evaluation is essential to building trust between end-user and AI. In this repo we develop methodologies using ideas from Uncertainty Modelling, Explainable AI and Algorithmic Fairness and 
combine these into an evaluation suite which identifies trustworthy AI. Below we detail these techniques. 

### Test Models with a Wide Range of Model Metrics 

Currently AI models are often evaluated using performance based metrics such as accuracy and speed. 
Optimising for trust requires a wider range of metrics which can be prioritised according to the system requirements. 

For example, if we are distuinguishing cancerous from non cancerous lung images, it may be a system requirement that we care more about limiting the number of false negatives (falsely classified healthy lung images). In 
this scenario, accuracy is the wrong metric to use, we should be using precision and recall instead. 

### Interactive Explanations 

### Uncertainty Report

### Counterfactual Fairness 
