# Sentiment Analysis Model for Indonesian 2019 Presidential Election Tweets

This repository contains a sentiment analysis model specifically trained to analyze tweets related to the 2019 Presidential Election in Indonesia. The model is designed to classify the sentiment of tweets as positive, negative, or neutral, providing insights into public opinion during the election period. The model includes two different approaches: Random Forest and LSTM.

---

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Room For Improvement](#room-for-improvement)
- [References](#references)
- [Attachment](#attachment)

---

# Introduction

This GitHub repository presents a sentiment analysis project focused on analyzing tweets related to the 2019 Presidential Election in Indonesia. The core objective of this project is to classify the sentiment of tweets as positive, negative, or neutral, thereby offering an objective analysis of public opinion during the election period. Utilizing a dataset of 1,814 labeled tweets, the project employs two distinct analytical approaches: Random Forest and LSTM (Long Short-Term Memory) networks, each chosen for their effectiveness in processing and categorizing textual data.

The dataset, specifically collected during the 2019 election, is annotated with sentiments, providing a structured foundation for training the models. This project aims to deliver insights into the sentiment distribution among the tweets, contributing to a better understanding of public sentiment during significant political events. Through this repository, I offer a comprehensive toolkit for sentiment analysis, designed to be both robust and sensitive to the nuances of social media discourse.

---

# Dataset

The dataset comprises 1,815 entries, each representing a tweet related to the 2019 Presidential Election in Indonesia. It is organized into three columns: an unnamed column that appears to serve as an index, 'sentimen' which denotes the sentiment of the tweet categorized into `negatif` (negative), `netral` (neutral), or `positif` (positive), and `tweet` which contains the text of the tweet itself.

Entries in the dataset vary, reflecting the political discourse during the election period. For instance, one of the tweets expresses a negative sentiment regarding Indonesia's international standing, while another tweet discusses the positive impact of the Asian Games on South Sumatra, showcasing a positive sentiment. Neutral sentiments are also captured, providing a balanced view of the political landscape during that time.

This rich dataset serves as a foundational element for training the sentiment analysis models, offering a comprehensive view of public sentiment during a significant political event. It underscores the diversity of opinions and topics discussed on social media platforms, making it a crucial resource for understanding and categorizing public opinion expressed through tweets.

---

## Model Architecture

The sentiment analysis model utilizes two different approaches: Random Forest and LSTM.

## Run on Google Colab

You can run the model on Google Colab by clicking the link below:

https://colab.research.google.com/drive/1GOURcsFUYcrAh4poz9E5gyhptpzjLJ-m?usp=sharing
