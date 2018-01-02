# Oscar Nominations Predictor:

According to the BBC and Time magazine the estimated total amount spent on campaigning for the Oscars range between $100 million to $500 million each year. Each studio spends close to $10 million on advertising, consultants, gifts and select screening. All to influence members of the Academy of Motion Pictures Arts and Science. But how much does this help? Each year there are surprise Oscar nominations and winners. This project aims to explore various features of a film to determine whether or not a film will be nominated. An effective model for the Oscar might explain why films are nominated, why films are not and why anomalies occur. It could also be effective in determining which films studios should campaign.

What genres of films get nominated? Do certain directors, writers and cast get nominated more often? Do films that deal with social and/or political issues get nominated? Does it rely on the month the film is released? How long it ran in the theatres? Does box office performance play a role? How well it was reviewed by critics? Other awards? Why do certain films with Oscar buzz under perform? Why do some films with little Oscar buzz perform well? 

Why do Drama films perform better than Action films? These features seem to play a role for a film to receive a nomination. These are important question film studios might ask when deciding to campaign for a film. As a data science these are questions about the relationship between the feature with the target variables.What features are indicators. What features positively correlate. What features negatively correlate. Modelling these features could explain why certain anomalies occur.


## Dataset

Data was scrapped from following three sources
1. Box Office Mojo
2. Kaggle
3. Wikipedia

Following existing projects from github were used to  get scripts to scrap these data sources
1. https://github.com/scruwys/and-the-award-goes-to
2. https://github.com/dianalam/movie-predictor

This raw data had a lot of missing values and all the features were not in one dataset. Hence the data from the sources mentioned above was cleaned, transformed, aggregated and merged to get the final complete and cleaned data. All the data cleaning ,merging and transformation code can be found in this [data cleaning](Cleaning_the_Data.ipynb) notebook.


### Learning Algorithms Used

Since the target variable is binary ( yes/No), a Decision Tree and Random Forest was used to model film nomination for the Academy Awards. Following features were used to predict the target variable:
* critic review score
* audience review score
* directors previous nominations
* directors previous awards (number of awards)
* Films previous awards (Globes, Bafta)
* Genre
* MPAA Rating
* Season (Spring, Summer, Holiday, Winter)

The correlation of the feature listed above with the target variable was determined in the preliminary statistics. The results of the initial exploratory analysis are shown in initial_analysis.pdf file. Both the Decision Tree and Random Forest will be able to give feature importance. Parameters for both models will need to optimized based on an average AUC on the ROC curve. The models will be evaluated using an ROC curve and AUC scores.

All the model based work right from building and evaluation is listed in this [project model](project_model.ipynb) notebook.


## Future Ideas
* Time Series analysis to explore some interesting trends
* Which genres were popular during a particular decade and predicting the same.
* Buzz analysis - does a movie about the trending topics makes it more likely to get nominated? We can do sentimental analysis to decide the fate of a film in Oscars.

## Contributors
* Khushnaseeb Ali
* Alexander Dudley Rabinowitz
