# Alphabet Soup Funding Neural Network
# Overview: 
The purpose of this analysis is to help the nonprofit foundation Alphabet Soup select applicants for funding with the best chance of success, by using machine learning and neural networks to create a model to predict whether applicants will be successful. The data provided by Alphabet Soup contains more than 34,000 rows of organizations that have recieved funding with a number of columns to be used for potential features: 
- Application Type (Alphabet Soup's application type) 
- Affiliation (Sector of Industry)
- Classification (Government organization classification) 
- Use Case (Use case for funding) 
- Organization (Organization Type)
- Status (Active status)
- Income Amount (Income classification)
- Special Considerations (Special considerations for the application)
- Ask Amount (Funding amount requested) 
- Campaign's outcome (Successful or not) 

# Results: 
## Data Preprocessing: 

### What variable(s) are the target(s) for your model? 
The variable "Is Successful" is the target for my model, as I want to be able to predict what features would lead to a successful campaign. 

### What variable(s) are the features of your model? 
Three variables were chosen for the features of the model - Use Case, Income Amount and Ask Amount, as I wanted to explore how these three factors would affect a campaign's outcome. For all three, bins were created based on the unique counts of each and to allow binary categorical analysis. Initially only Use Case and Income Amount were chosen as features, but Ask Amount was added during the optimization stage. 

### What variable(s) should be remove from the input data because they are neither targets nor features? 
EIN, Name, Application Type, Affiliation, Classification, Organization, Status and Special Consideration were all removed as neither targets nor features. 

## Compiling, Training and Evaluating The Model 

### How many neurons, layers and activation functions did you select for your neural network model, and why? 
The initial model had two layers, with 5 neurons in each layer, which was chosen as the dataset being used was not too complex and I didn't want to risk overfitting the data by increasing the model's complexity. These layers used ReLU activation function, with the output layer using Sigmoid activation function. I chose the ReLU activation function for its simplicity and efficiently, and I chose Sigmoid as it's effective with predicting probabilities with binary classification problems which is precisely what this project is. 

### Were you able to achieve the target model performance? 
No, the target model performance was over 75% accuracy but the model's accuracy was only 54.41%. 

### What steps did you take in your attempts to increase model performance? 
Firstly, a new feature of Ask Amount was added, and processed into categorical bins. Principoal Component Analysis was then conducted on featuresd Ask Amount, Use Case and Income Amt. 
For attempt #2, Income Amt was removed as a feature so that only Use Case remained. Attempt # 3 added a third layer and increased the neurons to 25 and increased the number of Epochs from 50 to 75. Attempt #4 used Ask Amount instead of Income Amount for the feature while keeping the third layer with increased neurons and increased Epochs. Attempt #5 used the same features and set up as #4, but swapped the activations of the layers from Relu to TanH and the activation of the output from Sigmoid to Softmax. Attempt #6 used the features of the initial model (Use Cast and Income Amt) but added the third layer with increased neurons and epochs. 

# Summary: 
Overall the most successful version of the model was #6, that used the features of Use Case and Income Amt, with 3 layers, the third having 25 neurons, using Relu and Sigmoid activatations and 75 epochs, with an accuracy of 54.45%. However, this is only a 0.04% accuracy increase over the first version's 54.41% accuracy that only had 2 layers and lower neurons and epochs. All six version of the model are relatively close in accuracy, ranging from 52.83% - 54.45%. Given that adjusting the layers, neurons, epochs and activations had minimal effective on the model's accuracy, I would recommend moving to a Mutilayer Perceptrons neural network which could provide a more accurate model since it uses multiple layers of nodes. 

