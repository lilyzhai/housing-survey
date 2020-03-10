# Ann Arbor Housing Survey
*W2020 MDST Project: a survey of housing in Ann Arbor, Michigan*

## Table of Contents 
* [Introduction](#introduction)
* [Description](#description)
* [Goals](#goals)
* [Stretch Goals](#stretch-goals)
* [A Look at the Data](#a-look-at-the-data)
* [Project Roadmap](#project-roadmap)

## Introduction
Any student at the University of Michigan knows how difficult it is to find affordable housing on- or off-campus. 
While dorms are a convenient option, they are not necessarily affordable: the cheapest undergrad housing option, a triple, comes out to about [$9,910](https://housing.umich.edu/undergraduate-rates/), or about $1,200 per month. Looking off-campus offers just as many, if not more, problems. Affordable housing is often located in inconvenient locations, while locations close to campus tend to have exorbitant prices ⁠— don't even get me started on some of the higher-end apartments! 🤯

If you're a student, grad or undergrad, you probably have a vested interest in improving the off-campus housing search. Even Ann Arbor townies might find some use in this project ⁠— housing trends around campus may be indicative of greater trends in the city at large.

## Description
The goal of this project is to conduct a detailed analysis of the state of student housing in A2 today as well as create a tool that students could feasibly use to make decisions about housing. Questions that we hope to answer include, but are not limited to:
* What trends can we observe in the listings when sorting by various features? Are there distinct trends at the neighborhood level?
* How can we develop a regression model to predict price with a reasonable degree of accuracy? What features seem to be most predictive of the price?
* Realty websites are kind of sketchy. After all, they *are* trying to sell you something! To this end, what interesting insights can we extract from the posted descriptions of each listing?
* **...and many more to be thought of!**

This is an exploratory project, so feel free to bring up anything you would like answered or explored! The scope of this project is not yet set in stone.

Join this project if you have any interest in the following:
* web systems and scraping
* data visualization
* natural language processing 
* geographic data
* machine learning 
    - supervised learning: *regression* 
    - unsupervised learning: *clustering* 
* finding housing for next year, lol

## Goals
1. Acquaint members with the basic structure and timeline of a data science project
2. Provide members with practical, hands-on experience in tools commonly used in industry and research: web scraping, regression techniques, version control, etc.
3. Identify key trends in housing and generate applicable insights that could help inform a potentially confused student in their housing search
4. Develop a regression model that can output a price range given user input; this would consist of "requirements" such as number of bedrooms, location, etc.
5. Build an interactive data visualization ⁠— a choropleth map ⁠— that best highlights trends and features
6. Publish results and visualization in the *Statement* with the Michigan Daily
7. Have fun and learn something! :)

## Stretch Goals
1. Gather historical data and visualize how features have changed over time
    - *TODO: obtain historical data (at least 5 years worth)*
2. Compare results to that of other "Ann Arbor-like" college towns (Madison, Urbana/Champaign, Durham?)
    - *TODO: develop a metric for similarity*
3. Incorporate images of the listings into the regression model
    - *TODO: a lot of pre-processing and feature engineering*
   
## A Look at the Data
Ideally, this is what a sample row from the dataset would look like after preliminary cleaning and feature extraction.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;address&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (`string`) | price (`float`) | bed (`int`) | bath (`float`)| area (`float`)| company (`string`)| neighborhood (`string`)| laundry (`boolean`)| pets (`boolean`)| parking (`boolean`)| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;utilities&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <br> (`list` of type `string`)| property_type (`string`) | year_built (`int`) | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;description&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <br> (`string`) | images <br> (`list` of type `string`) |
------- | ----- | --- | ---- | ---- | ------- | ------------ | ------- | ---- | ------- | --------- | --------------- | ------------ | ------------ | ------ |
544 N State St, Ann Arbor, MI 48104 | 4250.0 | 6 | 2.0 | `None` | PMSI | North Ingalls | 1 | 0 | 1 | water, <br> electricity, <br> heat, <br> ... | house | `None` | This wonderful 6 bedroom 2 bedroom home is... | https://s3.amazonaws.com/photos.rentlinx.com/W150/51048178.jpg, https://s3.amazonaws.com/photos.rentlinx.com/L800/51048179.jpg, https://s3.amazonaws.com/photos.rentlinx.com/L800/51048181.jpg, ... |

There will probably be a little bit more data cleaning/extraction required ⁠— for example, one-hot encoding each type of utility.

## Project Roadmap
Week of **2/15**: 
- Exploratory Data Analysis

---

Week of **2/22**:
- Geocoding
- Natural Language Processing

---

Week of **2/29**: *SPRING BREAK*

---

Week of **3/7**:
- Geocoding
- Natural Language Processing

---

Week of **3/14**:
- Regression Analysis
- Choropleth Map

---

Week of **3/21**:
- Regression Analysis
- Choropleth Map

---

Week of **3/28**:
- Choropleth Map
- Preliminary Report

We plan to submit our report to the *Statement* at this point!

---

Week of **4/4**:
- Choropleth Map
- Final Report

---

Week of **4/11**:
- Final Report
- Conclusions and Next Steps
