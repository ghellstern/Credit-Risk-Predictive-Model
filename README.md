# Credit-Risk-Predictive-Model
Credit risk predictive model using stacking.  AUROC is used to evaluate performance.

This is based on the Kaggle competition "Give Me Some Credit".  The training and test data can be found at 
https://www.kaggle.com/c/GiveMeSomeCredit/data

The model I uploaded uses a stacking approach where the first layer contains multiple different classifiers, including a multilayer perceptron and trees.  The final predictions are done by a layer of XGBoost.  Features from the data were a bit thin initially so it was necessary to add a good amount more to increase prediction accuracy.  

The model gives an AUROC of 0.867108.  The winning team in the competition had an AUROC of 0.869558.  I ended up not doing too
bad for a weekend project, top 12% score among nearly 1000 teams.

If instead of the first layer predictions being the only features to the meta model, I use them as extra features to the ones that already exist, I can boost the score to 0.867119, which brings me up a couple spots in the leaderboard.

Note: If you want to run this model, you may have to do something different than me when it comes to using xgboost.  That is, simply 
running what is uploaded may not work because of how xgboost is installed.
