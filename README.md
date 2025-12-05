# 📚 Gradebook Analyzer (CRISP-DM Analysis)

This project, "Gradebook Analyzer," is a Python utility designed to perform fundamental statistical analysis and grading on a set of student marks. It aligns with the CRISP-DM methodology by focusing on clear **Business Understanding** (need for automated grade analysis) and providing structured **Data Understanding**, **Data Preparation**, and **Evaluation** steps.

## 1. Business Understanding

The primary goal is to **streamline the process of analyzing student grade data** to quickly assess class performance, identify high/low achievers, and automatically assign letter grades based on defined criteria.

## 2. Data Understanding and Preparation

### 📂 Input Data Format
The system accepts student data in two ways: **Manual Input** or **CSV File Input**.

**Required Format:** A collection of student records, each consisting of a **Name** (string) and **Marks** (integer).

* **CSV File (`marks.csv`):** The file must be a simple comma-separated file with two columns: `student_name,marks`.
    ```csv
    John Doe,95
    Jane Smith,82
    ...
    ```

### ✨ Data Preparation
The script automatically handles the conversion of marks to integers and stores the data in a dictionary format (`{name: marks}`) for efficient processing. Basic error handling is included for file not found and invalid data types.

## 3. Modeling and Evaluation (Analysis)

The analysis is performed using a series of defined functions, which act as the **analytical model** for the grade data.

### 📊 Key Statistics (Evaluation Metrics)
The program calculates and outputs the following descriptive statistics:
* **Average (Mean) Score:** The arithmetic mean of all marks.
* **Median Score:** The middle value of the sorted marks.
* **Max Score:** The highest mark achieved.
* **Min Score:** The lowest mark achieved.

### 📝 Grade Assignment Logic
Letter grades are assigned based on the following fixed thresholds (the grading *model*):

| Marks Range | Grade |
| :---------- | :---- |
| $\ge 90$    | A     |
| $\ge 80$    | B     |
| $\ge 70$    | C     |
| $\ge 60$    | D     |
| $< 60$      | F     |

### 📋 Pass/Fail Criteria
Students are categorized as 'Passed' or 'Failed' using a threshold of **40 marks**. This is a critical **evaluation** component to quickly assess overall class success.

## 4. Deployment

### ⚙️ How to Run
1.  Ensure you have Python installed.
2.  Save the provided code as `main.py`.
3.  If using the CSV input option (Option 2), create a file named `marks.csv` in the same directory.
4.  Run the script from your terminal:

    ```bash
    python main.py
    ```

### 💻 Usage
Follow the on-screen menu:
1.  **Manual Input:** Enter the number of students, then provide the name and marks for each student sequentially.
2.  **CSV Input:** Reads data from `marks.csv`.
3.  **Exit Program:** Terminates the application.

After data input, the program immediately prints the full **Evaluation** report, including statistics, grade distribution counts, pass/fail lists, and a final name-marks-grade table.
