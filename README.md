# Tanzanian-Well-Data
## Objective 
* Using machine learning models and data  from Taarifa and the Tanzanian Ministry of Water, predict which pumps are functional, which need some repairs, and which don't work at all.
* Perform feature analysis to look for breakdown of well development  and look for human error in well functionality 
## Data Analysis

### Distributions of wells
![Imgur](https://i.imgur.com/YY4syw2.png)

There are higher populations around the edges of the country along with a high density of non-functional wells. Central Tanzania has the most working wells and with lower average populations. When it come to well that need to be repaired, they tend to be more sporadically located.A trend can begun to be seen with location of well and the population of the surrounding area on the status group of the well

### Funder
![Imgur](https://i.imgur.com/cKjcfK2.png)

After depicting the top three funders of wells in Tanzania, it can clearly bee seen that Danida is the only group to fund more functional than non-functional well. When factoring in well that need repair into the functioning wells category, only then do we see the Tanzanian Government and Hesawa just barley produce more functioning wells than not. This could be an indication the organizations, especially the Government, are choosing quantity over quality. 

### Installer
![Imgur](https://i.imgur.com/qDREd57.png)

Of the top three installers of wells used, DWE is the only company to produce more than 50% of their wells as functional, indicating that they are the most reliable one. The government, who is also a funder, again is just barely producing equivalent amounts of functional and non-functional well when factoring in the wells that need repair.  RWE on the other hand just fails completely in terms of well success rate. With limited data on the matter, on could assume the Government is raising money to fund wells and paying itself to build a portion of those. It leads to a gray area of corruption that could be a cause as to why the government as an installer is underperforming

### Management 
![Imgur](https://i.imgur.com/pWKXO8K.png)

This chart of popular management groups is the first to indicate more functional wells are being observed than not for each individual group. With Funder and Installer organization struggle to produce functioning wells, starts to show management groups as the key part in what will define success. As with the other charts there is a clear leader for who is the most popular individual to contract work out to. There appears to be no indication as to why one specific individual it more prioritized than another.

## Modeling


## Initial Model - Decision Tree
![Imgur](https://i.imgur.com/XIAyVOD.png)

Models Sampled:
1. Logistic Regression 
1. Decision Tree
1. XGBoost
1. K-Nearest Neigbor 

The first model performance struggled with categorizing “functional needs repair”. In terms of “Functional” and “non-functional” they had good performance for an initial model. With an overall of 74% accuracy and a macro average of 0.62 the mode performed as expected with it not being to exceptional 

## Final Model – Grid Search Random forest
![Imgur](https://i.imgur.com/Je8ro1h.png)

Iterations:
1. Grid Search 
1. Random Forest
1. Oversample
1. Undersample

After going through several iterations of decision drees, an optimized grid search random showed to have the highest increase performance. F1-score for “functional need repair” had a minor increase but still had poor performance. This is likely due to the lack of data point within the group. The new mode increased its accuracy by 5% to 79% and increased macro f1-score 0.03 for a final of 0.65

## Recommendations 
1. Raise more money per well
1. Reallocate how the money is being spend on the well
1. Focus on quality over quantity 

## Future Work
1. Analyze the amount of money spent per well
1. Find the number of daily uses per well and its status
1.Look at the list of materials used for each status group of wells


