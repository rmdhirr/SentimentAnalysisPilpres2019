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

# Methodology
## 1. Data Checking

The data checking phase is crucial for ensuring the dataset's quality and readiness for analysis. This involves a series of steps aimed at understanding the dataset's structure, refining its contents, and verifying its completeness.

### 2. Print The Head of The Dataset

Initially, the dataset is examined by looking at the first few entries. This step provides insight into the structure and content of the data, including the presentation of tweets and their associated sentiment labels.

### 3. Drop Unnamed Columns

Upon inspection, any unnecessary columns that do not contribute to the analysis are identified and removed. Specifically, an unnamed column, likely serving as an index, is removed to streamline the dataset and focus on relevant data.

### 4. Null Checking

A thorough check for missing values is conducted to ensure the dataset's integrity. Identifying and addressing any null values is essential to avoid inaccuracies in the sentiment analysis. A dataset without missing values in key columns is crucial for a robust analysis.

These steps collectively enhance the dataset's quality, making it well-prepared for an in-depth sentiment analysis by ensuring cleanliness, relevance, and completeness of the data.

---

## Exploratory Data Analysis

Exploratory Data Analysis (EDA) is conducted to uncover insights and patterns within the dataset, specifically focusing on the sentiment-laden tweets related to the 2019 Indonesian Presidential Election. This section details the analytical techniques employed to dissect the dataset.

### 1. Word Clouds

#### Positive Sentiment
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/6f70d28c-6701-4665-b58b-7205d6264530)

#### Negative Sentiment
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/37208081-dc60-4ac3-ab93-66185efd5b96)

#### Neutral Sentiment
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/088c81db-4058-4f20-844e-81c3a7842be6)

### 2. Sentiment Distribution

The distribution of sentiments within the dataset is analyzed to understand the proportion of positive, negative, and neutral tweets. This analysis provides insight into the overall sentiment landscape of the dataset, revealing the dominant emotional tones conveyed in the tweets.

![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/d86b07ee-2412-4c58-a144-a8ff08c5f14f)

### 3. Tweet Length Distribution

The length of tweets is examined across different sentiment categories. This analysis helps in understanding if the sentiment expressed is correlated with the length of the tweets, offering insights into the verbosity of expressions associated with each sentiment.

![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/d0790745-94c8-4f0a-af64-b7bcc5da92a5)

### 4. Most Common Words

The most frequently occurring words in each sentiment category are identified and visualized. This step delves into the specific language and terminology associated with positive, negative, and neutral sentiments, providing a deeper understanding of the lexical choices in sentiment expression.

#### Most Common Words in Positive Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/430d915d-56f7-4edd-8407-519a84c9db21)

#### #### Most Common Words in Negative Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/78d75df6-cbee-4904-9f7a-f0c3ba31c16a)

#### Most Common Words in Neutral Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/3a1d8d5f-eb82-41eb-af13-c9e6b4ccc6c3)

### 5. Number of Unique Words

The diversity of vocabulary across different sentiment categories is quantified by counting the unique words used in each category. This analysis sheds light on the lexical richness and variety in the expression of sentiments.

![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/c6994077-f890-4fda-9172-cc29e9baa2fa)

### 6. Top Hashtags and Mentions

The most common hashtags and mentions are identified for each sentiment category, highlighting the key topics and public figures that are frequently referenced in the context of each sentiment. This aspect of the analysis connects the tweets to broader discussions and narratives.

#### Top Hashtags in Positive Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/d6b91c08-9085-4c01-b5aa-5283a4bd9ce8)

#### Top Mentions in Positive Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/f8e4f449-8e49-48f5-a8c1-5289ba8206b2)

#### Top Hashtags in Negative Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/197b9e26-51e9-4bb0-98f2-37a6773560b2)

#### Top Mentions in Negative Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/5b3cc39e-d7c2-4201-a4ea-be48725ef174)

#### Top Hashtags in Neutral Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/230d8874-66aa-4935-98e8-55a1555ae0cc)

#### Top Mentions in Neutral Tweets
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/8364cedf-52a9-44c6-be6d-f513410f3c2e)

### 7. Average Word Length

The average length of words within tweets of each sentiment category is calculated and compared. This analysis provides insights into the complexity and informativeness of the language used to express different sentiments.

![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/eeedf023-376f-49fd-a07d-d24dfb01ed06)

Each of these analytical steps contributes to a comprehensive understanding of the dataset, revealing patterns, trends, and characteristics inherent in the sentiment-laden tweets. This EDA forms the basis for further modeling and analysis in the sentiment classification task.

---

## Preprocessing

The preprocessing phase is essential for cleaning and standardizing the dataset to enhance the performance of sentiment analysis models. This section details the steps taken to preprocess the tweets.

### Preprocess Caption

The initial step involves a comprehensive preprocessing of tweet texts, which includes converting all text to lowercase, removing hashtags, numbers, non-ASCII characters, URLs, mentions, punctuation, and excessive whitespaces. Additionally, repeating characters are reduced to a single instance to normalize variations in word spellings. Emoji codes within the tweets are converted to their corresponding emoji characters to retain emotional expressions. These steps collectively refine the text, making it more uniform and analytically viable.

### Replace Slang Words

Slang words prevalent in social media texts are replaced with their standard equivalents using a predefined dictionary of slang terms. This process ensures that informal expressions commonly used in tweets are standardized, aiding in the accurate interpretation of the text's sentiment.

### Apply Preprocessing

The cleaned tweet texts undergo further preprocessing, which includes applying the aforementioned caption preprocessing and slang replacement functions. This multi-step cleaning process ensures that the dataset is devoid of irrelevant and noisy elements, focusing solely on meaningful content.

#### Dataset Post-preprocessing
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/63aafb5b-4318-4a31-aaa8-8060cd1e1119)

### Word Cloud After Preprocessing

Post-preprocessing, word clouds are generated for each sentiment category to visually represent the most common words in the cleaned dataset. This visualization helps in assessing the effectiveness of the preprocessing steps and in understanding the predominant themes and expressions in the refined texts, providing insights into the sentiments expressed in the tweets.

#### Word Cloud for Positive Sentiment (Post-preprocessing)
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/f33a6a81-3f91-4f30-b493-790b4ad07fe8)

#### Word Cloud for Negative Sentiment (Post-preprocessing)
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/4c82b075-0797-4e80-820b-308a8aed16ae)

#### Word Cloud for Neutral Sentiment (Post-preprocessing)
![image](https://github.com/aridofflimits/SentimentAnalysisPilpres2019/assets/147245715/353fe57f-cdcd-480a-a32f-b8af85ea2de2)

---


## Model Architecture

The sentiment analysis model utilizes two different approaches: Random Forest and LSTM.

## Run on Google Colab

You can run the model on Google Colab by clicking the link below:

https://colab.research.google.com/drive/1GOURcsFUYcrAh4poz9E5gyhptpzjLJ-m?usp=sharing
