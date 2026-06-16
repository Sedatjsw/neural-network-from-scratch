# Neural Network from Scratch using NumPy

This project demonstrates the implementation of a fully connected neural network from scratch using NumPy, without relying on deep learning frameworks such as TensorFlow or PyTorch.

The project focuses on understanding the core mathematical and computational principles behind neural networks, including forward propagation, backpropagation, gradient descent optimisation, and neural network architecture design.

The implementation was applied to a real-world superconductivity dataset to predict critical temperature values using regression.

---

## Project Overview

The main objective of this project is to build, train, evaluate, and optimise a neural network entirely from first principles using numerical computing techniques.

The project explores:

* Neural network implementation from scratch
* Forward and backward propagation
* Gradient descent optimisation
* Learning rate behaviour
* Architecture comparison
* Model complexity and generalisation trade-offs

The neural network was trained on a large real-world dataset containing over 21,000 observations and 81 numerical input features.

---

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn (data preprocessing and evaluation utilities only)

---

## Dataset

The project uses the Superconductivity Dataset containing:

* 21,263 samples
* 81 numerical input features
* Target variable: `critical_temperature (Tc)`

The dataset was preprocessed using:

* Train/Test split
* Feature standardisation
* Numerical scaling for stable optimisation

---

## Neural Network Architecture

The neural network was implemented manually using NumPy matrix operations.

### Components Implemented

* Forward pass computation
* ReLU activation function
* Linear output layer
* Mean Squared Error (MSE) loss
* Backpropagation algorithm
* Gradient descent parameter updates

The optimisation objective used during training was:

```text id="x9r3mv"
Loss = mean((y - ŷ)^2)
```

---

## Model Pipeline

```text id="g7m1pk"
Input Data (X, y)
↓
Train / Test Split
↓
Feature Scaling
↓
Forward Pass
↓
Loss Computation (MSE)
↓
Backpropagation
↓
Gradient Descent Update
↓
Evaluation (MSE & R²)
```

---

## Experimental Architecture Analysis

Multiple neural network architectures and learning rates were evaluated to analyse optimisation behaviour and generalisation performance.

### Attempt 1 — Baseline Network

Architecture:

```text id="z3n8tw"
81 → 8 → 1
```

Learning Rate:

```text id="q7d4ma"
0.01
```

Observation:

* Training diverged and produced NaN loss values

---

### Attempt 2 — Reduced Learning Rate

Architecture:

```text id="n5t1qb"
81 → 8 → 1
```

Learning Rate:

```text id="v2k9rm"
0.001
```

Observation:

* Stable convergence
* Smooth optimisation behaviour

---

### Attempt 3 — Larger Hidden Layer

Architecture:

```text id="j4r6wx"
81 → 16 → 1
```

Observation:

* Best overall performance
* Lower test loss
* Improved generalisation

---

### Attempt 4 — Increased Depth

Architecture:

```text id="m8q2lp"
81 → 16 → 8 → 1
```

Observation:

* Increased model complexity did not improve performance
* Generalisation slightly decreased

---

## Final Model Performance

Selected Model:

```text id="b1v7ns"
81 → 16 → 1
```

### Evaluation Metrics

* Test MSE ≈ 242.47
* Test R² ≈ 0.796
* RMSE ≈ 15.6

The final model explained approximately 79.6% of the variance in superconductivity critical temperature values.

---

## Key Insights

* Lower learning rates significantly improved optimisation stability
* Larger hidden layers slightly improved predictive performance
* Increasing network depth did not improve generalisation
* Simpler architectures produced more stable training behaviour
* Neural network optimisation is highly sensitive to hyperparameter selection

---

## Technical Report

A presentation-style technical report containing:

* Neural network implementation details
* Optimisation experiments
* Architecture comparisons
* Training behaviour analysis
* Performance evaluation
* Visualisations and results

is included in the `reports` folder.

---

## Project Structure

```text id="w4m8zn"
neural-network-from-scratch
 ├── data
 ├── notebooks
 ├── reports
 └── README.md
```

---

## Skills Demonstrated

* Neural Networks
* Backpropagation
* Gradient Descent
* Deep Learning Fundamentals
* Machine Learning
* Numerical Computing
* Model Optimisation
* Hyperparameter Tuning
* Regression Analysis
* Python Programming

---

## Conclusion

This project demonstrates the implementation and optimisation of a neural network entirely from scratch using NumPy.

The project highlights both the mathematical foundations and practical optimisation challenges involved in neural network training, including learning rate stability, architecture selection, and generalisation performance.

The experimental analysis also demonstrates how increased model complexity does not always improve predictive performance.

---

## Author

Sedat Aydin
MSc Big Data Analytics & Artificial Intelligence
