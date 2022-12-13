# -Neural_Network_Charity_Analysis
Overview of the Analysis

Using Machine Learning and Neural Networks for this project, I created a binary classifier that will help to predict if the applicants that will be funded by a Charitable organization called Alphabet Soup will be successful. For this analysis we had a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup. This project compromised of the following 3 steps:

- Preprocessing the data for the neural network
- Compile, Train and Evaluate the Model
- Optimizing the model

Results

Data Preprocessing
- Variable that was considered as the target for my model: IS_SUCCESSFUL Column
- Variables that were considered features for my model: Every Column except for IS_SUCCESSFUL which is our target and the ones we will drop
- Variable that were neither targets or features for the dataset: Columns that I dropeed are EIN, NAME because they will have little to no impact om our outcome

Compiling, Training and Evaluating the Model
The number of neurons, layers, and activation functions I selected for my neural network model:

The first layer had 80 neurons, the second has 30 there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."

![8030](https://user-images.githubusercontent.com/108476566/207356753-654762c1-b1b9-44bf-831b-119344d50940.png)


Was the model able to achieve the target model performance?

The model was not able to reach the target 75%. The accuracy for my model was 53%.

![Evaluatemodel](https://user-images.githubusercontent.com/108476566/207357267-ad1d13ab-98a3-4128-8ea4-c4044221259e.png)


The steps taken to try and increase model performance

Attempt 1: Removed additional feature, that is the 'USE_CASE' column. Rest of the model components stayed the same, however model accuracy went down to 43%.

![DropEIN](https://user-images.githubusercontent.com/108476566/207380004-6eb554d8-8098-4761-bf13-f7945356ea13.png)

![Evaluatetestdata](https://user-images.githubusercontent.com/108476566/207380457-e90ac998-3601-413f-bdf7-3d2c3423430f.png)


Attempt 2: Adding Additional neurons to hidden layers and additional hidden layers are added. 

![DefineModelNodes](https://user-images.githubusercontent.com/108476566/207381027-d1d2ed06-c9bb-4bad-ad4b-54a7f2db8a69.png)

![Modelloss](https://user-images.githubusercontent.com/108476566/207381412-f6ba3d93-4d21-4804-803d-f293db2eadda.png)


Attempt 3: Changing activation function of output layer from "sigmoid" to "tanh." The accuracy of the model went down even more to 50%.
![attempt3](https://user-images.githubusercontent.com/108476566/207381719-090a4e35-c213-46dd-a7bf-fe1c2c65631e.png)

![Attempt3results](https://user-images.githubusercontent.com/108476566/207381993-db2faf16-135b-4a83-87b6-6de99cac89ca.png)



Summary

The final model accuracy score of 52% after optimization. The initial neural network had a accuracy score of 53%. Overfitting created this loss in accuracy. 
