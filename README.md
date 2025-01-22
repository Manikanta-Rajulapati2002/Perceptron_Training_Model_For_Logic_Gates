**Brief explaintaion for the perceptron model training for the Logic gates** 
This explaination consists of five main steps, detailing the implementation and functionality of the 
code for training a perceptron model on a logic gates dataset. 

**Step 1: Defining the Logic Gate Dataset** 
For instance
• The code defines datasets for logic gates, starting with the OR gate. 
• The dataset is structured as: 
o Inputs (X): [[0, 0], [0, 1], [1, 0], [1, 1]] 
o Outputs (y): [[0], [1], [1], [1]] 
• The code defines datasets for logic gates, starting with the XOR gate. 
• The dataset is structured as: 
o Inputs (X): [[0, 0], [0, 1], [1, 0], [1, 1]] 
o Outputs (y): [[1], [0], [0], [0]] 

**Step 2: Creating the Perceptron Model** 
• The perceptron model is implemented using PyTorch. 
• Key components of the model: 
o Linear layer (nn.Linear): Connects two input features to a single output 
neuron. 
o Activation function (nn.Sigmoid): Maps raw outputs to probabilities in the 
range [0, 1], suitable for binary classification. 
• The forward method defines how input data flows through the perceptron. 

**Step 3: Training the Perceptron** 
• The train_perceptron function trains the model on the input dataset. 
• Key steps in the training process: 
1. Convert input and target data to PyTorch tensors. 
2. Define the loss function (nn.BCELoss) for binary classification. 
3. Use the Stochastic Gradient Descent (SGD) optimizer to update model 
weights. 
4. Train the model for a specified number of epochs (default: 1000): 
▪ Perform forward propagation to compute predictions. 
▪ Calculate and backpropagate the loss. 
▪ Update weights using the optimizer. 
5. Track and log the loss at every 100 epochs for monitoring. 
• The function returns: 
o The trained model. 
o A list of loss values to visualize the learning curve.
 
**Step 4: Visualizing the Decision Boundary** 
• The plot_decision_boundary function plots the decision boundary learned by the 
perceptron. 
• The steps are: 
1. Create a mesh grid over the feature space. 
2. Predict probabilities for grid points using the trained perceptron. 
3. Plot the decision boundary using contour levels (threshold = 0.5). 
4. Overlay the dataset points on the decision boundary for comparison. 
• This visualization provides insights into how the perceptron separates the two classes 
in the dataset.

**Step 5: Training and Visualization for Logic Gates** 
• The code iterates through the dataset dictionary and performs the following for each gate: 
1. Trains the perceptron using train_perceptron. 
2. Plots the training loss curve to observe model convergence. 
3. Visualizes the decision boundary to demonstrate the perceptron’s 
classification regions. 
• These steps illustrate the perceptron's ability to solve the logic gates 
problem effectively.

**Purpose and Key Takeaways** 
• The code demonstrates how a perceptron can learn to classify data for logic gates.
• Training loss curves illustrate model convergence. 
• Decision boundary plots reveal the regions learned by the perceptron, effectively 
  separating input classes for a simple logic gates. 
