# Netflix-Data-Analysis-Project
Data Analysis internship project exploring Netflix movies, TV shows, trends, and business recommendations.

# Netflix Movies & TV Shows Data Analysis Project

This repository contains a comprehensive data analysis project completed for the PlutoAcademy AI & ML Internship Program. The project utilizes Python, Pandas, Matplotlib, and Seaborn to uncover audience trends, clean platform content metadata, and provide strategic business recommendations for streaming media catalogs.

## Project Deliverables
* **Google Colab Notebook:** [Access the Complete Code & Workspace Here](https://colab.research.google.com/drive/1MsLjA776JYfAOUX4bBes-prj2ECAReRs?usp=sharing)
* **Dataset Used:** [Kaggle Netflix Movies & TV Shows Dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows)

---

## 1. Data Cleaning Summary & Decisions
* **Dropped Columns:** `director` and `cast` were completely omitted from active analysis as they contained over 30% missing values and were not critical to macro-level trend evaluations.
* **Imputed Missing Values:** Missing entries in the `country` feature were designated as *'Unknown'*, and missing maturity ratings were explicitly marked *'Not Rated'* to preserve row integrity for volume tracking.
* **Type Formatting:** The `date_added` column was stripped of whitespace and parsed into datetime objects to cleanly extract year-over-year additions (`year_added` and `month_added`).
* **Feature Engineering:** Movie durations were isolated, stripped of text tags (like 'min'), and parsed into standard integers (`duration_num`) to execute mathematical metrics and scatter distribution mapping.

---

## 2. Insights & Business Recommendations

### 1. Shift Capital from Volume to Engagement (Referencing Chart 1: Pie Chart)
* **Finding:** The **Pie Chart** analysis reveals a massive catalog volume imbalance: Movies comprise **69.6%** of all content entries, whereas TV Shows account for only **30.4%**. 
* **Recommendation:** While movies bulk up catalog counts quickly, multi-season TV shows drive long-term habit formation and subscriber retention. Netflix should pivot its core original budget to increase the ratio of TV Shows, directly mitigating subscriber churn between major movie drops.

### 2. Capitalize on Q4 Viewer Spikes for Major Releases (Referencing Chart 6: Heatmap)
* **Finding:** The chronological **Heatmap** indicates a distinct, recurring concentration of asset uploads during the fourth quarter (**October, November, and December**), consistently reaching peak volume densities.
* **Recommendation:** This pattern aligns with holiday periods and colder seasonal weather in the Northern Hemisphere when consumer screen time naturally spikes. Netflix should synchronize its highest-budget "Originals" and marquee marketing campaigns with this winter window to maximize immediate viewership velocity.

### 3. Standardize Original Movie Runtimes for Maximum Completion (Referencing Chart 3: Histogram)
* **Finding:** Movie durations follow a clean normal distribution (bell curve) that peaks sharply between **90 and 110 minutes**, followed by a steep drop-off for films extending past the two-hour mark.
* **Recommendation:** Production teams should target a strict runtime constraint of roughly 100 minutes for standard original feature acquisitions. This optimizes audience completion rates and satisfies internal recommendation algorithms, keeping users from abandoning lengthy films halfway through.

### 4. Mitigate Market Saturation by Scaling Regional Production Hubs (Referencing EDA Question 2)
* **Finding:** The exploratory data analysis establishes that the **United States** (3,649 titles) and **India** (972 titles) dominate catalog production, heavily towering over all other regional outputs.
* **Recommendation:** To sustain growth past domestic market saturation, Netflix must aggressively scale localized production hubs in fast-growing international markets (e.g., South Korea, Japan, Spain). This approach creates high-value regional assets that cross over into massive global hits at a fraction of standard Hollywood production overheads.

### 5. Double Down on Core Anchor Genres (Referencing Chart 4: Bar Chart)
* **Finding:** The **Bar Chart** highlights that **Dramas, Comedies, and International Movies** are the absolute largest categories by volume across the platform.
* **Recommendation:** Continue leveraging international dramas as high-ROI, cross-border assets. A single gripping dramatic asset can be easily subbed/dubbed to capture core target demographics across multiple continents simultaneously, maximizing utility from a single production spend.

---

## 3. Most Surprising Finding
> What surprised me the most was the data from the **Scatter Plot (Chart 5)** when compared against the platform's explosive growth. Despite the astronomical explosion of content added after 2015, the average runtime of movies remained rigidly anchored around the 100-minute mark. I expected that the structural freedom of streaming and the rise of independent cinema would result in a highly fragmented spread of experimental, shorter, or much longer films, but the traditional cinematic runtime format remains completely unbothered by the digital shift.
