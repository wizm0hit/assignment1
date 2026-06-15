# GLA ML Session 1 - Python, Pandas & Data Visualization

## Overview

This notebook introduces fundamental Python programming, data analysis with Pandas, feature engineering, and data visualization using Matplotlib.

The exercises simulate a student performance dataset and demonstrate how to analyze, transform, and visualize data.

---

## Topics Covered

### 1. Python Basics

* Working with lists
* Using loops (`for`)
* Calculating averages
* Conditional statements (`if-else`)

Example:

* Calculate average marks
* Determine whether a class has passed or failed based on the average score

---

### 2. Creating a Dataset with Pandas

A student dataset is created containing:

| Column             | Description               |
| ------------------ | ------------------------- |
| student_id         | Unique student identifier |
| attendance_percent | Attendance percentage     |
| assignment_score   | Assignment marks          |
| quiz_score         | Quiz marks                |
| lab_completed      | Lab completion status     |

---

### 3. Data Exploration

The notebook demonstrates:

```python
df.shape
df.head()
df.info()
df.describe()
```

Used to understand:

* Dataset dimensions
* Sample records
* Data types
* Statistical summary

---

### 4. Feature Engineering

#### Total Score

A new column is created:

```python
df['total_score'] = df['assignment_score'] + df['quiz_score']
```

#### Eligibility Check

Students are marked eligible if:

* Attendance ≥ 75%
* Total Score ≥ 70
* Lab Completed = True

```python
df['eligible']
```

---

### 5. Filtering Data

Retrieve only eligible students:

```python
eligible_students = df[df["eligible"] == True]
```

---

### 6. Grading System

Grades are assigned using a custom function:

| Score Range | Grade |
| ----------- | ----- |
| 90+         | A     |
| 80–89       | B     |
| 70–79       | C     |
| Below 70    | F     |

---

### 7. Risk Detection

Students are flagged as "at risk" when:

* Attendance < 75%, or
* Total Score < 70

```python
df['at_risk']
```

---

## Data Visualizations

### Bar Chart

Displays total score for each student.

```python
plt.bar(...)
```

### Pie Chart

Shows grade distribution.

```python
plt.pie(...)
```

### Scatter Plot

Compares assignment scores and quiz scores.

```python
plt.scatter(...)
```

### Line Chart

Visualizes attendance trends.

```python
plt.plot(...)
```

### Histogram

Shows the distribution of total scores.

```python
plt.hist(...)
```

---

## Technologies Used

* Python
* Pandas
* Matplotlib

---

## Learning Outcomes

After completing this notebook, students will be able to:

* Use Python loops and conditions
* Create and manipulate DataFrames
* Perform basic data analysis
* Create new features from existing data
* Filter and query datasets
* Build simple grading systems
* Identify at-risk students
* Create common visualizations using Matplotlib

---

## Author

GLA University – Machine Learning Session 1
