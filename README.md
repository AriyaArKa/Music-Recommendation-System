# 🎵 Music Recommendation System Using Machine Learning

A content-based music recommendation web app that suggests similar songs based on lyrical content. This project leverages natural language processing and cosine similarity to help users discover new music that resonates with their favorite tracks.

![Screenshot](static/img.png)

## 🚀 Features

- Enter a song name to get top 20 similar song suggestions.
- Content-based filtering using TF-IDF and cosine similarity.
- Responsive and stylish UI powered by Bootstrap.
- Preprocessed song lyrics from a Kaggle dataset.

## 🧠 How It Works

This system uses a **content-based filtering** approach:
1. Clean and preprocess song lyrics (lowercase, remove special characters, stemming).
2. Convert lyrics into vectors using **TF-IDF Vectorizer**.
3. Compute **cosine similarity** between song lyrics.
4. Return top N similar songs based on similarity scores.

## 🛠️ Tech Stack

- **Frontend**: HTML, Bootstrap 5
- **Backend**: Flask (Python)
- **ML/NLP**: Scikit-learn, NLTK
- **Data**: [Kaggle - Songs Recommendation Dataset](https://www.kaggle.com/datasets/noorsaeed/songs-recommendation-dataset)

## 📦 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/AriyaArKa/Music-Recommendation-System.git
   cd Music-Recommendation-System
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download dataset from Kaggle and prepare `df.pkl` and `similarity.pkl`:

   ```python
   from kaggle.api.kaggle_api_extended import KaggleApi
   api = KaggleApi()
   api.authenticate()
   api.dataset_download_files('noorsaeed/songs-recommendation-dataset', path='data/', unzip=True)
   ```

5. Run the app:

   ```bash
   python app.py
   ```

6. Visit `http://127.0.0.1:5000` in your browser.

> ⚠️ Note: GitHub does not support files larger than 100MB. Make sure your `similarity.pkl` and `df.pkl` are under this limit or use Git LFS.

## 📁 Project Structure

```
├── app.py
├── df.pkl
├── similarity.pkl
├── static/
│   ├── img.png
│   └── screenshot.png
├── templates/
│   └── index.html
├── data/
│   └── songdata.csv
├── README.md
└── requirements.txt
```

## 🖼️ UI Preview

![Screenshot 12](https://github.com/AriyaArKa/Music-Recommendation-System/blob/main/images/Screenshot%20_12.png)
![Screenshot 13](https://github.com/AriyaArKa/Music-Recommendation-System/blob/main/images/Screenshot%20_13.png)
![Screenshot 14](https://github.com/AriyaArKa/Music-Recommendation-System/blob/main/images/Screenshot%20_14.png)
![Screenshot 15](https://github.com/AriyaArKa/Music-Recommendation-System/blob/main/images/Screenshot%20_15.png)




## 📌 Future Enhancements

- Add audio previews using Spotify API.
- Enable fuzzy matching for typos in song search.
- Add user-based collaborative filtering support.

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

🔗 Connect with me on [LinkedIn](https://www.linkedin.com/in/arka-nath55/) | 🌟 Star the repo if you found it helpful!