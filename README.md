# Introduction to Intelligent Systems - Assignment



## Q1 — Fuzzy Logic System: Washing Machine Cycle Time



### Problem Statement

Design a fuzzy logic system to determine the **washing machine cycle time** based on two inputs: **Dirt Level** and **Load Size**.



### Inputs \& Outputs

|Variable|Type|Range|Fuzzy Sets|
|-|-|-|-|
|Dirt Level|Input|0 – 10|Low, Medium, High|
|Load Size|Input|0 – 10|Small, Medium, Large|
|Cycle Time|Output|0 – 80|Short, Medium, Long|



### Membership Functions

**Dirt Level (Trapezoidal)**

|Label|Trapezoid Points|
|-|-|
|Low|\[0, 0, 2, 4]|
|Medium|\[2, 4, 6, 8]|
|High|\[6, 8, 10, 10]|



**Load Size (Trapezoidal)**

|Label|Trapezoid Points|
|-|-|
|Small|\[0, 0, 2, 4]|
|Medium|\[2, 4, 6, 8]|
|Large|\[6, 8, 10, 10]|



**Cycle Time (Trapezoidal)**

|Label|Trapezoid Points|
|-|-|
|Short|\[0, 0, 15, 35]|
|Medium|\[25, 40, 60, 75]|
|Long|\[60, 75, 90, 90]|



### Fuzzy Rules (7 Rules)

|Rule|Dirt Level|Load Size|Cycle Time|
|-|-|-|-|
|1|Low|Small|Short|
|2|Low|Large|Medium|
|3|Medium|Medium|Medium|
|4|High|Small|Medium|
|5|High|Large|Long|
|6|Medium|Large|Long|
|7 *(default)*|Medium|Medium (OR)|Medium|



### Methodology

* **Inference Method:** Mamdani
* **Defuzzification:** Centroid method
* **Membership Function Type:** Trapezoidal
* **Library Used:** scikit-fuzzy



### How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Upload `Q1\_SmartWash\_FuzzyController.ipynb`
3. Click **Runtime → Run All**
4. At Step 8, enter custom Dirt Level and Load Size values when prompted



### Outputs

* Membership function plots for Dirt Level, Load Size, and Cycle Time
* Test results table showing cycle time for 5 sample inputs
* Interactive user input section for custom values
* 3D surface plot showing cycle time across all combinations of Dirt Level and Load Size



## Dependencies

All dependencies are installed automatically inside the notebook using `!pip install`.

|Library|Purpose|
|-|-|
|`scikit-fuzzy`|Fuzzy logic inference system|
|`numpy`|Numerical computation|
|`matplotlib`|Plotting membership functions and graphs|



## Credits

**Developed by:** Vivek Dhoot

**Course Project:** Introduction to Intelligent Systems

**Institution:** Manipal University Jaipur

## License

This project is open-source for learning and portfolio use. No commercial usage allowed without permission.

