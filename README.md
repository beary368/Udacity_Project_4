
# Udacity Project 4: Boston AirBnB CRISP-DM Process

## This project uses data from the Boston Metroplex's AirBnBs to answer question I posed after taking an initial look at the data. The questions are below:
  1. Is there a spatial discrepancy in price based on neighborhood?
  2. What is the price seasonality in Boston? What month is most affordable/expensive? Day of the week?
  3. What is the best predictor of price for Boston AirBnB's? How well can we model it?

# Motivation

I was motivated to explore this data as I have been a user of [AirBnB](https://www.airbnb.com/) in the past. The questions specifically were a motivation of my personal background and my current position at Mars. I have a background as a meteorologist so making maps (and making sense of them...) is a consistent part of my job. Additionally, the heavy market analysis we do in my everyday job in cocoa were the main drivers in the other questions. Thus, I combined them to fully suit my interests in the project.

# Installation

The vast majority of the packages were installed via the most recent distribution of conda
```bash
conda 4.6.14
```
All other packages (mainly Cartopy and Gmaps) were install via:
```bash
conda install -c conda-forge (Insert Package Here)
```

# Packages

### Packages I used for this project are below.
* python==3.6.4
* Numpy==1.15.4
* pandas==0.22.0
* matplotlib==2.2.2
* scikit-learn==0.20.1
    * See this website for dependent packages to install [Sklearn](https://github.com/scikit-learn/scikit-learn/blob/master/README.rst#user-installation)
* Cartopy==0.17.0
* seaborn==0.8.1
* gmaps==0.8.4
    * You will need to register an API Key on [Google Maps API](https://developers.google.com/maps/documentation/javascript/get-api-key)

# Files
There are 2 files which I utilized to answer the 3 questions. __Listings.csv__ was the main file used to answer questions 1 and 3. It contains all relevant information about the listing itself such as bedrooms, bathrooms, price, and neighborhood. __calendar.csv__ was utilized to provide context of seasonality of the price of Boston's AirBnBs. This file provided dates and relevant prices along these dates.

# Results/Findings

### Question 1: Is there a spatial discrepancy in price based on neighborhood?
  
  1. More expensive neighborhoods are downtown which intuitively makes sense.
  2. The ones which are affordable look like rooms either in a dorm or a shared room of an apartment.
  3. The expensive AirBnBs farther away from Downtown are usually multiple bedrooms and bathrooms and possibly full-size mansions. So in theory the extended commute is offset by much more housing space.
  4. There is also a conglomeration of cheaper properties west of Fenway in Allston which provides closer access to downtown attractions like Boston University, Fenway Park and Harvard/MIT.

### Question 2: What is the price seasonality in Boston? What month is most affordable/expensive? Day of the week?
  
  1. We can see the months of September and October are the most expensive months to visit Boston and stay in an AirBnB. We can also see the price drops sharply during after these periods as it becomes colder. The cheapest time appears to be February.
  2. It appears you want to visit Boston on a Weekday to get the best deal which makes sense because majority of people will be at work during this time. However, difference between the mean of a weekend price and a weekday price is less than 10 dollars or 5% of total cost.

### Question 3: What is the best predictor of price for Boston AirBnB's? How well can we model it?

  1. Some items which people would intuitively assume are included with an entire house stay (i.e. hangers, shampoo, essentials, and lock on bedroom door) have a definitely negative effect on the price. This may be due to the perception of people purchasing that the seller would only advertise these things if there is no luxury (or seen as luxury) amenities available.
  2. People who visit Boston enjoy dogs more than cats. Dogs create a premium of 7 dollars while cats have a small detraction from average price.
  3. The notion that Americans enjoy Air Conditioning is true as venues with A/C advertised garnered a 10+ dollar premium.
  4. Number of listings by a host does not factor into price.
  5. Another bedroom costs you 3.25 times as much as another bathroom would.
  6. Every person accomodated only is 6.5 dollars more, meaning a large group could save significant amounts of money over hotels if a shared space isn't a problem. Interesting as hotels usually charge premiums/multipliers for guests (guests are only 4 dollars more). 


# Authors, Acknowledgements, Licensing

* Thank you to [Kaggle](https://www.kaggle.com/airbnb/boston) and [AirBnB](https://www.airbnb.com/) for collaborating on the data for me to analyze.
* Thank you for [Udacity](https://www.udacity.com/) for providing a platform for me to explore these data sets for an interesting project.
* Thank you to Alan Mosca from Udacity for helping with the integration of Google Maps and AirBnB data.
