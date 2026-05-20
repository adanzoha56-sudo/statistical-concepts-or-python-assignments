# statistical-concepts-or-python-assignments
Chapter 1 Statistical Concepts Assignment
# =========================================================
# Statistical Concepts Using Python
# Chapter 1 Assignment
# =========================================================

# Import Libraries
import pandas as pd
import numpy as np
from scipy.stats import trim_mean
import matplotlib.pyplot as plt

# ---------------------------------------------------------
# Creating Dataset
# ---------------------------------------------------------

data = {
    "Student": ["A", "B", "C", "D", "E", 
                "F", "G", "H", "I", "J"],

    "Marks": [78, 85, 92, 67, 88,
              73, 95, 81, 69, 84]
}

# Convert into DataFrame
df = pd.DataFrame(data)

# Display Dataset
print("========== DATASET ==========")
print(df)

# ---------------------------------------------------------
# Mean
# ---------------------------------------------------------

mean_value = df["Marks"].mean()

print("\n========== MEAN ==========")
print("Mean of Marks =", mean_value)

# ---------------------------------------------------------
# Median
# ---------------------------------------------------------

median_value = df["Marks"].median()

print("\n========== MEDIAN ==========")
print("Median of Marks =", median_value)

# ---------------------------------------------------------
# Trimmed Mean
# ---------------------------------------------------------

trimmed_mean_value = trim_mean(df["Marks"], 0.1)

print("\n========== TRIMMED MEAN ==========")
print("Trimmed Mean of Marks =", trimmed_mean_value)

# ---------------------------------------------------------
# Variance
# ---------------------------------------------------------

variance_value = df["Marks"].var()

print("\n========== VARIANCE ==========")
print("Variance of Marks =", variance_value)

# ---------------------------------------------------------
# Standard Deviation
# ---------------------------------------------------------

std_value = df["Marks"].std()

print("\n========== STANDARD DEVIATION ==========")
print("Standard Deviation of Marks =", std_value)

# ---------------------------------------------------------
# Statistical Summary
# ---------------------------------------------------------

print("\n========== STATISTICAL SUMMARY ==========")
print(df.describe())

# ---------------------------------------------------------
# Histogram
# ---------------------------------------------------------

plt.figure(figsize=(7,5))

plt.hist(df["Marks"], bins=5)

plt.title("Histogram of Student Marks")
plt.xlabel("Marks")
plt.ylabel("Frequency")

plt.show()

# ---------------------------------------------------------
# Boxplot
# ---------------------------------------------------------

plt.figure(figsize=(5,5))

plt.boxplot(df["Marks"])

plt.title("Boxplot of Student Marks")
plt.ylabel("Marks")

plt.show()

# ---------------------------------------------------------
# Interpretation
# ---------------------------------------------------------

print("\n========== INTERPRETATION ==========")

print("1. Mean shows the average marks of students.")
print("2. Median represents the middle value.")
print("3. Trimmed mean reduces effect of extreme values.")
print("4. Variance shows data spread.")
print("5. Standard deviation indicates consistency.")
print("6. Histogram shows distribution of marks.")
print("7. Boxplot helps identify spread and outliers.")
