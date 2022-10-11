![Header](https://github.com/cmhollman/Phase_4_Project/blob/main/Images/twitter_header.jpeg)



# Tweet Sentiment Classifier Using NLP

**Author**: [Chris Hollman](mailto:chollman91@gmail.com)

## Overview

The goal of this project is to build a classification model capable of categorizing tweets by sentiment. The final product will be a set of visualizations that could be used to quickly identify popular topics and provide a sense of the prevailing public opinion.

## Business Problem

An online publication group would like to leverage twitter data in order to provide resources for their writers to create content more efficiently. The final product should help cut down research time and maximize the output of relevant, well-informed articles. 


## Data

The data for this project comes from one dataset which is included in this repository:
-Data/tweet_data.csv

The data consist of about 9,000 tweets compiled by CrowdFlower. These tweets are focused on the 2012 South by Southwest (SXSW) conference. This event happens annually in Austin, Texas and celebrates innovation in technology and performing arts. The data in this set is tagged by sentiment (Postive, Negative, No Sentiment) and is directed towards either Apple or Google products. As you can see in the following graph, there was a substantial class imbalance present in this dataset.

![sentiment_dist](https://github.com/cmhollman/Phase_4_Project/blob/main/Images/brand_sent_dist.png)

## Methods

We applied both a Multinomial Naive Bayes model and an AdaBoost model to the tweets. With there being such a large class imbalance, f1 scores for the minority groups (positive and negative sentiment)


## Results

Our model is still very much a work in progress. The confusion matrix below is from our current working model which is able to classify a small number of tweets from the minority classes correctly. This is an improvement from the baseline model, which only ever predicted that a tweet belonged to the majority class. The 'final' model achieved a .60 overall accuracy score on test data.

![Conf_mat](https://github.com/cmhollman/Phase_4_Project/blob/main/Images/conf_mat_adb.png)


## Conclusions

The final visualizations from this project are available in the presentation (linked at the bottom of this file). Based on these visuals I would recommend the following to a writer tasked with writing about SXSW 2012:

-**iPad 2 Design Breakdown** The iPad 2 made major waves, being mentioned in more tweets than even the Apple brand itself. A deeper look into these tweets revealed a split in the overall public opinion of the iPad's design and overall quality. A detailed review would be of interest to the many people interested in purchasing a new tablet.

-**Failed Launch of Circles** Google was set to launch and new social network called "Circles" at SXSW 2012. There was quite a bit of buzz around it but the launch simply never occured. Since Circles was mentioned very frequently in both positive and negative Google tweets, a look into why the launch didn't happen would make for a compelling story. 

-**Marissa Mayer** An overview of the festival as a whole would be wise to include at least a brief look into Marissa Mayer's presence at the festival. She was mentioned frequently among positive tweets pertaining to Google, and many of them included very quotable excepts from her presentation. 

### Next Steps

-**More Minority Class Data** Our model's lack of performance is largely due to the huge class imbalance. If more examples of negative tweets that vaugely relate to tech can't be sourced, the model can be redesigned either by building a binary classifier or by undersampling the majority class. Ultimately, this decision may influence which classification model will be at the heart of the project.

-**Testing Other Subject Matter** Ideally, our model should be able to work reasonably well within a variety of subjects. It would be prudent to test its ability on tweets pertaining to other realms. 

-**More Recent Tweets** The tweets in this dataset are over 10 years old at this point. More recent (and balanced) data should result in greater model performance.


## For More Information

See the full analysis in the [Jupyter Notebook](https://github.com/cmhollman/Phase_4_Project/blob/main/Review_NLP.ipynb) 

or review this [presentation](https://github.com/cmhollman/Phase_4_Project/blob/main/NLP_Project_Slides.pdf).

For additional info, contact Chris Hollman at [chollman91@gmail.com](mailto:chollman91@gmail.com)


## Repository Structure

```
├── Data
├── Images
├── NLP_Project_Slides.pdf
├── README.md
└── Twitter_NLP.ipynb