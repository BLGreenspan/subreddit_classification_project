# Using Data Science to Write Comedy
#### Brandon Greenspan: [LinkedIn](https://https://www.linkedin.com/in/brandonlgreenspan)

## Problem Statement
I am a comedy writer (True Story). I've run out of my own original ideas, so in order to get a good idea to pitch to Mike Schur, I want to find common word choice/themes that fans of both The Good Place and Parks & Recreation are using. In order to accomplish this, I will need to build a classification model. While the success metric I'm aiming for in the model selection is accuracy, ultimately, my goal is to find the words that the model misclassifies in order to best identify the overlap of both shows that might indicate what elements a successful Mike Schur show would contain. Ideally, I want the accuracy rate of a selected model to be above 90%, which means that my model should be a better predictor than the baseline model, but not too accurate because I actually need enough misclassification to come up with show ideas. If the model theoretically did not misclassify any variables, then I would have an blank page, which is not an improvement upon how many comedic ideas I can conjure.

Before I get to meet Michael Schur, I have to present my process for showrunners at NBC, which is not a technical audience.

## Executive Summary
As I comedy writer, I'm only as good as my last script.  Unfortunately, I haven't written any good scripts, and I have accepted the fact that if I can't succeed with comedic talent, I can succeed with data.  Michael Schur had a lot of success with sitcoms like The Office, Parks & Rec, Brooklyn 99, The Good Place, and many more.  I have the ambitious goal to pitch a show idea to Michael Schur, while generating my show idea from data.

In order to generate a show that Michael Schur would want to develop, I will scrape the Subreddits for Parks & Rec and The Good Place to get an idea of what truly resonated with fans.  Data cleaning is fairly minimal since we are only working with Booleans and Strings, so we won't need to impute any string data.  To get a better understanding of our data, we will see how long our posts are as well as the most common words used for each Subreddit.  Out of these common words, we will create a custom stoplist for modeling.

After calculating our baseline model, we will run a Train, Test, Split for the purposes of training and testing any future models, and evaluating the accuracy scores of each model.  The classification models we build are Logistic Regression, Multinomial Naive Bayes, Gaussian Naive Bayes, KNN, & Support Vector Machine.  Since we will be using a gridsearch method for all of these models in order to finetune our hyperparameters, this does take some time to run.

Once we select a model, we will investigate our confusion matrix and assess the model's accuracy, sensitivity, specificity, precision, and true negative rates to get a sense as to the strength of the model beyond the initial accuracy score that led to its selection.  Then, we'll evaluate the strongest coefficients that the model is built on to see which words/phrases are the strongest predictors of a certain show.  Lastly, we'll dig into the words and phrases that most often lead to misclassification.

After looking at our misclassified words, we'll finally try to generate a sitcom idea.  Will the idea be enough to impress Mike Schur?

## Project Files
These data came from this:
[Parks & Rec Subreddit](https://www.reddit.com/r/PandR/)
[The Good Place Subreddit](https://www.reddit.com/r/TheGoodPlace/)


## Data Dictionary
[Data Dictionary for Original Data Categories](https://pushshift.io/api-parameters/)


## Conclusion
The Multinomial Bayes model scored between 93-97% on accuracy, so we were able to achieve our modeling goal from a statistical standpoint, however writing comedies is hard.  This model can't necessarily guarantee a successful pilot.  A lot of the overlap happens on words that still aren't overly descriptive towards themes, but let's give this a shot.

Interestingly the model seems to misfire on scouts, so I think my show would have to do with campers or talent scouts.  Song is another word the model misfires on.  The words hilarious, actress, charity, and podcast also appear.  Yes, I see it now- the lead is a hilarious struggling actress named Charity, who gets casted on a singing show by Don, the talent scout for the show, who fell in love with our leading actress at first sight, and offerred her a spot on his show without hearing her sing, so he can be around her.  Will Don's "charity offer" to cast a struggling actress, also named Charity, professionally and romanticly pay off?  If she can't sing, Don's career is over.  If Charity discovers Don's motivations, will she get disgusted and leave the show altogether?  Last thing, Don is British (UK and England are also stopwords).

This actually does seem like a fun idea to develop.  Maybe the lead actress or a supporting character also has a podcast.  If we're truly judging our goal, this did generate an idea that my comedic ineptitude wouldn't have discovered on its own.  Now I just need to develop the characters and pitch it to Mike Schur.


## Recommendations
If I were to implement this further and look for even more ideas, I would probably run a decision tree model and possibly try a bootstrapping and bagging method (which I wasn't able to due to time constraints).  Additionally, I might look deeper into which rows misclassified and adjust my stopwords to improve accuracy.  I could even look to scrape more subreddits and attempt to classify new Subreddits in addition to The Good Place and Parks & Rec.  If I do that, I would likely have to rely more on boosting, bagging, and bootstrapping since I would be running classification on more than one target variable.

All of this would likely result in a more accurate model, but once again, I don't want to be too accurate because then I wouldn't be left with many words to generate ideas.


## References
- [Parks & Rec Subreddit](https://www.reddit.com/r/PandR/)
- [The Good Place Subreddit](https://www.reddit.com/r/TheGoodPlace/)



```python

```
