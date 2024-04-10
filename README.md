# deep-learning-challenge



Explain the purpose of the analysis (4)
Answer all 6 questions in the results section (10)

#H1 Overview: 

#H1 Results: 

#H2 Data Preprocessing: 

#H3 What variable(s) are the target(s) for your model? 

#H3 What variable(s) are the features of your model? 

#H3 What variable(s) should be remove from the input data because they are neither targets nor features? 

#H2 Compiling, Training and Evaluating The Model 

#H3 How many neurons, layers and activation functions did you select for your neural network model, and why? 

#H3 Were you able to achieve the target model performance? 

#H3 What steps did you take in your attempts to increase model performance? 
Firstly, a new feature of Ask Amount was added, and processed into categorical bins. Principoal Component Analysis was then conducted on featuresd Ask Amount, Use Case and Income Amt. 
For attempt #2, Income Amt was removed as a feature so that only Use Case remained. Attempt # 3 added a third layer and increased the neurons to 25 and increased the number of Epochs from 50 to 75. Attempt #4 used Ask Amount instead of Income Amount for the feature while keeping the third layer with increased neurons and increased Epochs. Attempt #5 used the same features and set up as #4, but swapped the activations of the layers from Relu to TanH and the activation of the output from Sigmoid to Softmax. Attempt #6 used the features of the initial model (Use Cast and Income Amt) but added the third layer with increased neurons and epochs. 

#H1 Summary: 
Overall the most successful version of the model was #6, that used the features of Use Case and Income Amt, with 3 layers, the third having 25 neurons, using Relu and Sigmoid activatations and 75 epochs, with an accuracy of 54.45%. However, this is only a 0.04% accuracy increase over the first version's 54.41% accuracy that only had 2 layers and lower neurons and epochs. All six version of the model are relatively close in accuracy, ranging from 52.83% - 54.45%. Given that adjusting the layers, neurons, epochs and activations had minimal effective on the model's accuracy, I would recommend moving to a Mutilayer Perceptrons neural network which could provide a more accurate model since it uses multiple layers of nodes. 

- Model #1 had Use Case and Income Amt as features, using two layers with relu activations and sigmoid output activation - 54.41% accuracy
- Model #2 with Use Case as Features, with 2 layers, 52.83% accuracy
- Model #3 used Model #2 with 3 layers and increased neurons, 53.69% accuracy
- Model #4 used Ask_AMT as Features, with 3 layers, 53.55% accuracy
- Model #5 used Model #4 with TanH and Softmax instead of Relu and Sigmoid, 53.43% accuracy
- Model #6 used Model #1 with 3 layers and increased neurons previously used in Model #3, 54.45% accuracy 
