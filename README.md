# MachineLearning--Apriori--Association
Applying Apriori on a Real world dataset of customers purchasing groceries.


Association Rule Learning :

Apriori:-

How the Apriori Algorithm work.

It has three parts to it. It has the support, the confidence and the lift.


Let’s take Movie Recommendation example.

-Support :  
	       
	       Movie Recommendation:     Support(M) = (#user watchlists containing M) /      #user watchlists

-Confidence :   

	        Movie Recommendation:   confidence(M1   M2) = #user watchlists containing M1 and M2 / #user watchlists containing M1 

-Lift : 
	Movie Recommendation: 
Lift(M1  M2) = confidence(M1  M2) / support(M2)



Apriori Algorithm run through:

First step, set a minimum support and confidence, then, take all the subsets in transactions having higher support than minimum support, then, take all the rules of these subsets having higher confidence than minimum confidence. And finally, sort the rules by decreasing lift.

Now that I have put in words what I learned about Apriori. Most large companies like Youtube or Netflix do not just use Apriori! Apriori is just a very basic approach for things like recommendations. I believe larger companies use lots of combinations of algorithms, and they probably even do specific engineered algorithms depending on the case.


Unfortunately, after some research it turns out that sklearn library does not have classes on Apriori, so I had to use a library that download it from the internet called Apyori.

In this huge real-world data set, each row represents a customer and the columns of that row represents the groceries purchased by that customer. Unlike the usual data sets that I worked with, this dataset’s first row does not have the names of the columns, therefore I had to adjust my data preprocessing accordingly to make it work. I also reorganized the data from the dataset and put them in a list as string values. And then the algorithm follows. Please note that I had to play around with the parameters of the apriori function in order to achieve good rules.

As we can see from the results displayed in the table at the very bottom that people who purchase fromage blanc are very likely to purchase honey with a lift of 5.16 (which is quite good). Therefore, a business decision such as making offers like buy 1 fromage blanc and get a free honey could be beneficial for example.



