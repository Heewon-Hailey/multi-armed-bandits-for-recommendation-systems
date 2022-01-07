# multi-armed-bandits-for-recommendation-systems



## About the project
Multi-armed bandits (MABs) are a simple but powerful framework for sequential decision making under
uncertainty. Through the 2000s, Yahoo! Research led the way in applying MABs to problems in online
advertising, information retrieval, and media recommendation. One of their many applications was to Yahoo!
News, in deciding what news items to recommend to users based on article content, user profile, and the
historical engagement of the user with articles. Given decision making in this setting is sequential (what do we
show next?) and feedback is only available for articles shown, Yahoo! researchers observed a perfect formulation
for MABs like those (-Greedy and UCB) learned about in class. Going further, however, they realised that
incorporating some element of user-article state requires contextual bandits: articles are arms; context per
round incorporates information about both user and article (arm); and f0; 1g-valued rewards represent clicks.
Therefore the per round cumulative reward represents click-through-rate, which is exactly what services like
Yahoo! News want to maximise to drive user engagement and advertising revenue. In this project, you will
work individually (not in teams) to implement several MAB algorithms. Some will be directly from class, while
others will be more advanced and come out of papers that you will have to read and understand yourself.
By the end of the project you should have developed:
ILO1. A deeper understanding of the MAB setting and common MAB approaches;
ILO2. An appreciation of how MABs are applied;
ILO3. Demonstrable ability to implement ML approaches in code; and
ILO4. An ability to pick up recent machine learning publications in the literature, understand their focus,
contributions, and algorithms enough to be able to implement and apply them. (And being able to
ignore other presented details not needed for your task.)


## Implemented algorithms

1. ɛ-greedy MAB
2. UCB MAB
3. LinUCB contextual MAB including evaluation and hyperparameter tuning
4. TreeBootstrap contextual MAB
5. KernelUCB contextual MAB

For evaluation, off-policy evaluation is implemented.


## Version 

Python 3.7.11
numpy 1.19.5
scikit-learn 0.23.1
matplotlib 3.2.2

----

Have fun 
