# Airbnb Recommendation System

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Processing](#data-processing)
3. [Models Used](#models-used)
    - [Popularity-Based Model](#popularity-based-model)
    - [Collaborative Filtering](#collaborative-filtering)
    - [Content-Based Model](#content-based-model)
    - [Hybrid Model](#hybrid-model)
4. [Interactive Dashboard](#interactive-dashboard)
5. [Model Performance and Similarity Scores](#model-performance-and-similarity-scores)
6. [Conclusion](#conclusion)
7. [Limitations](#limitations)
   
## Project Overview
Our Airbnb Recommendation System aims to improve the precision of property matches on Airbnb, setting a benchmark for future enhancements. By integrating state-of-the-art machine learning models and sophisticated data handling techniques, our system ensures scalability and adaptability. As we continue to refine our algorithms and expand our dataset, we anticipate further advances in user experience and system performance, promising a new era of personalized travel planning.

## Data Processing
We use the package Airbnb Scraper from Apify to obtain our raw data. We manually inputted 47 most visited cities in the world selected by GoVisity. Furthermore, we selected the Airbnb features we think are crucial for building our recommendation system, such as room type, number of bedrooms, number of guests, etc. The data frame was reshaped by creating dummy variables to represent the presence or absence of specific amenities. We also selected the most frequent listing amenities as variables to simplify our model.

## Models Used
### Popularity-Based Model
This model recommends properties based on their popularity among users. Popularity can be determined by total weight score (a function of various metrics).

### Collaborative Filtering
This model analyzes user behavior and preferences over similar users to predict what current users might like. It includes URL input-based recommendations.

### Content-Based Model
Content-based aspects consider the features of the listings (like amenities, style, etc.) matched against keywords provided by the user.

### Hybrid Model
Combines collaborative filtering and content-based models to provide more accurate and personalized recommendations.

## Interactive Dashboard
https://github.com/Jessicalllll/AirbnbRecommendation/assets/77706422/966c8f80-5978-425e-8358-fae786b7d441

## Model Performance and Similarity Scores

| Model                           | Largest Similarity | Average Similarity |
|---------------------------------|--------------------|--------------------|
| Popularity Model                | 45.23%             | 41.37%             |
| Hybrid Model (CF & CB)          | 75.48%             | 82.05%             |
| Collaborative Filtering Model   | 67.34%             | 56.63%             |


## Conclusion

Our Airbnb recommendation system showcases three distinct models, each with their strengths in matching user preferences with available properties. The Hybrid Model demonstrates the highest average similarity score at 82.05%, indicating its superior performance in providing personalized recommendations. The Collaborative Filtering Model follows, with the Popularity Model having the lowest average similarity score. This evaluation highlights the effectiveness of combining multiple approaches to enhance the accuracy and relevance of recommendations.

## Limitations

Common limitations across all models include data availability and limited contextual understanding because we have a relatively small dataset. Addressing these challenges requires a combination of data enrichment, algorithmic refinement, and continuous monitoring to enhance recommendation accuracy and user satisfaction.

## References

- [Airbnb Scraper](https://console.apify.com/actors/GsNzxEKzE2vQ5d9HN/console )
- [GoVisity: Top 50 Most Visited Cities in the World](https://govisity.com/most-visited-cities-in-the-world/)
