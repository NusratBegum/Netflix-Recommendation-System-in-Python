# Netflix Movies & TV Shows Recommendation System

A comprehensive data analysis and content-based recommendation system built on the Netflix Movies and TV Shows dataset.

## Project Overview

This project performs exploratory data analysis (EDA) on Netflix's content library and implements a content-based recommendation engine using TF-IDF vectorization and cosine similarity.

## Features

- **Exploratory Data Analysis**: In-depth analysis of content distribution, genres, countries, ratings, and temporal patterns
- **Feature Engineering**: Creation of derived features for enhanced analysis
- **Statistical Testing**: Hypothesis testing to validate key observations
- **Recommendation System**: Content-based filtering using natural language processing techniques

## Dataset

**Source**: [Kaggle - Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)

The dataset contains information about movies and TV shows available on Netflix, including:
- Title, type, director, cast
- Country of production
- Release year and date added to Netflix
- Content rating and duration
- Genre categories and descriptions

## Project Structure

```
├── main.ipynb          # Main Jupyter notebook with analysis and model
├── README.md           # Project documentation
└── requirements.txt    # Python dependencies (if applicable)
```

## Analysis Highlights

### Content Distribution
- Movies comprise ~70% of Netflix's library
- TV Shows account for ~30%, with increasing additions in recent years

### Geographic Insights
- United States dominates content production
- India and United Kingdom are significant contributors

### Genre Trends
- International Movies, Dramas, and Comedies are most prevalent
- Different genre distributions between Movies and TV Shows

### Temporal Patterns
- Content additions peak towards year-end
- Friday is the most common day for new releases

## Recommendation System

The recommendation engine uses:
- **TF-IDF Vectorization**: Converts text features into numerical vectors
- **Cosine Similarity**: Measures content similarity based on feature vectors
- **Combined Features**: Genres, director, cast, country, rating, and description

### Usage

```python
# Get recommendations for a title
recommendations = get_recommendations("Stranger Things", top_n=10)

# Or use the user-friendly function
recommend_netflix("The Crown", show_details=True)
```

## Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation
- **NumPy** - Numerical operations
- **Matplotlib & Seaborn** - Data visualization
- **scikit-learn** - TF-IDF vectorization and similarity computation
- **SciPy** - Statistical testing

## Key Findings

1. Netflix has been shifting focus towards TV Shows in recent years
2. Content rating and type are significantly associated
3. US content is over-represented compared to other countries
4. Movies and TV Shows have different release year distributions

## Future Improvements

- Implement collaborative filtering with user viewing data
- Add sentiment analysis on content descriptions
- Build a hybrid recommendation system
- Create an interactive web application
- Incorporate user ratings and reviews

## Installation

```bash
# Clone the repository
git clone https://github.com/NusratBegum/Netflix-Recommendation-System-in-Python.git

# Navigate to project directory
cd Netflix-Recommendation-System-in-Python

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn scipy kagglehub

# Open the notebook
jupyter notebook main.ipynb
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

Nusrat Begum

---

*Built as part of a data science internship project, December 2025*
