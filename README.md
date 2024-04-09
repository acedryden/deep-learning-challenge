# deep-learning-challenge

Write a Report on the Neural Network Model (30 points)
Write an analysis that includes a title and multiple sections, labeled with headers and subheaders (4 points)
Format images in the report so that they display correction (2)
Explain the purpose of the analysis (4)
Answer all 6 questions in the results section (10)
Summarize the overall results of your model (4)
Describe how you could use a different model to solve the same problem, and explain why you would use that model (6)


- Model #1 had Use Case and Income Amt as features, using two layers with relu activations and sigmoid output activation - 54.41% accuracy
- Added new Ask_Amt Bins as a feature
- Performed Principal Component Analysis
- Model #2 with Use Case as Features, with 2 layers, 53.42% accuracy
- Model #3 used Model #2 with 3 layers and increased neurons, 53.69% accuracy
- Model #4 used Ask_AMT as Features, with 3 layers, 53.43% accuracy
- Model #5 used Model #4 with TanH and Softmax instead of Relu and Sigmoid, 53.43% accuracy
- Model #6 used Model #1 with 3 layers and increased neurons previously used in Model #3, 54.47% accuracy 
