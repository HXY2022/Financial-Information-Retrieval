<img width="401" alt="image" src="https://user-images.githubusercontent.com/101479845/163987059-903b3592-46dd-4217-b138-7c3a2c5ce966.png">  

# Financial Information Retrieval
This is the file for the explanation of the report of Financial Information Retrieval. 

With the development of the gaming industry, the potential of gaming is becoming greater. However, it is challenging to survive without a good strategy. This report focuses on the comments on an incumbent in the gaming ecosystem to help game manufacturers create great and long-life games. This project aims to categroy the key features on a good game to provide suggestions for game producers.

# API

we use both offical and third-party APIs to collect data from Steam, Reddit and Metacritic.

<img width="100" alt="截屏2022-04-19 11 50 21" src="https://user-images.githubusercontent.com/101479845/163988140-f6d1f721-eb99-4f2b-96c0-a294b900e91f.png">Steam: Steam is a video game digital distribution storefront launched in 2003. It is the largest digital distribution platform for PC gaming holding nearly 75% and taking up at least 18% of PC game sales.

<img width="91" alt="image" src="https://user-images.githubusercontent.com/101479845/163988647-e92ff8a7-aae3-423a-847b-dbce2e731e5e.png">Reddit: Reddit is a website that provides a platform for users to send posts. 

<img width="95" alt="image" src="https://user-images.githubusercontent.com/101479845/163988991-aa897059-d083-4667-a687-547bfddd1c36.png">Metacritic: MetaCritic is a professional review website for games, books and movies, and TV shows. 

## Steam-webspider-2018 & steam-webspider-2019-2021

This is how we use webspider to retrive data from steam.

## steam-review-api

This is how we use the official api-steamworks to collect data from steam.

## reddit-api

This is how we use pushshift to collect data from reddit.

## metacritic-api

This is how we use beautifulsoup package to collect data from Metacritic.

## natural-language-processing

We use natural language processing to generate the wordcloud for comments from steam, reddit and metacritic as well as the sentiment analysis by introducing the positive and negative lexicons.

## feature-filter & feature-filter rating

We defined non-feature related words as stopwords, and delete them from the comments to identify the key features.

## Authors

* **Group 9 ** 
* 2675497y
* 2637982x
* 2539533h
* 2638024h
* 2632079h
