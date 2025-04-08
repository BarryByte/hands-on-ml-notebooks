# Exercises from chapter 1 - The Machine learning landscape.

1. How would you define Machine Learning?

- Rather than being explicitly programmed with rules, machine learning builds systems that improve their performance based on a defined metric or performance measure.
- It allows machines to analyze data, identify patterns, and make decisions or predictions based on that analysis.

2. Can you name four types of problems where it shines ?

- Assisting humans in dicovering insights like hidden patterns.
- predictions, Image recognition ,Natural language processing
- Build systems that adapt to fluctuating environments
- problems for which we have no algorithmic solution


3. What is a labelled training set ?

- labelled training dataset have n number of features and one target or label for each instance.
- used in supervised learning
- if the training dataset does not contain target feature it comes under unsupervised learning

4. What are the two most common supervised tasks ?

- prediction of sales of a product over n number of stores
- spam detection
- house price prediction
- regression and classification

5. Can you name four common unsupervised tasks ?

- Customer segmentation - dividing customers into distinct groups based on similar behaviors or characteristics
- Market Basket Analysis - identifying associations between items (eg : products frequently bought together)
- PCA
- image segmentation - partitioning an image into meaningful regions for analysis
- association rule learning : technique used to find relation among variables in large datasets , e.g., Recommending products based on past purchases

5. What type of Machine Learning algorithm would you use to allow a robot to
walk in various unknown terrains?
- ~~Live image processing - image segmentation~~
- reinforcement learning - this approach enables a robot to learn optimal actions through trail and error by receiving feedback ( rewards or penalties ) from the enviornment.
- also integrating real-time image processing helps the robot interpret its surroundings for effective navigation.

6. What type of algorithm would you use to segment your customers into multiple
groups?

- unsupervised algorithm - customer segmentation - cluster of similar customer
- however if you know what groups you would like to have then you can feed many examples of each group to a classification algorithm - supervised learning.


7. Would you frame the problem of spam detection as a supervised learning prob‐
lem or an unsupervised learning problem?

- supervised learning

8. What is online learning system ?

- they can learn incrementally as opposed to batch learning system
- this helps the system to adapt rapidly to both changing data and autonomous systems

9. What is out-of-core learning ?

- Out-of-core algorithms can handle vast quantities of data that cannot fit in a computer’s main memory. An out-of-core learning algorithm chops the data into mini-batches and uses online learning techniques to learn from these mini-batches


10. What type of learning algorithm relies on a similarity measure to make predictions ?

- instance based learning system learns the training data by heart
- when given a new instance it uses similarity measure (like nearest neighbors) to find the most similar learned instance and uses them to make prediction
- also knows as lazy learning


11. What is the difference between a model parameter and a learning algorithm’s hyper parameter ?

- model’s parameters - these are the internal variables of the model that are learned from the training data.
- hyper-parameters - these are external configurations ( like learning rate, number of clusters ) set by the practitioner to guide the training process and can be turned to improve performance


12. What do model-based learning algorithms search for? What is the most common
strategy they use to succeed? How do they make predictions?

- search objective - they search for a function or model that best captures the relationship between input features and outputs.
- use optimization techniques to minimize a loss function (like mse or rmse )
- once trained these models predict outcomes by applying the learned function to new input data.


13. Can you name four of the main challenges in Machine Learning?
- Data cleaning - most of the time while building a ML project is do clean the irrelevant features and making new features
- complexity and evolving nature of ML process.
- poor quality of data
- overfitting and underfitting models.

14. If your model performs great on the training data but generalizes poorly to new instances, what is happening? Can you name three possible solutions?

- good on training data and bad on new instances, problem of overfitting
- probable solutions are :
  - regularization
  - gather more data
  - reduce noise in training data
  - select fewer parameters (if every essence of the training data is captured it will learn every possible pattern which it should not learn)


### Key Differences between train-validate-test sets :

#### Purpose:
> Training Set: To train the model and adjust its parameters.
>
> Validation Set: To tune hyperparameters and prevent overfitting.
>
> Test Set: To evaluate the final model's performance on unseen data.

#### Usage:
>Training Set: Used during the training phase.
>
>Validation Set: Used during the model selection phase.
>
>Test Set: Used after the model is fully trained and tuned.

#### Impact on Model:
> Training Set: Directly influences the model's parameters.
>
> Validation Set: Influences the choice of hyperparameters but does not directly affect the model's parameters.
>
>Test Set: Provides an unbiased evaluation of the model's performance.

15. What can go wrong if you tune hyperparameters using the test set?

- the primary role of test set is for checking unbaised performance of our model, tuning their hyperparameter would essentially make them optimized specifically for the test setand later when the model is tested on unseen data it would boom!

