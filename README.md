# Neural_Network_Charity_Analysis

## With knowledge of machine learning and neural networks, create a model that is capable of predicting if applicants will be sccessful when funded by Alphabet Soup. 

### Resources
- Data Source: charity_data.csv

- Software: Jupyter Notebook 6.1.4

### Results
- Data Preprocessing
	- What variable(s) are considered the target(s) for your model?
		- IS_SUCCESSFUL 
	- What variable(s) are considered to be the features for your model?
		- APPLICATION_TYPE    
		- AFFILIATION          
		- CLASSIFICATION      
		- USE_CASE             
		- ORGANIZATION         
		- INCOME_AMT    
		- ASK_AMT   
		- SPECIAL_CONSIDERATIONS
		- STATUS    
	- What variable(s) are neither targets nor features, and should be removed from the input data?
		- EIN
		- NAME

- Compiling, Training, and Evaluating the Model
	- How many neurons, layers, and activation functions did you select for your neural network model, and why?
		- 2 layers, 80 neurons and 30 neurons becuase it was recommended not to add excessive layer to avoid overfitting and the number of neurons should be in range of 2 times to 2/3 of input feature number.
		- ReLu function because it is ideal for looking at positive nonlinear input data for classification or regression.
	- Were you able to achieve the target model performance?
		- No, I was not able to achieve the target model performance of 75% accuracy rate.
	- What steps did you take to try and increase model performance?
		- drop more columns 
		- change the number of values to replace if counts are less than x
		- increase the number of neurons
		- increase the hidden layer
		- change the activation function
		- change the number of epochs

### Summary 
- First attempt
	- drop SPECIAL_CONSIDERATIONS
	- change replace value <700 for APPLICATION_TYPE and <1800 for CLASSIFICATION
	- add third hidden layer and change the number of neurons
	
![alt text](https://github.com/Yunaka1269/Neural_Network_Charity_Analysis/blob/main/First_attempt.PNG "First")

- Second attempt
	- drop SPECIAL_CONSIDERATIONS and INCOME_AMT
	- change replace value <1000 for APPLICATION_TYPE
	- change activation function to all sigmoid
	- add third hidden layer
	- decrease the number of epochs
	
![alt text](https://github.com/Yunaka1269/Neural_Network_Charity_Analysis/blob/main/Second_attempt.PNG "Second")

- Third try
	- drop SPECIAL_CONSIDERATIONS and STATUS
	- change replace value <700 for APPLICATION_TYPE and <700 for CLASSIFICATION
	- add the fourth hidden layer
	- increase epochs number
	
![alt text](https://github.com/Yunaka1269/Neural_Network_Charity_Analysis/blob/main/Third_attempt.PNG "Third")

- Fourth try
	- drop SPECIAL_CONSIDERATIONS, STATUS, INCOME_AMT, and ASK_AMT
	- change replace value <700 for APPLICATION_TYPE and <1800 for CLASSIFICATION
	
![alt text](https://github.com/Yunaka1269/Neural_Network_Charity_Analysis/blob/main/Fourth_attempt.PNG "Fourth")
