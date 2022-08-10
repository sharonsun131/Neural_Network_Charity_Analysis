# Neural_Network_Charity_Analysis
## Overview of the analysis: Explain the purpose of this analysis.

The purpose of this analysis is to use machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Data id from a CSV file, which containing more than 34,000 organizations that have received funding from Alphabet Soup over the years

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing

* What variable(s) are considered the target(s) for your model?

  The column 'IS_SUCCESSFUL' is considered the target for the model. 

* What variable(s) are considered to be the features for your model?

  The column "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION","STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_
AMT" are considered  to be the fetures for the model. 

* What variable(s) are neither targets nor features, and should be removed from the input data?

  The columns 'EIN' and 'NAME' are removed from the input data. 
  
Here is the DataFrame: 

![Screen Shot 2022-08-10 at 1 34 12 PM (2)](https://user-images.githubusercontent.com/102264298/183990717-eab8dd8c-310b-4a5a-89dc-8ba155b60654.png)


### Compiling, Training, and Evaluating the Model


* How many neurons, layers, and activation functions did you select for your neural network model, and why?

![Screen Shot 2022-08-10 at 2 09 56 PM (2)](https://user-images.githubusercontent.com/102264298/183998274-82b72ab1-b57d-4bf5-966c-0a1ea6992667.png)



* Were you able to achieve the target model performance?

The model accuracy is only around 56%, which is less than 75%. In this case, I am unable to achieve the target model performance.  

![Screen Shot 2022-08-10 at 1 34 32 PM (2)](https://user-images.githubusercontent.com/102264298/183990708-32074745-672a-4de4-81b2-193087986812.png)

* What steps did you take to try and increase model performance?

To increase the performance of the model, 

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
