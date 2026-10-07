# Student Performance Indicator — Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on student performance data to understand how students' test scores are associated with factors such as:

- Gender
- Race/Ethnicity
- Parental level of education
- Lunch type
- Test preparation course

The analysis focuses on identifying patterns and relationships between these demographic/educational factors and students' **Math, Reading, and Writing scores**.

---

## 🎯 Problem Statement

The objective of this project is to understand how a student's performance in exams is affected by variables such as **gender, race/ethnicity, parental level of education, lunch type, and test preparation course**.

---

## 📊 Dataset

The dataset contains **1,000 rows and 8 original columns**.

**Dataset source:** [Students Performance in Exams — Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

### Features

| Feature | Description |
|---|---|
| `gender` | Gender of the student |
| `race_ethnicity` | Student's race/ethnicity group (A–E) |
| `parental_level_of_education` | Highest education level of the student's parents |
| `lunch` | Type of lunch: standard or free/reduced |
| `test_preparation_course` | Whether the student completed the test preparation course |
| `math_score` | Mathematics score |
| `reading_score` | Reading score |
| `writing_score` | Writing score |

During the analysis, two additional features were created:

- `total score` — Sum of Math, Reading, and Writing scores
- `average` — Average of the three subject scores

---

## 🛠️ Technologies & Libraries

The project was developed in Python using:

- **Python**
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical data visualization
- **Jupyter Notebook** — Interactive analysis environment

---

## 🔍 Project Workflow

The notebook follows an exploratory data analysis workflow:

1. Problem understanding
2. Data collection
3. Data inspection and validation
4. Missing-value analysis
5. Duplicate-value analysis
6. Data-type inspection
7. Unique-value analysis
8. Descriptive statistics
9. Feature exploration
10. Feature engineering
11. Univariate analysis
12. Bivariate analysis
13. Multivariate analysis
14. Outlier detection
15. Interpretation of findings
16. Conclusion

---

## 🧹 Data Quality Checks

The dataset was checked for:

- Missing values
- Duplicate records
- Data types
- Number of unique values
- Descriptive statistics
- Categories present in categorical features

### Results

- **No missing values** were found.
- **No duplicate records** were found.
- Numerical and categorical features were identified for further analysis.

---

## 🧮 Feature Engineering

Two new features were created from the subject scores:

```python
df['total score'] = df['math_score'] + df['reading_score'] + df['writing_score']
df['average'] = df['total score'] / 3
```

These features were then used to analyze overall student performance.

---

## 📈 Exploratory Data Analysis

### 1. Score Distribution

Histograms and KDE plots were used to examine the distribution of:

- Average score
- Total score

The analysis also compared score distributions across gender and other categorical variables.

### 2. Subject Performance

The notebook compares performance across Math, Reading, and Writing.

Key observation:

- Students generally performed better in **Reading and Writing** than in Mathematics.
- Most Math scores were concentrated around **60–80**.
- Reading and Writing scores were largely concentrated around **50–80**.

### 3. Gender Analysis

The dataset contains a relatively balanced number of male and female students.

The analysis found:

- Female students have a **higher average overall score**.
- Male students have a **higher average Math score**.
- Female students tend to perform better overall.

### 4. Race/Ethnicity Analysis

The analysis compares the performance of students across Groups A–E.

Key observations:

- **Group E** students have the highest average scores.
- **Group A** students have the lowest average scores.
- Groups A and B tend to have lower overall performance compared with the other groups.
- Group C and Group D contain the largest numbers of students.

### 5. Parental Level of Education

Parental education levels were analyzed in relation to student performance.

Key observations:

- The largest group of parents falls under **Some College**.
- Students whose parents have **Bachelor's or Master's degrees** tend to have higher scores than students in other parental-education categories.

### 6. Lunch Analysis

Lunch type was examined as a factor associated with student performance.

Key observation:

- Students receiving **standard lunch** tend to perform better than students receiving **free/reduced lunch**.

The dataset also contains more students receiving standard lunch than free/reduced lunch.

### 7. Test Preparation Course

The notebook compares students who completed the test preparation course with those who did not.

Key observation:

- Students who **completed the test preparation course** have higher scores across **Math, Reading, and Writing** than students who did not complete it.

### 8. Outlier Analysis

Boxplots were used to inspect the distributions of:

- Math scores
- Reading scores
- Writing scores
- Average scores

### 9. Multivariate Analysis

A pairplot was used to examine relationships between the numerical score variables.

The analysis indicates that:

> Math, Reading, and Writing scores increase approximately linearly with one another.

---

## 📊 Visualizations Used

The notebook uses several visualization techniques, including:

- Histograms
- KDE plots
- Count plots
- Pie charts
- Bar charts
- Violin plots
- Boxplots
- Pairplots

These visualizations were used for both univariate and multivariate exploration.

---

## 💡 Key Findings

The main findings from the analysis are:

1. **Gender:** Female students have a higher overall average, while male students perform better in Math on average.
2. **Race/Ethnicity:** Group E students show the highest scores, while Group A students show the lowest.
3. **Parental Education:** Higher parental education levels, particularly Bachelor's and Master's degrees, are associated with higher student scores in the analysis.
4. **Lunch:** Students receiving standard lunch tend to have better academic performance.
5. **Test Preparation:** Students who completed the test preparation course score higher across all three subjects.
6. **Subject Performance:** Mathematics shows comparatively weaker performance, while Reading shows stronger performance.
7. **Score Relationships:** Math, Reading, and Writing scores show positive, approximately linear relationships with one another.

---

## 📁 Project Structure

```text
Student-Performance-EDA/
│
├── data/
│   └── stud.csv
│
├── EDA STUDENT PERFORMANCE.ipynb
│
└── README.md
```

> The exact filenames/folder structure can be adjusted to match the structure of the GitHub repository.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd Student-Performance-EDA
```

### 2. Install the required libraries

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the notebook

Open:

```text
EDA STUDENT PERFORMANCE.ipynb
```

Make sure the dataset is available at:

```text
data/stud.csv
```

---

## 📌 Conclusion

This project demonstrates how **Exploratory Data Analysis** can be used to investigate factors associated with student academic performance.

The analysis suggests that **gender, race/ethnicity, parental education, lunch type, and completion of a test preparation course** are associated with differences in student scores. Among the factors examined, completing the test preparation course is associated with higher performance across Math, Reading, and Writing.

Overall, the project provides a structured exploration of the dataset and establishes a foundation for further statistical analysis or machine-learning-based student performance prediction.

---

## 👤 Author

**[Your Name]**

If you found this project useful, consider ⭐ starring the repository.
