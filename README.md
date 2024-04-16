# Sentiment Analysis of Twitter Data.

## Introduction

![]()

This project scrapes data from twitter using the nitter library, uses Power Query for data cleaning and Text Analytics for sentiment classification. Then uses Power BI desktop for visualization.


## Skills Demonstrated
-	Web Scraping
-	Data Analysis (Power Query)
-	Text Analytics (Power Query)
-	Data Visualization (Power BI Desktop)



## Data Collection and Gathering
Utilizing the Nitter library, tweets were collected from the Twitter platform, focusing on the hashtag 'jagunjagunmovie.' The collected data serves as the foundation for the sentiment analysis system. The data collection spanned a specific time frame, from August 10, 2023, to September 10, 2023.
### Feature Extraction
Features crucial for sentiment analysis were extracted from the collected tweets using the Nitter library. These features include user information, tweet text, date, and engagement metrics. The goal was to capture relevant information for sentiment classification.
### Data Storage
The final processed data was stored in a CSV file ('twitter_data_final.csv'). System design includes considerations for efficient data storage and retrieval, ensuring that the data is accessible for further analysis.


## Tools and Techniques Used
This section elaborates on the tools and techniques employed in the sentiment analysis process. It includes details about libraries, frameworks, and technologies utilized for data preprocessing, feature extraction, sentiment analysis modeling, and visualization.
### Python Libraries
Python libraries, often referred to simply as "libraries" or "modules," are collections of pre-written code that provide a wide range of functionalities to extend the capabilities of the Python programming language. These libraries contain reusable functions, classes, and constants that programmers can leverage to expedite development, simplify coding tasks, and enhance the performance of their Python applications. Some of the libraries used for this project includes:
-	Pandas (pd): Pandas is a powerful data manipulation and analysis library for Python. It provides data structures like DataFrames and Series, which are efficient for handling structured data. Pandas is widely used for data cleaning, manipulation, analysis, and visualization tasks in data science and machine learning projects.
-	Nitter: Nitter is a privacy-friendly front-end for Twitter. It allows users to view Twitter content without JavaScript, cookies, or tracking. Nitter provides an alternative way to access Twitter content while preserving privacy.
-	WordCloud: WordCloud is a Python library used to generate word clouds from text data. A word cloud is a visual representation of text data, where the size of each word indicates its frequency or importance within the text. Word clouds are often used to quickly understand the most common words in a text corpus or to visualize word frequency distributions.
-	Matplotlib.pyplot (plt): Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. ‘pyplot’ is a submodule of Matplotlib that provides a MATLAB-like plotting interface. It allows users to create plots, charts, histograms, and other visualizations with ease.
### Power BI
Power BI is a business analytics service provided by Microsoft, offering users an intuitive interface to interactively visualize and analyze data. It allows connections to various data sources such as databases and spreadsheets, enabling users to create data models with relationships between different datasets. With a rich set of visualization tools, users can generate interactive charts, graphs, and maps to explore their data. Power BI facilitates the creation of dashboards and reports for monitoring key metrics and trends, and it supports collaboration and sharing features for easy dissemination of insights within organizations.


## Data Cleaning
The generated csv file(“twitter_data_final”) was imported to Power Query from Power BI desktop for cleaning and preprocessing.
 
Figure 4.1 – Power Query Editor
In the Power Query editor, the following steps were taken to ensure that the data is ready for analysis:
-	Remove Index Column
This column was removed because it is not useful in the analysis. Right-click on the column and select “Remove” from the options.
 
Figure 4.2 – Remove Index Column
-	Format Date Column
 Figure 4.3 –Date column before formatting
The following steps were taken to format the date column:
-	Replace UTC with nothing by clicking on replace values in the Transform tab.
- Split the date column by position 0,4,7,12.
- The date column is then split into 4 columns.
-	Remove “date.4” column.
-	Change the data type of date.2 and date.3 to text data type. Click on “Whole Number” in the home tab and click on “Text” for both columns.
-	Merge date.1, date.2 and date.3 to a single column using custom columns in “Add Columns” tab.
-	Change the data type of the new date column to “Date” and rename to Date.
-	Remove date.1, date.2 and date.3 columns.
 
Figure 4.4 – Date column after being formatted
## Sentiment Analysis
Power Query was utilized to apply Sentiment Score for sentiment analysis using "Text Analytics." Several steps were executed, including scoring sentiment, filtering null values, and creating additional columns to categorize sentiments and include corresponding emoji URLs.
-	Click on Text Analytics on the Home Tab.
-	Click on Score Sentiment and use the text column.
-	A new column (Score sentiment) is created.
-	The data type is “Any” by default. Change the data type to “Decimal”.
-	Filter to remove rows where score sentiment is null.
-	Rename score sentiment to Score by double-clicking on the column name and typing score.
-	Add a conditional column called Sentiment Score to say if the score is Positive, Negative or Neutral.
-	Change the data type of Sentiment Score to “Text”.
-	Add another conditional column named Icon URL to include the URLs of happy, sad and neutral emojis to indicate Positive, Negative and Neutral Scores respectively. The URL was gotten from icons8.com website.
-	Change the data type of Icon URL to “Text”.
-	Close and apply to Power BI desktop for analysis and visualization.


## Word Cloud Generation
A Word Cloud was generated to visually represent the most frequently occurring words in the collected tweets. The WordCloud library was employed with parameters set to limit the number of words and customize the background colour. The resulting visualization provides an overview of prominent words in the dataset.
 
Figure 4.5 – Word Cloud Visual.


## Visualization Using Power BI
Power BI was used to create visualizations to aid analysis of the result.
 
Figure 4.6 - Dashboard
You can interact with the dashboard using this link - https://tinyurl.com/SentimentAnalysisDashboard
### Analysis of The Result
-	The tweets were collected from about 3,500 users.
-	The tweets gathered had a total of about 182,000 likes and 27,000 retweets.
-	Most of the tweets gathered are positive because according to the analysis, 49.38% of the tweets are positive while 17.02% are negative and 33.6% are neutral.


## Conclusion
In conclusion, the sentiment analysis system developed in this study offers valuable insights into audience sentiment surrounding 'jagunjagunmovie.' Despite limitations, the system's findings contribute to a deeper understanding of audience preferences and perceptions in the digital age. Moving forward, continued refinement and innovation are essential to unlocking the full potential of sentiment analysis in shaping the future of content creation and audience engagement strategies.


## Recommendations
These are the recommendations based on the insights gained from the sentiment analysis project.
-	Encouraging organizations to leverage sentiment analysis tools and techniques to better understand customer feedback and market trends.
-	Advocating for the integration of sentiment analysis capabilities into decision-making processes in various industries.
-	Promoting further collaboration between academia and industry to advance sentiment analysis research and applications.
-	Providing resources and support for organizations to implement and utilize sentiment analysis effectively in their operations.

By implementing these recommendations, the sentiment analysis system can evolve into a robust tool for monitoring and understanding audience sentiment in the dynamic landscape of social media, facilitating informed decision-making, and enhancing audience engagement strategies in the entertainment industry.
