# Amazon Prime Video Content Analysis & Interactive Dashboard


![Static Badge](https://img.shields.io/badge/Visualization-Power_BI-yellow?style=for-the-badge)
![Static Badge](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> A comprehensive analysis of the Amazon Prime Video catalog, detailing the journey from raw data to actionable insights. This project involves data cleaning, exploratory data analysis (EDA) using Python, and the creation of a fully interactive dashboard in Power BI.

This repository contains the complete workflow for analyzing the Amazon Prime Video dataset. The primary goal is to understand the composition of the content library, identify key trends, and present these findings in a dynamic and visually appealing dashboard.

---

### 📋 Table of Contents

* [Project Overview](#-project-overview)
* [Dashboard Preview](#-dashboard-preview)
* [Data Source](#-data-source)
* [Methodology](#%EF%B8%8F-methodology)
    * [1. Data Cleaning & Preprocessing](#1-data-cleaning--preprocessing)
    * [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
    * [3. Visualization](#3-visualization)
* [Key Insights & Findings](#-key-insights--findings)
* [Future Work](#-future-work)
* [Tools & Libraries](#-tools--libraries)
* [Repository Structure](#-repository-structure)
* [How to Reproduce](#-how-to-reproduce)
* [Contact](#-contact)

---

### 🚀 Project Overview

This project provides a deep dive into the content available on Amazon Prime Video. By analyzing a dataset of nearly 10,000 titles, we can answer critical questions about the platform's content strategy, such as:

* What is the distribution between movies and TV shows?
* Which countries are the primary content producers?
* What are the most popular and frequently listed genres?
* How has the volume of content added to the platform evolved over the years?

The analysis is conducted in a Jupyter Notebook, and the final results are consolidated into an intuitive Power BI dashboard for easy exploration.

---

### 📊 Dashboard Preview

The interactive dashboard provides a holistic view of the Prime Video library. Users can filter by genre, country, and release year to dynamically explore the data.

![Amazon Prime Video Analysis Dashboard](https://github.com/LakshitaPagaria/Amazon-Prime-Video-Analysis-Project/blob/main/Amazon%20Prime%20Video%20Analysis%20Dashboard.png)
*Note: You will need to upload the dashboard image to your repository and update the link above.*

---

### 💾 Data Source

The analysis is based on the `amazon_prime_titles.csv` dataset, which is publicly available on Kaggle.

* **Dataset Link:** [Amazon Prime Video Titles on Kaggle](https://www.kaggle.com/datasets/shivamb/amazon-prime-movies-and-tv-shows)

<details>
<summary><strong>Click to view Data Dictionary</strong></summary>

| Column | Description | Data Type |
| :--- | :--- | :--- |
| `show_id` | Unique identifier for each title. | `object` |
| `type` | The type of content ('Movie' or 'TV Show'). | `object` |
| `title` | The name of the title. | `object` |
| `director` | The director(s) of the movie. | `object` |
| `cast` | The main actors in the title. | `object` |
| `country` | The country or countries of production. | `object` |
| `date_added`| The date the title was added to Prime Video. | `object` |
| `release_year`| The year the title was originally released. | `int64` |
| `rating` | The content rating (e.g., 13+, 18+, ALL). | `object` |
| `duration` | Duration (minutes for movies, seasons for TV shows).| `object` |
| `listed_in` | The genre(s) the title is listed under. | `object` |
| `description`| A brief summary of the title. | `object` |

</details>

---

### 🛠️ Methodology

The project follows a structured approach, moving from raw data to a polished, interactive dashboard.

#### 1. Data Cleaning & Preprocessing

The initial dataset contained missing values and potential duplicates. The following steps were performed in the `prime_video_analysis.ipynb` notebook to ensure data quality:
* **Handling Null Values:**
    * Missing values in the `director` and `cast` columns were imputed with the string `'Unknown'`.
    * Missing `country` values were filled with the mode (the most frequently occurring country, which was the United States).
* **Removing Duplicates:** Any exact duplicate rows were identified and removed from the dataset.
* **Data Export:** The cleaned dataset was exported to `prime_video_cleaned.csv` for use in Power BI. A separate file, `prime_video_country_map.csv`, was also created for the map visualization.

#### 2. Exploratory Data Analysis (EDA)

With a clean dataset, a thorough EDA was conducted to uncover patterns and trends. Key areas of analysis included:
* **Content Type Distribution:** A bar chart was created to visualize the count of Movies vs. TV Shows.
* **Top 10 Countries:** The top 10 countries by the number of titles were identified and plotted.
* **Release Year Trends:** A line chart was used to show the trend of titles released per year.
* **Content Rating Analysis:** The distribution of the top 10 content ratings was analyzed.
* **Genre Analysis:** The `listed_in` column was parsed to count the occurrences of each genre, and the top 10 were visualized.

#### 3. Visualization

The insights from the EDA were brought to life in an interactive Power BI dashboard. The dashboard features:
* **Key Performance Indicators (KPIs):** Cards displaying total titles, number of movies, and number of TV shows.
* **Donut Chart:** Showing the percentage split between movies and TV shows.
* **Bar Charts:** For the top 10 genres and top 10 countries.
* **Area Chart:** Illustrating the number of titles by release year.
* **Map Visualization:** A geographic representation of title distribution by country.
* **Slicers:** Interactive filters for Genre, Country, and Release Year.

---

### 💡 Key Insights & Findings

The analysis and dashboard revealed several key insights into the Amazon Prime Video library:
> * **Movies Dominate the Catalog:** The platform has a significantly larger collection of movies compared to TV shows.
> * **US-Centric Content Library:** The United States is the largest single contributor of content to the platform.
> * **A Surge in Recent Content:** There has been a dramatic increase in the number of titles released in the last two decades.
> * **Drama and Comedy Lead the Way:** These are the two most common genres found in the Prime Video library.

---

### 🔮 Future Work

This project provides a solid foundation for further analysis. Potential future work could include:
* **Sentiment Analysis:** Performing sentiment analysis on the `description` column to gauge the overall tone of the content.
* **Time-Series Analysis:** Analyzing the `date_added` column to identify trends in content acquisition over time.
* **Network Analysis:** Creating a network graph of directors and cast members to find key collaborators.

---

### 💻 Tools & Libraries

This project utilizes the following tools and Python libraries:

* **Python** for data analysis and manipulation.
    * **Pandas:** For data cleaning, manipulation, and aggregation.
    * **Matplotlib & Seaborn:** For creating static visualizations within the Jupyter Notebook.
    * **Collections (Counter):** For efficient counting of genres.
* **Jupyter Notebook:** As the primary environment for coding and analysis.
* **Power BI:** For creating the final interactive and shareable dashboard.

---

### 📂 Repository Structure

```
├── amazon_prime_titles.csv               # Raw, original dataset
├── prime_video_analysis.ipynb            # Jupyter Notebook with the full Python analysis
├── prime_video_cleaned.csv               # Cleaned data, ready for Power BI
├── prime_video_country_map.csv           # Data prepared for map visualizations
├── Amazon Prime Video Analysis Dashboard.jpg # Screenshot of the final dashboard
└── README.md                             # This documentation file
```

---

### 🚀 How to Reproduce

To replicate this analysis on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Install the required libraries:**
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```

3.  **Run the Jupyter Notebook:**
    Launch the `prime_video_analysis.ipynb` notebook to execute the data cleaning and EDA. This will also generate the cleaned CSV files.
    ```bash
    jupyter notebook prime_video_analysis.ipynb
    ```

4.  **Explore the Dashboard:**
    Open Power BI and use `prime_video_cleaned.csv` as the data source to build the dashboard or create your own custom visualizations.

---

### 📬 Contact

Email: lakshitapagaria@gmail.com

Linkedin: https://www.linkedin.com/in/lakshita-pagaria/
