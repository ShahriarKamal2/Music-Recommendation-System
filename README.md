# Music-Recommendation-System

Music recommendation system using Spotify track features, clustering, and KNN-based similarity search.

## 📋 Overview

This project implements an intelligent music recommendation system that leverages Spotify's track features and machine learning algorithms to discover songs similar to your favorites. The system uses data clustering and K-Nearest Neighbors (KNN) similarity search to provide personalized music recommendations.

## ✨ Features

- **Spotify Integration**: Fetch track features and metadata from Spotify API
- **Feature Engineering**: Process and normalize Spotify audio features
- **Clustering**: Group similar songs using unsupervised learning techniques
- **KNN-Based Search**: Find the most similar tracks using K-Nearest Neighbors algorithm
- **Recommendation Engine**: Generate personalized music recommendations based on user preferences
- **Scalable Architecture**: Handle large music datasets efficiently

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Spotify Developer Account ([Create one here](https://developer.spotify.com/dashboard))
- pip package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ShahriarKamal2/Music-Recommendation-System.git
cd Music-Recommendation-System
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Set up Spotify API credentials:
   - Create a `.env` file in the project root
   - Add your Spotify API credentials:
```
SPOTIFY_CLIENT_ID=your_client_id
SPOTIFY_CLIENT_SECRET=your_client_secret
```

### Usage

```python
from recommendation_system import MusicRecommender

# Initialize the recommender
recommender = MusicRecommender()

# Get recommendations for a specific track
recommendations = recommender.get_recommendations(track_id='track_id', n_recommendations=10)

# Display recommendations
for track in recommendations:
    print(f"{track['name']} by {track['artist']}")
```

## 🔧 Project Structure

```
Music-Recommendation-System/
├── README.md
├── requirements.txt
├── src/
│   ├── data_fetcher.py          # Spotify API integration
│   ├── feature_processor.py      # Feature engineering and normalization
│   ├── clustering.py             # Clustering algorithms
│   ├── knn_search.py             # KNN similarity search
│   └── recommender.py            # Main recommendation engine
├── notebooks/
│   └── exploratory_analysis.ipynb # Data exploration and visualization
├── data/
│   └── tracks.csv               # Sample track data
└── tests/
    └── test_recommender.py      # Unit tests
```

## 🎯 How It Works

1. **Data Collection**: Fetch music tracks and their features from Spotify API
2. **Feature Normalization**: Scale audio features to ensure uniform importance
3. **Clustering**: Group similar tracks using K-means or similar algorithms
4. **Similarity Search**: Use KNN to find nearest neighbors in feature space
5. **Recommendation**: Return the most similar tracks sorted by relevance

### Key Spotify Features Used

- Acousticness
- Danceability
- Energy
- Instrumentalness
- Key
- Liveness
- Loudness
- Speechiness
- Tempo
- Valence

## 📊 Performance

The system efficiently processes and recommends from large music catalogs with:
- Sub-second query times for recommendation retrieval
- Scalable KNN implementation for large datasets
- Optimized clustering for improved grouping accuracy

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request with your improvements.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- [Spotify Web API](https://developer.spotify.com/documentation/web-api) for providing access to track features
- Scikit-learn for machine learning algorithms
- The open-source community for inspiration and tools

## 📧 Contact

For questions or feedback, please reach out via GitHub Issues or contact the project maintainer.

---

**Happy Music Discovering!** 🎵
