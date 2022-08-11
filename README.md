# Neural_Network_Charity_Analysis
## Overview of the analysis:

The purpose of this analysis is to use machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Data is from a CSV file, which containing more than 34,000 organizations that have received funding from Alphabet Soup over the years

## Results: 

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

  I select 2 hidden layers and an output layer for the neural network model. The first layer has 50 neurons, and the second has 30 neurons. The hidden layers have the "relu" activation function and the output layer has the "sigmoid" activation function.

![Screen Shot 2022-08-10 at 2 09 56 PM (2)](https://user-images.githubusercontent.com/102264298/183998274-82b72ab1-b57d-4bf5-966c-0a1ea6992667.png)

* Were you able to achieve the target model performance?

  The model accuracy is only around 56%, which is less than 75%. In this case, I am unable to achieve the target model performance.  

![Screen Shot 2022-08-10 at 1 34 32 PM (2)](https://user-images.githubusercontent.com/102264298/183990708-32074745-672a-4de4-81b2-193087986812.png)

* What steps did you take to try and increase model performance?

  To increase the performance of the model, I did some modifications to preprocess the dataset: 

     1. Dropping the columnns "SPECIAL_CONSIDERATIONS" and "STATUS".
     2. Change the values("APPLICATION_TYPE") to be replaced if counts are less than 3000.
     3. Change the values("CLASSIFICATION") to be replaced if counts are less than 18,000.
  
  Here are the revised DataFrame with only 27 columns instead of 44.  

![Screen Shot 2022-08-10 at 6 43 14 PM (2)](https://user-images.githubusercontent.com/102264298/184042011-837a2176-0778-414c-a387-cdc1a06ae82e.png)

#### Attempt 1

The first attempt is to add three more hidden layers and more neurons, and the accuracy is 70.13%. 

![Screen Shot 2022-08-10 at 6 43 25 PM (2)](https://user-images.githubusercontent.com/102264298/184042021-d1c8d024-88bf-4524-a5bd-f1ec77de72fc.png)

![attempt1](https://user-images.githubusercontent.com/102264298/184042028-42190a27-a1bb-46a4-b63d-b306ac497773.png)

#### Attempt 2

The second attempt is to add two more hidden layers again and more neurons, and the accuracy is 70.23%. 

![attemp2](https://user-images.githubusercontent.com/102264298/184042032-cf984d0b-93be-4113-b56a-2ce900bd3b7b.png)

![attempt2](https://user-images.githubusercontent.com/102264298/184042037-40040589-23db-496b-8f3a-a415cc3e4b4b.png)

#### Attempt 3

The third attempt is to add more neurons and change the activation function from "relu" to "tanh" for the hidder layers. As a result, the accuracy is 70.18%. 

![attemp3](https://user-images.githubusercontent.com/102264298/184042043-5a3e9d70-0062-4acc-b39d-1bdc06c7b6ed.png)

![attemp3-2](https://user-images.githubusercontent.com/102264298/184042053-eb033f6d-3a8a-4956-adab-3a7023c1eddb.png)

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

The accuracy score is around 70% at the end of optimization. This does not meet the 75% accuracy target, even though it is pretty close. In this case, this optimization methods did not significantly improved this project. In order to meet the target accuracy score, it is recommended to acquire more data, check for outliers and also we can use Random Forest Classifier to construct a multitude of decision trees at training time. 
