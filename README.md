# 🎬 Movie Popularity & Ratings — Exploratory Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a movie dataset containing information about approximately 9,800 movies.

The goal of this project is to explore movie popularity, ratings, genres, release years, and voting information using **Python, Pandas, Matplotlib, and Seaborn**.

> **Note:** Although the original dataset filename may suggest Netflix data, this dataset is a general movie dataset containing information such as movie title, popularity, vote count, vote average, language, genre, and poster URL. It does not contain Netflix-specific information.

---

## 🎯 Objectives

The main objectives of this analysis are:

* Understand the structure and characteristics of the movie dataset
* Perform basic data cleaning and preprocessing
* Analyze movie popularity and ratings
* Identify the most common movie genres
* Explore highly rated/popular movies
* Find movies with the highest and lowest popularity scores
* Analyze movie releases by year
* Visualize patterns and distributions in the data

---

## 📊 Dataset

The dataset contains **9,827 rows and 9 columns** before preprocessing.

### Original Columns

| Column              | Description                    |
| ------------------- | ------------------------------ |
| `Release_Date`      | Movie release date             |
| `Title`             | Movie title                    |
| `Overview`          | Short description of the movie |
| `Popularity`        | Movie popularity score         |
| `Vote_Count`        | Number of votes received       |
| `Vote_Average`      | Average movie rating           |
| `Original_Language` | Original language of the movie |
| `Genre`             | Movie genre(s)                 |
| `Poster_Url`        | URL of the movie poster        |

After initial exploration, the `Overview`, `Original_Language`, and `Poster_Url` columns were removed because they were not required for this EDA.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — data manipulation and analysis
* **NumPy** — numerical operations
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization
* **Jupyter Notebook**

---

## 🔎 Data Cleaning & Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Inspected the dataset using `info()` and `describe()`.
3. Checked for duplicate rows.
4. Converted `Release_Date` into a datetime format.
5. Extracted the release year from `Release_Date`.
6. Removed unused columns.
7. Converted `Vote_Average` into four categories:

   * `not_popular`
   * `below_avg`
   * `average`
   * `popular`
8. Removed rows affected by the rating categorization.
9. Split the comma-separated `Genre` column.
10. Used `explode()` so that each movie-genre combination could be analyzed separately.
11. Converted `Genre` into a categorical data type.
    The `Popularity` column contains significant right-skew and outliers. These were retained because they represent genuinely highly popular movies rather than obvious data errors.

---

## 📈 Analysis & Questions

### 1. What is the most frequent genre?

**Drama** is the most frequent genre in the dataset, representing approximately **14.5%** of the movie-genre rows.

---

### 2. Which genre is most common among popular movies?

Approximately **25.5%** of the rows fall into the `popular` rating category.

Within this group, **Drama** is the leading genre, representing approximately **20.1%** of the popular subset.

---

### 3. Which movie has the highest popularity?

The movie with the highest popularity score is:

**Spider-Man: No Way Home (2021)**

Genres:

* Action
* Adventure
* Science Fiction

Popularity score: **5083.954**

---

### 4. Which movies have the lowest popularity?

There is a tie for the lowest popularity score:

* **The United States vs. Billie Holiday (2021)**
* **Threads (1984)**

Both have a popularity score of **13.354**.

---

### 5. Which year had the most movie releases?

**2021** had the highest number of movie releases in this dataset.

---

### 6. Additional Analysis

The project also explores relationships between:

* Popularity
* Vote Count
* Vote Average

A correlation heatmap is used to examine relationships between these numerical variables.

The project also compares the **average popularity of different movie genres**, which is different from simply counting how frequently each genre occurs.

---

## 📊 Visualizations

The project uses several visualizations, including:

* Boxplot for Popularity outliers
* Genre distribution
* Rating category distribution
* Genre distribution among popular movies
* Movie releases by year
* Correlation heatmap
* Average popularity by genre

These visualizations make it easier to identify patterns and trends in the dataset.

---

## 💡 Key Findings

Some important findings from the analysis:

* **Drama** is the most frequently occurring genre.
* Drama also leads among movies categorized as `popular`.
* **Spider-Man: No Way Home** has the highest popularity score in the dataset.
* **The United States vs. Billie Holiday** and **Threads** share the lowest popularity score.
* **2021** was the year with the most releases in this dataset.
* The `Popularity` variable is heavily right-skewed, with a small number of movies having extremely high popularity scores.
* Genre frequency and average genre popularity are two different ways of looking at movie genres.

---

## 📁 Project Structure

```text
Movie-EDA/
│
├── Movie_EDA_corrected.ipynb
├── mymoviedb.csv
├── README.md
└── requirements.txt
```

---

## ⚙️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Movie-EDA.git
```

### 2. Navigate to the project folder

```bash
cd Movie-EDA
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Movie_EDA_corrected.ipynb
```

Make sure `mymoviedb.csv` is in the same project directory because the notebook loads the dataset using:

```python
pd.read_csv('mymoviedb.csv')
```

---

## 📦 Requirements

The main Python libraries used in this project are:

```text
numpy
pandas
matplotlib
seaborn
jupyter
```

---

## 🚀 Future Improvements

As a beginner Data Science project, there are several ways this project could be extended:

* Build a movie recommendation system
* Perform more detailed genre analysis
* Analyze trends in movie popularity over time
* Investigate the relationship between vote count and popularity
* Build an interactive dashboard using **Power BI**, **Tableau**, or **Streamlit**
* Apply Machine Learning to predict movie ratings or popularity
* Perform NLP analysis on movie overviews

---

## 👨‍💻 About

This project was created as part of my journey as a **beginner Data Science learner**, with a focus on learning data cleaning, exploratory data analysis, and data visualization using Python.

I'm continuously improving my Data Science skills through hands-on projects.

---

## ⭐ If you found this project useful

Feel free to explore the notebook, provide feedback, or suggest improvements.
