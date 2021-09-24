# Product Recommendation System for e-commerce business

### Introduction

Recommender systems are one of the most valuable applications of machine learning today. E-Commerce giants like Amazon attributes over 20% of their revenue to recommendations, and companies like YouTube and Netflix rely on them entirely to allow their users to discover new content. 

So what are Recommender Systems? To put it simply, Recommender System is a tool helping users find content and overcome information overload. It predicts interests of users and makes recommendation according to the interest model of users. 

There are several techniques to build a recommender system. Let us look at some of them here:

#### 1. Popularity based Recommendation System

It is a type of recommendation system which works on the principle of popularity and or anything which is in trend. These systems check about the product or movie which are in trend or are most popular among the users and directly recommend those.

For example, if a product is often purchased by most people then the system will get to know that the product is most popular so for every new user who just signed it, the system will recommend such popular products to the user and chances are high that the new user will also purchase them.

These type of recommendation systems does not provide personalized recommendations. It would recommend the same sort of products to all users, which are solely based upon popularity of the product.

#### 2. Content based Recommendation System

This is the simplest approach to building a recommender system, where items are recommended based on the attributes of the item themselves. For example, a movie recommender system may recommend movies based on genre, that we know the user likes. We may also combine different attributes of the movies item such as genre, year of release, director, lead actor etc. to make the recommendations more effective.

In case of products, we may use attributes such as product description, price, brand etc. to make the recommendations.

#### 3. Neighborhood – Based Collaborative Filtering

This is the idea of leveraging the behavior or others to inform what you might enjoy. At a very high level, it means finding other people like you and recommending stuff they liked. Or it might mean finding other things similar to the things that you like. That is, recommending stuff people bought who also bought the stuff that you liked. Either way, the idea is taking cues from people like you, your neighborhood, if you will, and recommending stuff based on the things they like that you haven't seen yet. That's why we call it collaborative filtering. It's recommending stuff based on other people's collaborative behavior. 


## Background

E-Commerce web stores have millions of products available in their catalogs. Finding the right product becomes difficult because of this ‘Information overload’. Users get confused and this puts a cognitive overload on the user in choosing a product. Recommender systems have become an integral part of e-commerce sites and other businesses like social networking, movie/music rendering sites. They have a huge impact on the revenue earned by these businesses and also benefit users by reducing the cognitive load of searching and sifting through an overload of data. Recommender systems personalize customer experience by understanding their usage of the system and recommending items they would find useful.

## Problem Statement

The goal of this project is to build Top-N recommender system using the different techniques mentioned above.

In this project, we will be working with Amazon Review Data from UCSD website (http://deepyeti.ucsd.edu/jianmo/amazon/index.html). This dataset contains product reviews and metadata from Amazon, including 233.1 million reviews spanning May 1996 – Oct 2018. The dataset includes reviews (ratings, text, helpfulness votes), product metadata (descriptions, category information, price, brand, and image features), and links (also viewed/also bought graphs).

Because of the vast size of the data, we will be working with a particular category of products - <b> Luxury Beauty </b>.

link:
http://deepyeti.ucsd.edu/jianmo/amazon/categoryFiles/Luxury_Beauty.json.gz
http://deepyeti.ucsd.edu/jianmo/amazon/metaFiles2/meta_Luxury_Beauty.json.gz


## Code Description

1. Data Loading and Preprocessing - This file contains the code for extracting the data from zip files, cleaning and preprocessing the data. Some EDA and basic data visualization has also been performed here. Finally, a cleaned CSV file is generated from this code, which is used for futher processing by the different recommendation systems.

2. Popularity Based Recommender System - This file contains the code for generating the top 10 most popular prodcuts based on the weighted score of the average rating and rantings count for each product.

3. Content Based Recommender System - This file contains the code for finding the list list of top 10 most similar products to the one rated by a user, based on the product description. Here we have used tfidfvectorizer to generated the tfidf matrix of the product descriptions and the terms used in them. Then using linear kernel (cosine similarity) we have generated the similarity score between different descriptions, to find the products that are most similar in description.

4. Collaborative Filtering Recommender System - This code contains the code for user-based and item-based collaborative filtering. Here we have used a python library <b> SurpriseLib </b> to generate the recommendations. We have used the KNN algorithm and cosine similarity metric for calculating distance.




