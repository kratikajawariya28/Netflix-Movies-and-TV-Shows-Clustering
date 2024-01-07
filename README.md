# Netflix Movies and TV Shows Clustering

## Overview

This project aims to optimize Netflix's content recommendation system for TV Shows and Movies by leveraging advanced data analysis and clustering techniques. The primary objectives include conducting detailed Exploratory Data Analysis (EDA), implementing text-based clustering to categorize similar content, and developing a sophisticated recommendation system to enhance user experience.

**Table of Contents**

1. [Overview](#overview)
2. [Problem Statement](#problem-statement)
3. [Data Wrangling](#data-wrangling)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Feature Engineering ](#feature-engineering)
6. [ML Model Implementation](#ml-model-implementation)
7. [Recommendation System](#recommendation-system)
8. [Conclusion](#conclusion)

## Problem Statement
The goal of this project is to analyze the Netflix catalog of movies and TV shows, which was sourced from the third-party search engine Flixable, and group them into relevant clusters. This will aid in enhancing the user experience and prevent subscriber churn for the world's largest online streaming service provider, Netflix, which currently boasts over 220 million subscribers as of 2022-Q2. The dataset, which includes movies and TV shows as of 2019, will be analyzed to uncover new insights and trends in the rapidly growing world of streaming entertainment.

## Data Wrangling
This section focuses on the initial phase of the project. We've organized the data wrangling process into four distinct sections:

#### **1. Handling Null Values:**
* Imputed 'Unknown' for 'director' and 'cast'.
* Imputed with the mode for the 'country'.
* Dropped null values in 'date_added' and 'rating' (those with a lower percentage).
#### **2. Unnesting Values:**
We performed unnesting on the following features:
* 'director'
* 'cast'
* 'listed_in'
* 'country'
#### **3. Typecasting:**
We adjusted the data types of the following features:
- 'duration' was converted to an integer (excluding 'min' and 'seasons' from the values).
- 'date_added' was converted to datetime in the required format.
- Feature Extraction:
Additional features were extracted from 'date_added':
'date'
'month'
'year'
#### **4. Rating Categorization:**
Given the varied coded categories in the 'rating' column, we created five bins to distribute values:
- Adult: TV-MA, NC-17
- Restricted: R, UR
- Teen: PG-13, TV-14
- All Ages: TV-G, TV-Y, TV-Y7, TV-Y7-FV, PG, G, TV-PG
- Not Rated: NR

## Exploratory Data Analysis (EDA)
Detailed exploration of the dataset to uncover patterns, insights, and trends related to Netflix Movies and TV Shows. Following are the findings from EDA which are crucial for subsequent phases of the project:

  - **Content Distribution:** The dataset is skewed towards movies, constituting 69.14%, while TV shows make up 30.86%.
  - **Target Audience:** Adult and teen audiences are the primary focus of the majority of shows, as indicated by the content's nature and rating.
  - **Geographical Origin:** The United States is the predominant source of movies and TV shows, followed by India and the United Kingdom.
  - **Popular Genres:** International Movies, drama, and comedies emerge as the most popular genres on the Netflix platform.
  - **Content Recency:** Netflix emphasizes recently released content, with a larger quantity of newer movies and TV shows compared to older ones.
  - **Shift in Focus:** A noticeable decrease in the number of movies added in 2020 suggests a potential shift in focus towards introducing more TV series.
  - **Seasonal Pattern:** December exhibits the highest number of content additions, indicating a focus on the winter season.
  - **TV Show Seasons:** A significant proportion of TV shows have only one season, suggesting a preference for shorter series.
  - **Movie Durations:** The majority of movies fall within the 60 to 120-minute range, reflecting a preference for standard-length films.
