# Jumbo-livestreaming
It's a industry cooperation with Jumbo livestreaming. Our group had three people, which I was responsible for GRU model training and forecasting. 

Additionally, I applied SHAP to produce a plot related to promotion terms, which showed the contribution made by each term. 

We focused our analyzing goal on clothes category, it led to a deeper and more comprehensive understanding in an aspect.


## Main Contribution 
**1. Effects between promotion terms with different genders:** We are curious about which promotion terms will encourage male and female to purchase an item. Therefore, we utilized CKIP, which is a hyphenation tool, to retrieve the targeted promotion terms according to the dictionary we created. We set the target to 1 if there are any promotion terms existing in product names, else 0. With linear regression, we checked the level of significance between whether using promotion terms with different genders.

**2. Effects between Assertive terms with different genders:** Then, after reading The power of talk: Exploring the effects of streamers’ linguistic styles on sales performance in B2B livestreaming commerce, we categorized our promotion terms to whether it is described with Assertive style. And again, we used linear regression to check the level of significance between whether using assertive terms with different genders.

**3. Effects between different price range with different promotion terms for each gender:** We seperate the price range by calculating mean of price columns, and set 1(= high price), 0(= low price) as  the target variable. We used LightGBM to help us to make classification on different price range according to various promotion terms and the amount of each product. We split the dataset by 70% for training , 30% for testing. And the performance is 72.71% on accuracy, then we applied TreeExplainer in SHAP to elucidate the impact of different price range corresponding to different promotion terms, there is a feature importance plot, too. We tried to let the model deal with multi categories problem better, because it will lead to a nicer plot compared with binary problem. The performance is merely 30 ~ 40% on accuracy. I thought the model needs more features to help itself to predict more precisely, under the limit of time, this is the best performance we can achieve now.
