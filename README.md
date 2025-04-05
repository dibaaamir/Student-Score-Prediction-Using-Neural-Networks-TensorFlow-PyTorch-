# 🎓 Student Score Prediction Using Neural Networks (TensorFlow/PyTorch)

This project implements a **regression-based neural network model** to predict student performance scores based on features such as previous scores, hours of sleep, and hours studied. The model is built using a deep learning framework (either **TensorFlow** or **PyTorch**) and trained on a small, structured dataset.

---

## 📂 Dataset Overview

The dataset consists of the following columns:

| Feature            | Description                                           |
|--------------------|-------------------------------------------------------|
| `Previous Scores`  | Student's previous academic performance               |
| `Sleep Hours`      | Average hours of sleep before the test                |
| `Hours Studied`    | Total hours spent studying for the test               |
| `Performance Index`| Target variable (the score to be predicted)           |

---

## 🛠 Project Workflow

### 1️⃣ Data Preparation
- Loaded the dataset into a Pandas DataFrame
- Performed **exploratory data analysis (EDA)** to understand the distribution and correlation of features
- Normalized the feature values using Min-Max scaling to bring all inputs to a common scale
- Split the dataset into:
  - **Training Set** – 70%
  - **Validation Set** – 20%
  - **Test Set** – 10%

### 2️⃣ Model Building
- Created a custom **neural network** using the selected framework
- Model architecture:
  - Input layer matching number of features (3)
  - Multiple hidden layers (tested different depths/sizes)
  - **1 output neuron** for regression output
- Activation function: `ReLU` in hidden layers, `Linear` in output

### 3️⃣ Training
- Loss function: **Mean Squared Error (MSE)**
- Optimizer: **Adam** (efficient adaptive learning rate optimizer)
- Tracked loss over epochs and visualized training performance
- Explained differences between MSE and optimizers used

### 4️⃣ Evaluation
- Evaluated model using **test data**
- Reported final **test loss**, **mean absolute error**, and optionally **R² score**
- Compared performance with different:
  - Learning rates
  - Epoch counts
  - Layer configurations

### 5️⃣ Model Tuning (Bonus)
- Improved model performance through:
  - Learning rate adjustment
  - Increasing epochs
  - Adding more hidden layers
  - Batch size tuning

---

## 📈 Visualizations

- Line plot of **training/validation loss** over epochs
- Scatter plots of **actual vs. predicted** scores
- Correlation heatmap between features (optional)

---

## 🧪 Technologies Used

- **Python 3**
- **Pandas / NumPy** – Data manipulation
- **Matplotlib / Seaborn** – Data visualization
- **TensorFlow** or **PyTorch** – Model creation and training
