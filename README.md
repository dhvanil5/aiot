📜 Project Description
The goal of this project is to analyze and compare public opinion on social media. By processing thousands of tweets, the application determines the emotional tone (positive, negative, or neutral) of the conversation surrounding each political figure. The dashboard presents these findings through a series of intuitive charts and statistical summaries, making it easy to understand the nuances of public sentiment at a glance.

This project was developed for an expo to showcase the real-world applications of Natural Language Processing (NLP) in analyzing public discourse.

✨ Key Features
Interactive Dashboard: A web-based interface built with Streamlit for easy interaction.

At-a-Glance Metrics: Key statistics like total tweet counts and average sentiment scores are displayed in metric cards.

Sentiment Breakdown: Bar and pie charts visualize the distribution and proportion of positive, negative, and neutral sentiments for each figure.

Qualitative Word Analysis: The dashboard extracts and displays the most frequently used words in both positive and negative tweets, offering insight into why the sentiment is what it is.

Non-Neutral Analysis: A "Deeper Dive" section filters out neutral tweets to provide a clearer view of the positive vs. negative opinion divide.

Statistical Validation: An independent samples t-test is performed to verify if the difference in sentiment between the two figures is statistically significant.

🛠️ Technologies Used
Python: The core programming language for the project.

Streamlit: For building and deploying the interactive web application.

Pandas: For data manipulation and analysis.

TextBlob: For performing the core sentiment analysis (calculating polarity).

Plotly Express: For creating interactive and aesthetically pleasing data visualizations.

NumPy & SciPy: For numerical operations and statistical tests (t-test).

🚀 Setup and Running the Project
Follow these steps to get the application running on your local machine.

1. Prerequisites
Make sure you have Python 3.7+ installed.

2. Clone the Repository (Optional)
If your code is in a Git repository, clone it:

Bash

git clone <your-repository-url>
cd <your-repository-directory>
3. Install Required Libraries
Install the necessary Python packages using pip.

Bash

pip install streamlit pandas textblob plotly scipy
4. Prepare Your Data
Ensure the following CSV files are in the same directory as your Streamlit application script (app.py):

rahul_reviews.csv

modi_reviews.csv

5. Run the Streamlit App
Execute the following command in your terminal:

Bash

streamlit run app.py
Your web browser will automatically open with the dashboard running.

🔬 Methodology
The project follows a systematic approach to sentiment analysis:

Data Loading: Two CSV files containing tweets are loaded into pandas DataFrames.

Data Cleaning: Basic preprocessing is performed, such as handling missing values.

Sentiment Scoring: For each tweet, the polarity is calculated using the TextBlob library. Polarity is a float between -1.0 (most negative) and +1.0 (most positive).

Sentiment Classification: Based on the polarity score, each tweet is labeled as:

Positive (Polarity > 0)

Negative (Polarity < 0)

Neutral (Polarity = 0)

Data Visualization: The processed data is visualized using Plotly to create comparative charts that highlight key differences in sentiment.

Statistical Analysis: A t-test is conducted to provide a statistical measure of the significance of the findings.
