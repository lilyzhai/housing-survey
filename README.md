# Ann Arbor Housing Survey
*W2020 MDST Project: a survey of housing in Ann Arbor, Michigan*

## Introduction
Any student at the University of Michigan knows how difficult it is to find affordable housing on- or off-campus. 
While dorms are a convenient option, they are not necessarily affordable: the cheapest undergrad housing option, a triple, comes out to about [$9,910](https://housing.umich.edu/undergraduate-rates/), or about $1,200 per month. Looking off-campus offers just as many, if not more, problems. Affordable housing is often located in inconvenient locations, while locations close to campus tend to have exorbitant prices; don't even get me started on some of the higher-end apartments! 🤯

If you're a student, grad or undergrad, you probably have a vested interest in improving the off-campus housing search. Even Ann Arbor townies might find some use in this project ⁠— housing trends around campus may be indicative of greater trends in the city at large.

## Description
The goal of this project is to conduct a detailed analysis of the state of (student) housing in A2 today. Questions that we hope to answer include, but are not limited to:
* Where is the "optimal" place to live, taking into account features such as price, room size, and location? Can we come up with a metric for optimality?
* What are the most desirable areas, and (how) can we predict a posting's "desirability"?
* What trends can we observe when we sort by various metrics or features? 
* What features are most predictive of the price? Any surprising insights?  
* **...and many more to be thought of!**

This is an exploratory project, so feel free to bring up anything you would like answered or explored! The scope of this project is not yet set in stone.

Join this project if you have any interest in the following:
* web systems and scraping
* data visualization
* natural language processing 
* machine learning 
    - regression 
    - supervised learning
* finding housing for next year, lol

## Goals 
1. Acquaint members with the basic structure and timeline of a data science project
2. Provide members with practical, hands-on experience in tools commonly used in industry and research: web scraping, regression techniques, version control, etc.
3. Identify key trends in housing and generate applicable insights that could help a potential confused student decide where to sign next year
4. Publish results and visualization in the Michigan Daily
5. Have fun and learn something! :)

## Stretch Goals
1. Gather historic data and visualize how features have changed over time
2. Compare results to that of other "Ann Arbor-like" college towns (Madison, Urbana/Champaign, Durham?)
    - *this needs to be formalized: develop a metric for similarity first*
3. Price prediction?
    - *given a location, predict how much housing is likely to cost (this is a simple regression task; probably too easy!)*
  
## A Look at the Data
Ideally, this is what a sample row from the dataset would look like after cleaning and feature extraction.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;address&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (`string`) | price (`int`) | bed (`int`) | bath (`int`)| area (`int`)| company (`string`)| neighborhood (`string`)| laundry (`boolean`)| pets (`boolean`)| parking (`boolean`)| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;utilities&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <br> (`list` of type `string`)| property_type (`string`) | year_built (`int`) | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;description&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <br> (`string`) | images <br> (`list` of type `string`) |
------- | ----- | --- | ---- | ---- | ------- | ------------ | ------- | ---- | ------- | --------- | --------------- | ------------ | ------------ | ------ |
544 N State St, Ann Arbor, MI 48104 | 4250 | 6 | 2 | `None` | PMSI | Medical Campus | 1 | 0 | 1 | water, <br> electricity, <br> heat, <br> ... | house | `None` | This wonderful 6 bedroom 2 bedroom home is... | https://s3.amazonaws.com/photos.rentlinx.com/W150/51048178.jpg, https://s3.amazonaws.com/photos.rentlinx.com/L800/51048179.jpg, https://s3.amazonaws.com/photos.rentlinx.com/L800/51048181.jpg, ... |

There will probably be a little bit more data cleaning/extraction required ⁠— for example, one-hot encoding each type of utility.
