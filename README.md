# Gradient Descent Student Mark Prediction using Python

This project demonstrates a simple **Gradient Descent algorithm** to predict a student's marks based on:

* Study Hours
* Previous Marks
* Attendance

The project is designed as a beginner-friendly introduction to **Machine Learning, Loss Functions, Gradients, Weights, and Learning Rate** using Python.

## 📌 Project Overview

The model starts with initial weights and calculates a predicted mark.

It then:

1. Calculates the prediction
2. Calculates the error
3. Calculates the loss
4. Calculates gradients
5. Updates the weights
6. Calculates a new prediction
7. Repeats the process using Gradient Descent

The goal is to reduce the prediction error over multiple iterations.

## 🧠 Concept Used

The basic prediction formula is:

```text
Prediction =
    Study Hours × Study Weight
    + Previous Marks × Mark Weight
    + Attendance × Attendance Weight
```

The error is calculated as:

```text
Error = Prediction - Actual Mark
```

The loss function is:

```text
Loss = Error²
```

The gradient is calculated as:

```text
Gradient = 2 × Error × Input
```

The weights are updated using:

```text
New Weight = Old Weight - Learning Rate × Gradient
```

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Google Colab
* Gradient Descent
* Basic Machine Learning concepts

## 📊 Input Features

| Feature       | Example Value |
| ------------- | ------------: |
| Study Hours   |             5 |
| Previous Mark |            80 |
| Attendance    |            90 |
| Actual Mark   |            77 |

Initial weights:

| Weight            | Value |
| ----------------- | ----: |
| Study Weight      |   0.4 |
| Mark Weight       |   0.5 |
| Attendance Weight |   0.2 |

Learning rate:

```text
0.00001
```

## 🔢 Initial Prediction

The initial prediction is:

```text
(5 × 0.4) + (80 × 0.5) + (90 × 0.2)
```

```text
2 + 40 + 18 = 60
```

Actual mark:

```text
77
```

Error:

```text
60 - 77 = -17
```

Loss:

```text
(-17)² = 289
```

After the first weight update, the prediction moves closer to the actual mark.

## 🔄 Gradient Descent Process

```text
Input Data
     ↓
Calculate Prediction
     ↓
Calculate Error
     ↓
Calculate Loss
     ↓
Calculate Gradients
     ↓
Update Weights
     ↓
Calculate New Prediction
     ↓
Repeat
```

## 💻 Example Code

```python
study_hours = 5
previous_mark = 80
attendance = 90

study_weight = 0.4
mark_weight = 0.5
attendance_weight = 0.2

actual_mark = 77
learning_rate = 0.00001

for i in range(10):

    prediction = (
        study_hours * study_weight +
        previous_mark * mark_weight +
        attendance * attendance_weight
    )

    error = prediction - actual_mark
    loss = error ** 2

    study_gradient = 2 * error * study_hours
    mark_gradient = 2 * error * previous_mark
    attendance_gradient = 2 * error * attendance

    study_weight = study_weight - learning_rate * study_gradient
    mark_weight = mark_weight - learning_rate * mark_gradient
    attendance_weight = attendance_weight - learning_rate * attendance_gradient

    new_prediction = (
        study_hours * study_weight +
        previous_mark * mark_weight +
        attendance * attendance_weight
    )

    print("Iteration:", i + 1)
    print("Prediction:", prediction)
    print("Error:", error)
    print("Loss:", loss)
    print("New Prediction:", new_prediction)
    print("-" * 40)
```

## 📈 Learning Outcome

Through this project, I learned:

* How machine learning prediction works
* What weights are
* What a learning rate is
* How loss is calculated
* What gradients are
* How Gradient Descent updates model parameters
* How repeated iterations can reduce prediction error
* How Python can be used to implement basic ML algorithms from scratch

## 🚀 Future Improvements

Possible improvements include:

* Add a larger student dataset
* Use multiple students for training
* Normalize the input features
* Add a bias/intercept
* Plot loss over iterations
* Compare different learning rates
* Implement the same model using NumPy
* Compare the implementation with Scikit-learn
* Build a complete student-performance prediction model

## 👨‍💻 Author

**Malik Ahmad**

BS Information Technology

Interested in:

* Artificial Intelligence
* Machine Learning
* Python
* Data Science
* Web Development

## ⭐ Project Purpose

This project is created for **learning and educational purposes** to understand the fundamental mathematics behind Gradient Descent and Machine Learning.
