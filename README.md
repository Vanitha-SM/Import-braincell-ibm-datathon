# Import-braincell-ibm-datathon

# **Scam Website and Product Detection Model**

This repository contains the code and resources for a machine learning model that detects scam websites and fake product information using data from Instagram, YouTube, Reddit, and other sources. The model applies natural language processing (NLP) techniques and various APIs to fetch, clean, and analyze data, enabling effective scam detection.

## **Table of Contents**
- [Introduction](#introduction)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Setup](#api-setup)
  - [Instagram API](#instagram-api)
  - [YouTube Data API](#youtube-data-api)
  - [Reddit API (PRAW)](#reddit-api)
- [Model Pipeline](#model-pipeline)
  - [Data Collection](#data-collection)
  - [Data Cleaning](#data-cleaning)
  - [NLP and Feature Extraction](#nlp-and-feature-extraction)
  - [Model Training](#model-training)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## **Introduction**

This project implements a scam detection system using machine learning techniques. It gathers data from multiple sources like Instagram ads, YouTube reviews, and Reddit discussions, processes the data, and builds an NLP model to detect scam content. The final model is deployed using a Flask API hosted on IBM Z LinuxONE.

## **Tech Stack**

This project uses the following technologies:

1. **Programming Language**: Python
2. **APIs and Web Scraping**:
   - Instagram Graph API
   - YouTube Data API
   - PRAW (Reddit API)
   - BeautifulSoup / Scrapy (optional for extra scraping)
3. **Data Preprocessing**:
   - Pandas
   - Numpy
   - Regular Expressions (Regex)
4. **Natural Language Processing**:
   - NLTK or SpaCy
   - TfidfVectorizer
   - Transformers (BERT, RoBERTa, GPT)
5. **Machine Learning**:
   - Scikit-learn (traditional models)
   - TensorFlow / PyTorch (deep learning)
6. **Database**:
   - PostgreSQL / MySQL
   - MongoDB
7. **Deployment**:
   - Flask or FastAPI
   - Docker
   - IBM Z LinuxONE Server

## **Features**
- Fetches and processes data from social media platforms.
- Utilizes state-of-the-art NLP techniques for text analysis.
- Supports both traditional machine learning and deep learning models.
- REST API for easy integration and real-time predictions.
- Deployed using Docker and Flask on IBM's cloud infrastructure.

## **Installation**

### Prerequisites
- Python 3.x
- Pip (Python package manager)
- Docker (optional for deployment)

### Clone the repository:
```bash
git clone https://github.com/your_username/scam-detection-model.git
cd scam-detection-model
```

### Install dependencies:
```bash
pip install -r requirements.txt
```

### Set up environment variables:
Create a `.env` file in the root directory and add the following:
```
youtube_api_key = 'AIzaSyDkP39RCjbjNVY853VQakvrfjskH-HA2-M'
reddit_client_id = 'aDhpqC7OZRkRfJ9sRFkIpg'
reddit_client_secret = 'J-_NSxzycV7naFkK4BkQKHlMiaqrew'
reddit_user_agent = 'SocialMediaDataScraper/1.0 (by u/HotDistribution5334)'
```

## **Usage**

Run the project locally:

```bash
python main.py
```

This will start the data collection process, preprocess the data, train the model, and serve the Flask API.

## **API Setup**

### **Instagram API**
1. Create an Instagram developer account and generate an access token.
2. Add your Instagram Access Token to the `.env` file.

### **YouTube Data API**
1. Set up a Google Cloud project and enable the YouTube Data API.
2. Add your YouTube API Key to the `.env` file.

### **Reddit API**
1. Create a Reddit app and obtain your Client ID, Secret, and User Agent.
2. Add these to the `.env` file.

## **Model Pipeline**

### **1. Data Collection**
- Instagram ads are fetched using the Instagram Graph API.
- YouTube video reviews are collected via the YouTube Data API.
- Reddit discussions are fetched using the Reddit API (PRAW).

### **2. Data Cleaning**
- Text data is cleaned using Pandas and Regex to remove unnecessary characters, stop words, etc.

### **3. NLP and Feature Extraction**
- TfidfVectorizer is used to convert text data into numerical features.
- Advanced NLP models like BERT or RoBERTa can be used for feature extraction.

### **4. Model Training**
- Both traditional models (Logistic Regression, SVM) and deep learning models (Neural Networks) are supported.
- The model is trained on scam-related data, and hyperparameters are optimized for the best performance.

## **Deployment**
- The Flask application is containerized using Docker.
- Deployment is managed on IBM Z LinuxONE for enhanced scalability and security.

## **Contributing**
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for more details.


