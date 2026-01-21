# Assignment-1

# Name: Raunaq Mittal

## Learning Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

---

## 1. Objective

The objective of this assignment is to learn a probability density function (PDF) from real-world data using a roll-number-dependent non-linear transformation. The assignment demonstrates how statistical estimation techniques can be used to model data distributions after applying a controlled transformation.

---

## 2. Dataset

- **Dataset Name**: India Air Quality Data
- **Source**: Kaggle
- **Link**: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data
- **Feature Used**: NO2 (Nitrogen Dioxide concentration), denoted as x

---

## 3. Roll Number Details

- **University Roll Number (r)**: 102303752

The transformation parameters are computed as:

- ar = 0.05 \* (r mod 7) = 0.25
- br = 0.3 \* (r mod 5 + 1) = 0.899

---

## 4. Methodology

The complete methodology consists of the following steps:

### **Step-1: Non-Linear Transformation**

Each NO2 value x is transformed into a new variable z using the roll-number-parameterized transformation:

z = x + ar _ sin(br _ x)

This transformation introduces non-linearity and ensures that the transformed data is unique for each student based on their roll number.

---

### **Step-2: Learning the Probability Density Function**

The transformed variable z is modeled using the following probability density function:

p̂(z) = c _ exp( -λ _ (z - μ)² )

The parameters of the PDF are learned using statistical estimation:

μ (Mean) is estimated as the sample mean of z
σ² (Variance) is computed from the transformed data
λ (Lambda) is calculated as:  
 λ = 1 / (2 \* σ²)
c (Normalization constant) is calculated as:  
 c = sqrt( λ / π )

This ensures that the probability density function integrates to 1.

---

### **Step-3: Parameter Submission**

The learned parameters μ, λ, and c are reported as the final outcome of the assignment.

---

## 5. Results

The estimated parameters obtained after applying the transformation and learning the PDF are:

| Parameter                  | Value                 |
| -------------------------- | --------------------- |
| μ (Mean)                   | 25.802708360471062    |
| λ (Lambda)                 | 0.0014590905290116402 |
| c (Normalization Constant) | 0.021550938267777164  |

These values are specific to the given roll number and dataset.

---

## 6. Tools & Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas

---

## 7. Repository Structure

```
PDF Non-Linear-Model
├── Assignment_102303752_UCS654.ipynb
└── README.md
```

## 8. Conclusion

In this assignment, a probability density function was learned from real-world NO2 air quality data using a roll-number-parameterized non-linear transformation. The transformed data was modeled using a Gaussian-shaped probability density function, and its parameters were estimated using statistical techniques. The obtained results correctly represent the distribution of the transformed variable. Since the transformation depends on the university roll number, the learned parameters may vary for different students.
