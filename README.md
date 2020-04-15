Wordsmiths---Parsing-Yelp-Data
--------
The Goal of this project is to be able to review restaurants through a use of key words, that we call "b0ugie words".
By taking millions of Yelp reviews, and then filtering by only the restaurants that receive all 5-star reviews, we were hoping to find a correlation between certain words and good reviews.
First, we did try with other parameters, like if the restaurant had a coat check, valet parking or other characteristics that would typically be associated with more expensive restaurants. But that data turned out to be too inconsistent and not a good indicator of quality. There is also just a lot fewer data points with anything other than star reviews, as basically all restaurants on Yelp have some review, but few have any of the other characteristics.
So, in order to find the "bougie words" we first filtered by Stars = 5 to see what words were the most common.
Using ReGex we remove stopwords and do some other clean ups and then filter by frequency.
Then we take all of the words that are in all non 5-star reviews, and eliminate them from our Bougie Word list, creating a list of words that are unique to 5-star reviews.
Then we take those words and query against all reviews again to see which restaurants have the highest number of those words.

