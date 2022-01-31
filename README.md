# Neural Network Charity Analysis
### Creating and Optimizing a Neural Network to Predict Effectiveness of Donations

For this analysis, I was tasked with creating a binary-classifying neural network that will predict whether charity ventures will be successful so that our company can allocate our funds more wisely.

## Results

### Initial Model

For the initial model I considered the effects of the following variables on whether or not a charity would be successful: application type, affiliation, classification, use case, organization type, status, income amount, special considerations and ask amount. I then found the number of unique values under each variable. Two categorical variables stood out: classification and application type. 

![unique values](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/Screen%20Shot%202022-01-30%20at%2012.05.17%20PM.png?raw=true)

In order to prevent confounding the model with excessive categories, I placed all values in the application type column with a count of less than 500 in an ‘other’ bin. I did the same for the classification column for values with a count of less than 1500.

![app type value counts](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/app_type_value_counts.png?raw=true)

![class value counts](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/class_value_counts.png?raw=true)

After creating my target, my variables, scaling the data and splitting the data into training and testing sets, I then created my neural network. I used two hidden layers -- one with eight nodes and one with five. I used “relu” for the activation function on both hidden layers and “sigmoid” for the output layer.

![first nn model](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/first_nn_model.png?raw=true)

The model yielded an accuracy of .53 and a loss of .69. This clearly was inadequate for Alphabet Soup’s purposes. I would need to create a better model.

![accuracy first model](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/accuracy_first_model.png?raw=true)

### (Attempted) Optimization

In order to improve the accuracy of my model, I used the same variables as the first model except I created different bins for the application type and classification variables when I noticed that for each variable there was a value that occurred more than all other values combined. I then put all other values in the ‘other’ bin for both variables.

![optimized type bins](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/optimized_app_type_value_counts.png?raw=true)

![optimized classification bins](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/optimized_class_value_counts.png?raw=true)

I then added another hidden layer and increased the number of neurons in the other layers. I also experimented with different activation functions. I tried both ‘tanh’ and ‘sigmoid’ activation functions, but they yielded the same results (below)

![accuracy optimized nn model](https://github.com/LiShanDa2021/neural_network_charity_analysis/blob/main/accuracy_optimized_model.png?raw=true)

As you can see, my adjustments failed to improve the model.

## Summary
Since neither of my models proved very accurate, I will need to go back to the drawing board and maybe watch a few videos on machine learning to see what makes it tick. This is my last assignment and I figure I can afford to lose a few points on it. Any feedback or suggestions on how to build a better model would be appreciated and implemented.
