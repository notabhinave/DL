# **Outlier Detection**

## **Aim**

To identify and remove outliers from a dataset using **two statistical methods** — **Z-Score** and **Interquartile Range (IQR)** — and visualize the effect of outlier removal on data distribution.

---

## **Short Description**

This project demonstrates how to detect and handle outliers in a dataset containing two variables:

* **X** → Independent variable (e.g., years of experience)
* **Y** → Dependent variable (e.g., salary)

The process includes:

1. **Data Loading & Initial Visualization**

   * The dataset is read from a CSV file.
   * A **boxplot** is plotted for both variables to visually identify extreme values.

2. **Z-Score Method**

   * Calculates the **mean** and **standard deviation** for each column.
   * Computes the **Z-score** for each value.
   * Marks values as outliers if their Z-score magnitude exceeds a given threshold (default = `2.8`).
   * Removes detected outliers and re-plots the boxplot.

3. **IQR Method**

   * Calculates **Q1** (25th percentile) and **Q3** (75th percentile).
   * Computes **IQR** = Q3 − Q1.
   * Flags values outside **\[Q1 − 1.5×IQR, Q3 + 1.5×IQR]** as outliers.
   * Removes detected outliers and re-plots the boxplot.

---

## **About the Result**

* **Initial Boxplot:** Showed visible outliers in both X and Y.
* **After Z-Score Cleaning:** Some extreme values were removed, leading to a more compact data range.
* **After IQR Cleaning:** Additional outliers were removed, further tightening the data spread.
* **Outcome:** The dataset became cleaner and more representative of the majority of observations, reducing the potential for skewed model training.

---

## **Result Highlights**

* Z-Score method is sensitive to the **threshold** value; lowering it may detect more outliers.
* IQR method is more **robust** to extreme values and often used for skewed data.
* Visualization via **boxplots** makes it easy to compare before and after cleaning.

---

