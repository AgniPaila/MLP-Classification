# MLP Neural Network Classifier - (Java, Python)

## 📚 Project Description

This project implements a custom MLP classifier in Java, trained on a synthetic dataset to explore the influence of various hyperparameters on generalization performance. The architecture allows flexible configuration of hidden layer sizes, activation functions (`sigmoid`, `tanh`, `relu`), learning rate and batch sizes.

Report.pdf includes the results of extensive experimentation, comparing the MLP NN performance under different conditions.

## 🧠 Project Architecture

The implementation consists of the following classes:

- **`MLP.java`**  
  Contains the `main()` method. Handles the training process, evaluation, and configuration.

- **`Layer.java`**  
  Represents a hidden or output layer of the MLP. Implements `forwardPass` and `backPropagation`.

- **`Neuron.java`**  
  Models an individual neuron. Handles output calculation, delta computation, and weight updates.

- **`Point.java`**  
  Represents a data sample in the format `[x1, x2, category]`. Used for both training and test datasets.

## 📁 Data Files
Training and test datasets are provided in .csv format:
-training_set.csv
-test_set.csv
These datasets are auto-generated via a helper Java class.

## 📊 Visualization
To visualize decision boundaries and error evolution, a Python script is included. It reads the test results and error logs and plots:
-Correct vs incorrect classifications
-Error rate per epoch

## 🔧 Configuration Parameters
Set the following parameters at the beginning of the MLP.java file:
-d: Input dimensions (default: 2)
-K: Number of output categories
-h1, h2, h3: Number of neurons per hidden layer
-hiddenLayersFunction: Activation function for hidden layers (sigmoid, tanh, relu)
-outputLayerFunction: Activation function for output layer
-learningRate: Training learning rate
-numBatches: Batch size
-terminateThreshold: Minimum error change threshold for stopping training

## 📈 Experimental Results
Experiments were performed with varying:
-Activation functions
-Hidden layer sizes
-Batch sizes (numBatches = 40 and 400)

### Best Results
| Activation Function   | Hidden Layers (H1, H2, H3) | Batches | Accuracy (%) |
| --------------------- | -------------------------- | ------- | ------------ |
| `sigmoid` / `sigmoid` | 21, 21, 21                 | 40      | **97.9**     |
| `tanh` / `tanh`       | 21, 18, 18                 | 40      | 96.1         |
| `tanh` / `sigmoid`    | 21, 15, 18                 | 400     | 95.7         |


## 🚀How to Run
Compile using: javac *.java

Run using: java MLP

## 📘 Course Info
- **Course:** Υπολογιστική Νοημοσύνη (Computational Intelligence)
- **Team:** This project was implemented in collaboration with one other student.
