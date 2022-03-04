

# Did JK Rowling take from JRR Tolkien?
## NLP with Reddit

---

### The Problem
#### Similarities Between the two Popular Series
Many people believe that JK Rowling took her ideas for Harry Potter from JRR Tolkien's Lord of the Ring Series… 
To prove this controversy, I wanted to make two models. One with unique keywords, and one without unique keywords. Unique keywords are words that would make it obvious to the model which subreddit a particular post came from. If the model built without the keywords did worse than the model built with the keywords, this may indicate a similarity between the material in the two books based off of their associated subreddit.

---

### Background
#### Common Themes
There are many themes that correspond with one another:

The ring bearer/ The chosen one
Gandalf the Grey/ Albus Dumbledore
Sauron the Deceiver/ Voldemort
The ring/ The horcruxes
Nazgul/ The dementors
Gollum/ The Elves
Shelob/ Aragog
Mirror of Galadriel/ Mirror of Erised-Pensieve
Dead Marshes/ Inferi
The power of the ring/ Legilimens


### Data Formatting and Modeling

I used Reddits API to obtain posts from two subreddits: Lord of the Rings, and Harry Potter. I then cleaned the data, took care of nulls and appended the data to a data frame for further processing and modeling. With null handling, I replaced nulls with empty spaces. I used pipelines to construct classification models fit with additional parameters for natural language processesing (NLP). My first model was able to identify which posts belonged to which subreddit with 97% accuracy, while the second model was unable to fit without the keywords present. This could be for many reasons, but my hypothesis is that the model did not do so well because the siilarities between the two subreddits without the unique keywords were great, proving my problem statement. 

---

### Observations

I observed that when taking out the keywords, the model failed to fit. This may be for many reasons, but I believe that it is because the material in both subreddits are so similar that they were no longer distinguishable to the model. This would prove my hypothesis that JK Rowling did draw deep inspiration from JRR Tolkein.

---

### Next Steps
From here there are many avenues to explore. There is trying to improve the model trying out various models, plotting a 3D vector map of word usage to see which had the greatest weight, sentiment analysis, and model stacking. 
