---
layout: post
title:      "Choosing the Right Activation Function for your Artificial Neural Network"
date:       2019-09-07 17:33:13 -0400
permalink:  choosing_the_right_activation_function_for_your_artificial_neural_network
---


**Key Neural Network Components**
* Input Layer – This layer provides the input features or outside information to the network and simply passes it along to the hidden layer
* Hidden Layer – This insulated layer consists of internal neurons where simple or complex computations take place receiving information from the input layer and passing along computed results to the output layer
* Output Layer – This layer spits out information learned by the network as an outputted result


**What is an Activation Function and why do we use them?**

Activation functions, or transfer functions, are integral elements of Artificial Neural Networks that enable the actual learning that a network experiences. These functions simulate synaptic nerve cells in animal brains by creating value thresholds to be exceeded in order for an output value to “activate” and produce a result. When a complex set of data as an input presents itself, a non-linear function does very well to predict and/or classify inputs to output response signals. These non-linear properties that produce outputs are activation functions.

A neural network generally consists of three components: Inputs(X), Weights(W), and Activation Functions f(x)

During the modelling process, we take the sum of products of Inputs(X) and their corresponding Weights(W) and apply an Activation Function f(x) which results in an output from that layer and the input to feed the next layer. A simple model consists of a single input layer, hidden layer, and output layer. However, models can grow in complexity and introduce multiple hidden layers as well as different numbers of neurons in each layer which enables a model to have more capacity to discover complex patterns in an input data set. 

Optimizing models based on accuracy and loss involves tuning of hyperparameters to iteratively discover the best possible combination of weights to achieve a robust end solution. However, it is often the upstream decision of what Activation Function to use that greatly impacts the effectiveness of your neural network.


**What are the most commonly used Activation Functions are there and how can I choose the best one?**

1. Sigmoid or Logistic
2. Softmax
3. Hyperbolic Tangent (Tanh)
4. Rectified Linear Unit (ReLu)

When choosing an activation function, one needs to clearly understand the appropriate applications of each approach, the pros and cons, and in what layers each function can be used in a neural network. There are a number of characteristics to consider, however it is often the simplest function that results in the most efficient model and often the best performing model.


**Sigmoid or Logistic**

f(x) = sigmoid(x) = 1/1 + e^-x

Sigmoid functions are commonly used as binary classification functions in linear regression models as well as activation functions in feed-forward neural networks. Sigmoid curves graphically represent a typical  “S” shape and outputs real-values ranging from 0 to 1. This type of activation function is ideal for models that predict the probability as an output. Sigmoid functions are also differentiable - you can find the slope of a sigmoid curve at any two points - and monotonic - curves are entirely non-decreasing.


**Softmax**

Softmax activation functions are readily used for classification neural networks to calculate the probabilities distribution of each target class over all possible target classes. Similar to sigmoid or logistic functions, softmax function’s range is from 0 to 1 and ideal for multi-classification tasks returning the probabilities for each class including the target. At a high-level, the softmax formula takes an input value(s) and computes the sum of the exponential values. That in return results in a ratio between those two values as the functional output. This is the primary advantage of using the softmax activation function - the output probabilities are divided such that the total output sums to 1. Softmax curves are also monotonic but represent more or an exponential positive curve when graphed.


**Hyperbolic Tangent (Tanh)**

Tanh activation functions are simply scaled sigmoid functions, so the formula will look very similar to what we saw above with sigmoid functions. Graphically, we see another zero-centered “s-curve”, but we see the ranges between the two functions differ. The tanh output values include negative values an extends from -1 to 1. One advantage of this function is that negative inputs will be mapped to strongly negative values and the zero inputs will be mapped near zero on a tanh graph. Another point of differentiation is that the gradient is stronger for tanh than sigmoid (derivatives are steeper). If gradient strength is an important factor in your decision, then choosing tanh over sigmoid may be the better option. However, both sigmoid and tanh functions do have their disadvantages as well, including both suffering from the vanishing gradient problem.


**Rectified Linear Units (ReLU)**

f(x) = relu(x) = max(0, x)

Rectified Linear Units functions are the most commonly used activation functions in the artificial neural networking world. They have many of the same characteristics and benefits of sigmoid functions, but choosing ReLU over sigmoid often results in better overall model performance. This method was developed to directly address a common issue that occurs during neural network modelling, the vanishing gradient problem. This phenomenon occurs when certain weights are adjusted to the point where a node will consistently fail to activate, eliminating that neuron from the overall model. The simplicity of the above formula means that the computational power required to iteratively run the non-linear calculations is far less than sigmoid or tanh functions. The one noteworthy shortcoming is that ReLU functions should only be used as activation functions in the hidden layers of a neural network (not as the input or output layer’s chosen function). Another disadvantage to be aware of is that negative values are transformed to 0 which may impact the efficiency of how your network properly fits and trains on a dataset. The output range is from 0 to infinity and both the function and derivative are monotonic.


**My Experience Choosing a Non-Linear Activation Function**

I realized firsthand the importance of choosing the correct activation function for my hidden and output layers during a recent artificial neural network project in which I attempted to detect malicious botnet attacks on IoT devices by gaining visibility into the network traffic between endpoints.

My initial neural networks all leveraged ReLU activation functions for all three layers (input, hidden, and output). It took a number of iterations with no actual learning occurring (despite my hyperparameter tuning efforts) between epochs before I realized that my chosen activation function was the root cause of my poor models. By changing my output layer activation function to sigmoid, I immediately saw the floodgates open and iterative improvements on classification accuracy and reduction in loss values after each epoch. That “aha” moment after hours of struggling to discover the root cause, inspired me to further investigate different types activation functions, their respective roles in machine learning, and write this blog that you are reading.

By Patrick Routh


Sources
https://www.geeksforgeeks.org/activation-functions-neural-networks/
https://missinglink.ai/guides/neural-network-concepts/7-types-neural-network-activation-functions-right/
https://www.analyticsvidhya.com/blog/2017/10/fundamentals-deep-learning-activation-functions-when-to-use-them/
https://ml-cheatsheet.readthedocs.io/en/latest/activation_functions.html#softmax
https://towardsdatascience.com/activation-functions-and-its-types-which-is-better-a9a5310cc8f
https://medium.com/the-theory-of-everything/understanding-activation-functions-in-neural-networks-9491262884e0
https://dataaspirant.com/2017/03/07/difference-between-softmax-function-and-sigmoid-function/
https://github.com/Kulbear/deep-learning-nano-foundation/wiki/ReLU-and-Softmax-Activation-Functions




