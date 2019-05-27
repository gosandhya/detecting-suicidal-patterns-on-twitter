# Project: Detecting Suicidal Patterns in Twitter Data
______________________________________________________________________________________________________

In this project, I aimed to use twitter data to detect patterns of suicidal behavior. Twitter data was collected from 232 individuals marked with a presence of suicide or healthy status. The objective of this research is three-fold: First, to analyze the timely change in individual’s speech as they get close to their committing suicide. Whether there are key diﬀerences in the patterns and behaviors among them and those who are marked healthy. Second, to build a predictive model to predict the risk of suicide in Twitter users. Lastly, to analyze and compare the network structure of userfollower relationship among the two groups. The results showed the tweets of individuals marked with suicide became less positive in the last 10 days before the suicide. The number of tweets was lower implying that individuals became less active. The network structure of healthy individuals are much dense and more connected than the ones marked as a suicide. The binary predictive model based on support vector machine can correctly build a tweet belonging to suicide group 50% the time and correctly predict the other label 98% of the time.



![word cloud](https://github.com/SandhyaaGopchandani/DetectingSuicidalPatternsTwitter/blob/master/word_cloud_last_seven_days.png)

Figure above shows the most frequent words used by the people who died of suicide seven days before their last tweet. The analysis can be extended to any time period by just specifying the number of days in the code line. The reason to do this analysis is to see if there is change of speech overtime as they progress towards the last day. The plot seems to highlight some interesting patterns as I see it. In the last 7 days, the more noticeable words are vicious, apology, hairloss, thank, love etc. But looking only at the word frequency may not be a good idea because the total number of tweets (hence words) in those time period may vary hinting towards a biased result.



![sentiment per day for last 10 days in affected group](https://github.com/SandhyaaGopchandani/DetectingSuicidalPatternsTwitter/blob/master/sentiment_affected_last_ten_days.png)

Figure 3 shows the average sentiment of tweets per over the last 10 days before the suicide compared to Figure 4 that shows the same analysis for healthy people. The reason to do this analysis to detect the overall emotion/sentiment of one day over the other. This might hint towards whether the pattern to be positive or negative on daily basis is same or diﬀerent for suicidal vs healthy individuals. Figure 3 shows that people who are at suicidal risk may not express the negative speech but their tendency to be positive in the speech has lowered as approaching the last day. Surprisingly, the negative sentiment is missing altogether for last 4 days. The one reason could be the lower number of tweets implying that they become less active on social media.

![sentiment per day for last 10 days in healthy group](https://github.com/SandhyaaGopchandani/DetectingSuicidalPatternsTwitter/blob/master/sentiment_healthy_last_ten_days.png)

Figure 4 shows the average sentiment per day for healthy individuals. The results seems to be as expected. The sentiment seems to hint towards randomness or due to chance which it should be. Mood might be one factor behind diﬀerent sentiments for each day but not following an ongoing pattern as it seems to be with the individuals with suicide status.



![confusion matrix](https://github.com/SandhyaaGopchandani/DetectingSuicidalPatternsTwitter/blob/master/confusion_matrix.png)

Shown above is the confusion matrix that compares the predicted and test label accuracy in terms of Precision and Recall. The dark blue is true negative that is probability, the model correctly predicting the ’no’ label and bottom value on diagonal marked as 0.46 is true positive rate that is the probability, a model correctly predicted ’yes’ label. Ideally, we want these two probabilities to be 1. So, it is apparent that there is need to improve on the True Positive Rate.

![network structure in affected group](https://github.com/SandhyaaGopchandani/DetectingSuicidalPatternsTwitter/blob/master/net_struct_affected_group.png)


Figure above shows the network structure of aﬀected group. The red colored nodes are the twitter ids of aﬀected individuals and nodes in yellow are the people who they follow. Overall, it seems that this group is inclusive and not very dense, implying that individual who are aﬀected do not form huge networks, but it is hard to say because there are only 4 nodes. This network might not be good representative of overall network structure of aﬀected group.

#### notes

Please refer to jupyter notebook (suicidal_pattern_analysis.ipynb) for the code and the PDF file (article) to read more about the analysis details.
