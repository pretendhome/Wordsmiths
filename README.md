# Wordsmiths---Parcing-Yelp-Data
The Goal of this project is to be able to review resturants through a use of key words, that we call "bugie words".  

By taking millions of Yelp reviews, and then filtering by only the resturants that receive all 5 star reviews, 
we were hoping to find a cooralation between certain words and good reviews.

First we did try with other paramaters, like if the resturant had a coat check, valet parking or other characteristics
that would typically be assoicated with more expensive resturants.  But that data turned out to be too inconsistant and 
not a good indicator of quality.  There is also just a lot fewer data points with anything other that star reviews, as 
basically all resturants on Yelp have some review, but few have any of the other characteristics.

So, in order to find the "bougie words" we first filtered by Stars = 5 to see what words were the most common.

Using ReGex we remove stopwords and do some other clean ups and then filter by frequency.

Then we take all of the words that are in all non 5 star revews, and eliminate them from our Bougie Word list, creating
a list of words that are unique to 5 star reviews.

Then we take those words and query against all reviews again to see which resturants have the hightest number of those words.
