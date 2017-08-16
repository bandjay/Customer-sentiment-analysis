# Customer-sentiment-analysis
## Project at Infosys (no code due to restrictions)
### Goal of this project is to build a classification model to categorize customers into "Happy" or "Unhappy" categories.
* Data was queried using SQL and complied data set for the analysis with email text, survey feedback and target sentiment variable

* Performed Feature engineering,data cleaning on email text,survey feedback in two steps
	i) For the email text used text mining methods such as regular expressions, tf-idf to convert raw text to numeric vectors and then used PCA (Principal Component Analysis) to obtain dense representation of features.
	ii) For the survey feedback,it represents scores to a set of questions in the range of 0-7  and this data has high proportion of missing values ,to handle missing data used NNMF (Non negative matrix factorization) to fill the missing scores.
and later both these feature sets were combined with target variable to obtain training data set.
 
* Modeled logistic regression for the binary classification of sentiment and to deal with over fitting techniques such as cross validation and regularization(LASSO,Ridge) were considered, used Accuracy as model evaluation metric.

* Interpreted variable selection using odds ratio and LASSO model to find out influential variables and it turns out that some of the survey feedback variables are important in classifying sentiment where as the dense features from text could not be interpreted as they are the principal components.

* Obtained the best model that has better accuracy and predicted sentiment on unseen customer data.
​