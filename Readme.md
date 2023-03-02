# Text Mining from Golden Globes Tweet Data #

## Problem Statement ##

Build a program to read tweets about the Golden Globes Awards and extract the critical information — as much of the following as you can:
- Host
- Award categories; Presenters
- Nominees, Favorites, Winners
- Excerpts from Winners’ statements; reactions
- Other honors, speeches
- Unexpected events
- Visuals (i.e., build a slide show)?

## Introduction ##

Process of information extraction (IE) is used to extract useful information from unstructured or semi-structured data. In this project, we focused on extracting the required information
from the json file by converting it into data frames and then going through a number of processes like Data Cleaning, EDA, Keyword analysis etc being some. This project aims to extract award information from tweets 
related to the Golden Globe Awards using text mining techniques, including natural language processing and sentiment analysis. 
The results of this project could provide a deeper understanding of public sentiment and trends surrounding the Golden Globe Awards, which could be useful for a variety of stakeholders in the entertainment industry.

## Methodology ##
We have defined functions for every task and have made a master function to call as per requirement. This way the code is easily readable and is easy to debug issues during code runs.
We have used the following concepts:
  - Read the json file and save it as a list of dictionaries
  - Pre-processing Data
    - Remove tweets containing opiniated words – think / could / should / maybe
    - Remove tweets which do not contain golden / globe
    - Scrape Actors: Used library BeautifulSoup to scrape IMDB list of all actors to validate our actor findings
    - Find Hosts: We go through each tweet and find the keyword host / Host. We also find names in the filtered tweets using regex – pair of words with first letters capital and a count of occurrences and store as a dictionary. We then sort the list and take the top 2 names.
    - Find Awards: We go through each tweet and find the keyword best / Best. We then filter the tweets by keywords Win / Wins / win / wins / goes to, and find the award names using regex – sentence of words with capital first letters starting with Best with their count of occurrences and store as a dictionary. We then sort the list and take the top 50 names.
    - Find Presenters: We go through each tweet and find the keyword presenters / presenting. We also find names in the filtered tweets using regex – pair of words with first letters capital and a count of occurrences and store as a dictionary. We then sort the list and take the top 15 names.
    - Find Nominees: We go through each tweet and find the keyword nominees / nominated. We also find names in the filtered tweets using regex – pair of words with first letters capital and a count of occurrences and store as a dictionary. We then sort the list and take the top 15 names.
    - Find Winners: Here we follow a different approach. We iterate over all the award names and search every tweet for a match. In the matches, We search the keywords wins / goes to and find the names using regex – pair of words with first letters capital and a count of occurrences and store as a dictionary. We then sort the list and take the top 50 names.
    - Report Function: Prints all the required findings in the defined format.



  ## Conclusion ##
 Information extraction from Twitter data can provide valuable insights into the specific award winners, event highlights, and trends surrounding events such as 
  the Golden Globe Awards. Text mining techniques such as natural language processing and sentiment analysis can be used to extract relevant information 
  from tweets, which can be used by businesses, researchers, and media outlets to make informed decisions. The evaluation of information extraction models
  is important to ensure that the extracted information is accurate and reliable. Common evaluation metrics such as precision and recall, F1 score, accuracy, 
  and confusion matrix can be used to evaluate the performance of the information extraction models.



