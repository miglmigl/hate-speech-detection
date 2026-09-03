# Hate Speech Detection in Tweets

University group project for the Natural Language Processing course.

## Overview

A machine learning model was built to classify English tweets as **offensive
(OFF)** or **not offensive (NOT)**.

1. **Data preparation** – tweets are cleaned (mentions, URLs, `MENTION###`
   placeholders and punctuation removed), tokenised, stop-words removed and
   words lemmatised. The training set is balanced so both classes have an equal
   number of tweets.
2. **Exploration** – a word cloud is generated from the cleaned tweets.
3. **Feature extraction** – several representations are computed:
   - sentiment (polarity, subjectivity)
   - text formatting (`!` count, `?` count, uppercase-word count, length)
   - TF-IDF
   - Word2vec (averaged word vectors)
4. **Training** – a Logistic Regression classifier is trained on each feature
   set separately and on all features combined, then compared with
   precision, recall, F1 and accuracy.
5. **Evaluation on new data** – the best model is tested on a separate set of
   political tweets and on a sexism dataset to check how well it generalises.
6. **Visualisation** – results are plotted as bar and line charts.
