# FB_follower

Facebook Followers:
Social media platforms like Facebook provide a myriad of data points about companies such as customer traction, foot traffic, and brand awareness among others.
 
By analyzing Facebook ‘check in’ data, Investment Bank Cowen used this data to track foot traffic to Chipotle starting in 2017, and thus predict falls in Chipotle stock performance as well. This metric of analyzing footfall became a staple for fast food restaurant research analysts as discussed by Yahoo Finance article.


Facebook is a great innovation that helps people to connect around the world. Besides linking individual people's social network, it also has great value for businesses. It has been seen as one of the best ways to generate word-of-mouth for the company, and each check-in will typically be seen by nearly 200 friends. If we think about which place could get the highest number of check-ins each year, "Disney" might be the answer nobody will deny. However, as a top favorite place,  will this function helps a lot for their continues performance? Will people talk about it on social media more frequently will boost the total number of visitors shortly? If there is a trend that affects the check-in rate, whether similar patterns can be captured by each business that has some common characteristics? 
By analyzing the check-in, talking_about frequency of the famous attractions (e.g., amusement park) from the Facebook dataset, I have examined several possible hypotheses as mentioned above. Are popular attractions benefit from social media? Which attraction has better social media ad strategy that helps the revenue? Will potential strategies can be easily applied to different business? The Jupyter notebook that includes all my preliminary analysis can be found here:
https://github.com/htian005/FB_follower/blob/master/Exercises-Facebook.ipynb

I have examined the correlations between different variables (e.g.,# check-ins and # talking_about_count) for the top 7 check_in places. The top 3 locations are all Disney places. However, the trends are relatively flat, which means people talking about Disney on Facebook didn't really affect the # check-ins. But, the follow-up question is, whether this happens to all the places. Clearly, more significant correlations can be found in the lower rank place, such as Busch Gardens, Sea World, and Knotts Berry Farm.
Further regression analysis is conducted using Busch Gardens data (1st plot). When the correlation is calculated by using the total # check-ins with total # talking_about_count in the same period, there is no regression model can be built to fit in the data. So I consider using the rolling correlation to move the observation window. It shows a significant relationship when the observation window is set to 2. So the further experiments are conducted by shifting the #talking_about_count from 1 to 3 month. With selecting one or more variables to build the linear regression model, we can check the R-square and adjust R-square to identify the best variable or variables that can fit into the model to predict the #checkins. For Busch Gardens, the final OLS model is built using the # talking_about_count 2 months ago. We can conclude that the increase in talking about BuschGardens on Facebook will affect the #checkins two months later. This conclusion potentially can help the ad marketing personnel to decide when will be the best time and where Facebook is an excellent place to advertise their promotions.

Based on all those experimental results, I want to build a framework that could automatically create the best model for specific business and generate some insights of the data as the advice for decision-making person.
