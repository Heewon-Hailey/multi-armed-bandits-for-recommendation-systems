# Multi Armed Bandits for recommendation systems


## About the project

This work is to implement several MAB algorithms including basic, contextual, and more advanced multi armed bandits from papers [1-4].


## Background

Multi-armed bandits (MABs) are a framework for sequential decision making under uncertainty. MABs solve problems in online advertising, information retrieval, and media recommendation. For instance, Yahoo! News decides what news items to recommend to users based on article content, user profile, and the historical engagement of the user with articles. Given decision making in this setting is sequential (what do we show next?) and feedback is only available for articles shown. MABs such as ɛ-Greedy and UCB show a perfect formulation. However, incorporating some element of user-article state requires contextual bandits: articles are arms; context per round incorporates information about both user and article (arm); and {0,1} -valued rewards represent clicks. Therefore the per round cumulative reward represents click-through-rate, which can maximise to drive user engagement and advertising revenue. 


## Datasets

The dataset `dataset.txt` contains 10,000 instances corrresponding to distinct site visits by users-events in the language of this part. Each instance comprises 102 space-delimited columns of integers:
 - Column 1: The arm played by a uniformly-random policy out of 10 arms (news articles)
 - Column 2: The reward received from the arm played|1 if the user clicked 0 otherwise; and
 - Columns 3-102: The 100-dim flattened context; 10 features per arm (incorporating the content of the article and its match with the visiting user), first the features for arm 1, then arm 2, etc. up to arm 10.


## Implemented algorithms

1. ɛ-greedy MAB
2. UCB MAB
3. LinUCB contextual MAB including evaluation and hyperparameter tuning [1]
4. TreeBootstrap contextual MAB [3]
5. KernelUCB contextual MAB [4]

For evaluation, off-policy evaluation [1-2] is implemented.


## Version 

Python 3.7.11<br>
numpy 1.19.5<br>
scikit-learn 0.23.1<br>
matplotlib 3.2.2<br>


## References 

[1] Lihong Li, Wei Chu, John Langford, Robert E. Schapire, ‘A Contextual-Bandit Approach to Personalized News Article Recommendation’, in Proceedings of the Nineteenth International Conference on World Wide Web (WWW’2010), Raleigh, NC, USA, 2010. 
https://arxiv.org/pdf/1003.0146.pdf

[2] Lihong Li, Wei Chu, John Langford, and Xuanhui Wang. ‘Unbiased offline evaluation of contextualbandit-based news article recommendation algorithms.’ In Proceedings of the Fourth ACM International Conference on Web Search and Data Mining (WSDM’2011), pp. 297-306. ACM, 2011.
https://arxiv.org/pdf/1003.5956.pdf

[3] Adam N. Elmachtoub, Ryan McNellis, Sechan Oh and Marek Petrik, ‘A Practical Method for Solving Contextual Bandit Problems Using Decision Trees’, in Proceedings of the Thirty-Third Conference on Uncertainty in Artificial Intelligence (UAI’2017), Sydney, Australia, 2017.
http://auai.org/uai2017/proceedings/papers/171.pdf

[4] Michal Valko, Nathan Korda, R´emi Munos, Ilias Flaounas, and Nello Cristianini, ‘Finite-time analysis of kernelised contextual bandits.’ In Proceedings of the Twenty-Ninth Conference on Uncertainty in Artificial Intelligence (UAI’13), pp. 654-663. AUAI Press, 2013.
http://auai.org/uai2013/prints/papers/161.pdf

----

Have fun 
