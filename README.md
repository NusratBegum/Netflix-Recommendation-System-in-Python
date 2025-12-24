# 🎬 Netflix Movies & TV Shows - Recommendation System

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

A comprehensive data analysis and content-based recommendation system for Netflix Movies and TV Shows using Python. This project performs extensive Exploratory Data Analysis (EDA) and builds an intelligent recommendation engine using machine learning techniques.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Key Findings](#key-findings)
- [Recommendation System](#recommendation-system)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🎯 Overview

This project analyzes Netflix's content library to uncover insights about viewing patterns, content distribution, and trends. It includes a sophisticated content-based recommendation system that suggests similar movies and TV shows based on various features like genres, cast, director, and descriptions.

### What Makes This Project Special?

- **Comprehensive EDA**: Deep dive into Netflix's content with 20+ visualizations
- **Advanced Feature Engineering**: 14+ engineered features from raw data
- **Statistical Analysis**: Hypothesis testing to validate insights
- **Smart Recommendations**: TF-IDF and cosine similarity-based recommendation engine
- **Professional Visualizations**: Netflix-themed color palette and styling
- **Interactive Analysis**: Ready-to-use Jupyter notebook with detailed explanations

## ✨ Features

- 📊 **Exploratory Data Analysis**
  - Content distribution (Movies vs TV Shows)
  - Geographic analysis (content by country)
  - Temporal trends (release years, addition patterns)
  - Genre and rating analysis
  - Duration analysis

- 🔬 **Statistical Testing**
  - Release year distribution analysis
  - Content type vs rating association
  - Geographic content representation
  - Temporal trend analysis

- 🤖 **Recommendation System**
  - Content-based filtering
  - TF-IDF vectorization (5000 features)
  - Cosine similarity matching
  - Multi-feature recommendations (genre, cast, director, description)

- 🎨 **Professional Visualizations**
  - Netflix-branded color scheme
  - Interactive plots
  - Clean, publication-ready figures

## 📁 Dataset

**Source**: [Netflix Movies and TV Shows Dataset on Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

**Details**:
- **8,807 titles** (Movies and TV Shows)
- **12 features**: show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description
- **Date Range**: Content added from 2008 to 2021
- **Coverage**: Global content from 100+ countries

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Kaggle account (for dataset download)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/NusratBegum/Netflix-Recommendation-System-in-Python.git
   cd Netflix-Recommendation-System-in-Python
   ```

2. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or install packages individually:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn scipy kagglehub jupyter
   ```

3. **Configure Kaggle credentials** (if needed)
   ```bash
   # Place your kaggle.json in ~/.kaggle/
   mkdir -p ~/.kaggle
   cp /path/to/kaggle.json ~/.kaggle/
   chmod 600 ~/.kaggle/kaggle.json
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook main.ipynb
   ```

## 💻 Usage

### Quick Start

Open `main.ipynb` and run all cells to:
1. Download and load the Netflix dataset
2. Perform comprehensive EDA
3. Build the recommendation system
4. Get personalized recommendations

### Get Recommendations

```python
# Use the recommendation function
recommend_netflix('Stranger Things')

# Or use the detailed function
recommendations = get_recommendations('Breaking Bad', top_n=10)
```

### Example Output

```
🎬 NETFLIX RECOMMENDATIONS FOR: 'STRANGER THINGS'
🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬🎬

📺 Top 10 Similar Titles:

1. Nightflyers
   Type: TV Show | Genre: TV Horror, TV Mysteries, TV Sci-Fi & Fantasy
   Rating: TV-MA | Year: 2018 | Match: 56.2%

2. Helix
   Type: TV Show | Genre: TV Horror, TV Mysteries, TV Sci-Fi & Fantasy
   Rating: TV-MA | Year: 2015 | Match: 55.3%
...
```

## 📂 Project Structure

```
Netflix-Recommendation-System-in-Python/
│
├── main.ipynb              # Main Jupyter notebook with complete analysis
├── README.md               # Project documentation (this file)
└── .gitignore             # Git ignore file
```

### Notebook Sections

1. **Data Loading & Initial Exploration**
   - Library imports
   - Dataset loading
   - Initial data inspection

2. **Feature Types Analysis**
   - Data types examination
   - Feature categorization

3. **Data Cleaning & Preprocessing**
   - Missing value handling
   - Data type conversions
   - Text preprocessing

4. **Feature Engineering**
   - Date feature extraction
   - Duration parsing
   - Genre and country splitting

5. **Exploratory Data Analysis**
   - Distribution analysis
   - Temporal trends
   - Geographic insights
   - Genre analysis

6. **Hypothesis Testing**
   - Statistical tests
   - Trend validation

7. **Content-Based Recommendation System**
   - TF-IDF vectorization
   - Similarity computation
   - Recommendation function

8. **Conclusions & Insights**
   - Key findings
   - Summary report

## 🛠️ Technologies Used

- **Python 3.8+**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib & Seaborn**: Data visualization
- **Scikit-learn**: Machine learning and NLP
  - TfidfVectorizer: Text feature extraction
  - Cosine Similarity: Content matching
- **SciPy**: Statistical analysis
- **Kagglehub**: Dataset management
- **Jupyter**: Interactive development environment

## 🔍 Key Findings

### Content Distribution
- **Movies**: 6,131 titles (69.6%)
- **TV Shows**: 2,676 titles (30.4%)
- Netflix has been increasingly adding TV Shows in recent years

### Geographic Insights
- **Top Producer**: United States (3,211 titles)
- **Other Major Producers**: India, United Kingdom
- Content from 100+ countries represented

### Content Characteristics
- **Most Common Rating**: TV-MA (Mature Audiences)
- **Top Genres**: International Movies, Dramas, Comedies
- **Average Movie Duration**: ~100 minutes
- **Average TV Show Seasons**: 1.8 seasons

### Temporal Patterns
- Peak content addition: End of year (Q4)
- Most additions on Fridays
- Release years span 1925-2021

## 🤖 Recommendation System

### How It Works

The recommendation system uses **Content-Based Filtering**:

1. **Feature Extraction**: Combines multiple text features
   - Genres (listed_in)
   - Cast members
   - Director
   - Country
   - Rating
   - Description

2. **Text Vectorization**: TF-IDF (Term Frequency-Inverse Document Frequency)
   - 5,000 feature matrix
   - Captures content uniqueness

3. **Similarity Computation**: Cosine Similarity
   - Measures content similarity (0-1 scale)
   - Higher scores = more similar content

4. **Recommendation Generation**
   - Ranks all titles by similarity
   - Returns top N matches

### Performance
- **Matrix Size**: 8,807 titles × 5,000 features
- **Computation Time**: < 1 second per recommendation
- **Accuracy**: High relevance based on content features

## 📊 Results

The project successfully:

✅ Analyzed 8,807 Netflix titles with comprehensive visualizations  
✅ Identified key trends in Netflix's content strategy  
✅ Validated hypotheses using statistical tests  
✅ Built a functional recommendation system  
✅ Generated relevant recommendations for various content types  

### Sample Recommendations

For **"Stranger Things"** (Sci-Fi TV Show):
- Nightflyers (56.2% match)
- Helix (55.3% match)
- Chilling Adventures of Sabrina (54.4% match)

For **"Breaking Bad"** (Crime Drama):
- Dare Me (51.1% match)
- The Lizzie Borden Chronicles (49.9% match)
- Ozark (47.5% match)

## 🚀 Future Improvements

- [ ] Implement collaborative filtering using user data
- [ ] Add sentiment analysis on descriptions
- [ ] Create hybrid recommendation system
- [ ] Build interactive web application (Flask/Streamlit)
- [ ] Include user ratings and reviews
- [ ] Add real-time trending analysis
- [ ] Implement deep learning models (neural networks)
- [ ] Create API for recommendations

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Contact

**Nusrat Begum**

- GitHub: [@NusratBegum](https://github.com/NusratBegum)
- Project Link: [https://github.com/NusratBegum/Netflix-Recommendation-System-in-Python](https://github.com/NusratBegum/Netflix-Recommendation-System-in-Python)

## 🙏 Acknowledgments

- Dataset provided by [Shivam Bansal on Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- Inspired by Netflix's recommendation algorithms
- Thanks to the open-source community

---

**⭐ If you found this project helpful, please consider giving it a star!**

---

*Last Updated: December 2025*
