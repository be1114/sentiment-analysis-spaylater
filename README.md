# sentiment-analysis-spaylater
Analyzing SPayLater-related Twitter comments to classify sentiment (positive, negative, neutral) and identify the emotions expressed within each sentiment.

# Overview
This project focuses on analyzing public comments related to SPayLater collected from Twitter/X.

The system is designed to perform a two-stage analysis. First, each comment is classified into **Positive, Negative, or Neutral** sentiment. After the sentiment is identified, the system performs an additional analysis to determine the **emotion expressed within the comment**.

The overall concept of the project is:


## Objectives

The objectives of this project are:

* To analyze public opinions related to SPayLater.
* To classify comments into positive, negative, or neutral sentiment.
* To identify emotions expressed within the analyzed comments.
* To develop an application that allows users to analyze individual comments.
* To provide a more detailed interpretation of public feedback by combining sentiment and emotion analysis.

---

## Dataset

The dataset consists of public comments related to SPayLater collected from Twitter/X.

The collected data was processed and prepared before being used for sentiment analysis.

The dataset contains text-based comments that were labeled and prepared for the model training and evaluation process.

> The original dataset is not publicly included in this repository due to data privacy and redistribution considerations.

---

## Data Preprocessing

Text data from social media often contains informal language, symbols, links, mentions, and other elements that may affect the analysis.

Therefore, the collected comments undergo several preprocessing steps before being used by the model.

The general preprocessing workflow is:

```text id="c5m3v8"
Raw Comment
     ↓
Data Cleaning
     ↓
Text Normalization
     ↓
Tokenization
     ↓
Sequence Conversion
     ↓
Padding
     ↓
Model Input
```

The preprocessing stage prepares the text data into a format that can be processed by the LSTM model.

---

## Sentiment Analysis

The first stage of the system is sentiment classification.

The comments are classified into three sentiment categories:

* **Positive**
* **Negative**
* **Neutral**

Natural Language Processing (NLP) techniques are applied to process the text before it is passed to the classification model.

---

## LSTM Model

The sentiment classification uses an **LSTM (Long Short-Term Memory)** model.

LSTM is a type of Recurrent Neural Network (RNN) designed to process sequential data. Since text consists of sequences of words, LSTM can be used to learn patterns and relationships within text sequences.

### LSTM Workflow

```text id="0cn6e4"
Preprocessed Text
        ↓
Tokenization
        ↓
Sequence & Padding
        ↓
LSTM
        ↓
Dense Layer
        ↓
Sentiment Prediction
        ↓
Positive / Negative / Neutral
```

The model is trained using labeled text data and evaluated using a separate test dataset.

### Why LSTM?

LSTM was selected because it is designed to process sequential information and can capture patterns within sequences of words.

This makes it suitable for text classification tasks such as sentiment analysis.

---

## Emotion Detection

After the sentiment of a comment has been identified, the system performs an additional emotion detection process.

The purpose of this stage is to provide a more detailed interpretation of the detected sentiment.

For example:

```text id="uyf5xw"
Comment
   ↓
Positive Sentiment
   ↓
Emotion Detection
   ↓
Detected Emotion
```

A sentiment/emotion dictionary is used as one of the components in this process.

This allows the system to go beyond identifying whether a comment is positive, negative, or neutral and further determine the emotion expressed in the comment.

---

## Overall System

The complete process can be illustrated as follows:

```text id="2v7h7h"
             Twitter/X Comments
                     ↓
             Data Preprocessing
                     ↓
              Sentiment Analysis
                     ↓
          ┌──────────┼──────────┐
          ↓          ↓          ↓
       Positive   Negative    Neutral
          │          │          │
          └──────────┼──────────┘
                     ↓
              Emotion Detection
                     ↓
              Emotion Result
```

The system therefore provides two levels of information:

**Level 1 — Sentiment**

> Positive / Negative / Neutral

**Level 2 — Emotion**

> The emotion associated with the analyzed comment.

---

## Technologies

The project was developed using:

* **Python**
* **Natural Language Processing (NLP)**
* **LSTM (Long Short-Term Memory)**
* **TensorFlow / Keras**
* **Pandas**
* **NumPy**

Additional libraries and frameworks may be used for application development and data processing.

---

## Application

The model and analysis process are implemented into an application that allows users to enter a comment and obtain the sentiment and emotion analysis results.

### Application Interface

![Application Interface](screenshots/home.png)

### Input

Users can enter a comment related to SPayLater into the application.

![Input](screenshots/input.png)

### Analysis Result

The application displays the detected sentiment and emotion.

![Analysis Result](screenshots/result.png)

---

## Example of Analysis

The following examples illustrate the analysis process:

| Comment                                                          | Sentiment | Emotion   |
| ---------------------------------------------------------------- | --------- | --------- |
| "SPayLater sangat membantu untuk kebutuhan saya."                | Positive  | [Emotion] |
| "Saya kecewa karena mengalami masalah saat menggunakan layanan." | Negative  | [Emotion] |
| "Saya menggunakan SPayLater untuk melakukan pembayaran."         | Neutral   | [Emotion] |

> The examples above are illustrative and should be replaced with actual examples and results from the system.

---

## Model Evaluation

The LSTM model is evaluated using several classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

### Performance

| Metric    | Score |
| --------- | ----: |
| Accuracy  |   XX% |
| Precision |   XX% |
| Recall    |   XX% |
| F1-Score  |   XX% |

### Confusion Matrix

![Confusion Matrix](screenshots/confusion-matrix.png)

The evaluation results provide an indication of how well the model performs in classifying the sentiment categories.

---

## Results and Insights

The analysis provides an overview of public sentiment toward SPayLater and the emotions expressed within those comments.

By combining sentiment classification and emotion detection, the system can provide a more detailed understanding of public feedback.

The analysis can be used to identify:

* The distribution of positive, negative, and neutral comments.
* Common emotions expressed by users.
* Patterns in positive and negative feedback.
* Potential areas of customer experience that may require further attention.

### Key Findings

**Finding 1:**
[Write your actual finding based on the analysis.]

**Finding 2:**
[Write your actual finding based on the analysis.]

**Finding 3:**
[Write your actual finding based on the analysis.]

---

## Source Code

Selected application source code is provided in this repository:

* `view.py`
* `server.py`

The core implementation details, trained model, sentiment/emotion dictionary, and original dataset are not publicly included.

This repository is intended to demonstrate the project's concept, implementation, analysis process, and results while keeping selected internal components private.

---

## Skills Demonstrated

This project demonstrates experience in:

* Data Collection and Preparation
* Data Cleaning
* Natural Language Processing
* Sentiment Analysis
* Emotion Detection
* Machine Learning
* LSTM
* Python Programming
* Model Evaluation
* Data Interpretation
* Application Development

---

## Project Purpose

This project was originally developed as part of an academic research project and is presented here as a portfolio project.

The project demonstrates the application of data processing, NLP, machine learning, and analytical techniques to extract insights from public social media comments.

---

## Disclaimer

This project is intended for academic and portfolio purposes.

The analysis is based on publicly available comments collected from Twitter/X and does not represent the official opinions, policies, or statements of SPayLater or its affiliates.
