# **Activation Functions Crash Course**

## **Written By:** Aarish Khan
## **Date:** 4 January 2024

> **Our learning objectives in this Course!**

![learningobjectives](learningobj.png)

1. we will learn the basic activation functions.
2. The types of activation functions in **nn (neural network)**
3. Most widely used activation functions.
4. How to choose activation functions for our analysis.
5. Lastly, we will learn coding activation functions in python.

> **Intro to Activation Functions**

![activationfunctions](image.png)

> **Defintion of Activation Function**

- An activation function is a mathematical function that takes the output of an artificial neuron and implements.
- Sometimes, the activation function can be known as transfer functions.
- If the output range of the activation function is limited, than it may be called a squashing function.

> **Example of Activation Function**

![example](image-1.png)'

> **Types of Activation functions**

![thetypesoffunctions](activationfunctiontype.png)

- there are many types of activation functions such as:
1. Linear activation function
2. Step activation function
3. Sigmoid activation function
4. tanH activation function
5. ReLU activation function
6. Softmax activation function


> **Why Activation functions?**

![whyactivationfunctions](why.png)

- It helps us model non-linearity into our neural networks.

- Without an activation function, each neuron would just pass on its input to the next layer without any modification.
-  This makes the learning process very simple and easy but also quite boring.

![activationfunc](help.png)

- Activation functions are mathematical equations that determine the output of a neural network model.

> **Where exactly Activation functions are used?**

![whereisitused](image-2.png)

> **The purpose of Activation function**

The main purpose of an activation function is to introduce non-linearity in the system so that the neurons become capable of learning from the data present in the input layer. 

The activation function takes the weighted sum of all the inputs to each neuron and then applies a transformation
to produce an output. 

The transformed value is then passed onto the next layer or the output layer.

> **Linear Activation Function**

- It simply returns its input without any change, hence it can be described mathematically as f(x)= x.

![linearactivation](linearactivation.png)

- Linear activation function is also known as no activation or identity function.
- The function does not do anything to the weighted sum of the input, it simply spits out the value as it was given.
- the formula for linear is: f(x) = x.

> **Two major problems in Linear activation Function**

![linearactivationfunction](linearfunction.png)

- It's not possible to use backpropagation as the derivative of the function is a constant and has no relation to the input x.

- The problem with linear activation function is that they do not allow the neurons to express complex relationships between inputs.

> **Non-Linear activation Function**

![nonlinear](Nonlinear.png)
- Non-linear activation functions map the input to an output which is not a straight line.

- They introduce non-linearity into the system, making the learning process more complex and interesting.

- They help model complex relationships between inputs and outputs.

> **Backpropagation can also be refered as:**

* Error Backpropagation\
* Backward Error Propagation\
* Backward Propagation\
* Gradient Descent Backpropagation\
* Backward Pass\
* Error Correction Algorithm\
* Reverse Propagation of Errors\

> **Binary step function**

![binarystep](binary.png)

- Binary Step Function (or Heaviside Function), denoted by H(x), is defined as:
H(x) = 0 if x < 0

- The binary step function is a threshold-based activation function.
- After a certain threshold neuron is activated.

> **Sigmoid\Logistic function**

![sigmoidfunction](Sigmoid.png)

- The sigmoid function is a mathematical function commonly used in machine learning and artificial neural networks.
-  It is specifically utilized in the activation function of neurons to introduce non-linearity to the network. 

> The formula: **F(x) = 1/(1+e^(-x))**

- Sigmoid Function maps any real value into a value between 0 and 1.

- f(x) represents the output of the sigmoid function for a given input x.
- e is the base of the natural logarithm, approximately equal to 2.71828.

> **Advantages of Sigmoid**

![advantages](sigmoid1.png)

- They are widely used because its commonly used for models where we have to predict the probabillity as output.
- It normalizes the output of each neuron.

> **Disadvantages of Sigmoid**

![disadvantages](disadvantges.png)

* Its computanionally expensive
* outputs are not zero centered.
* The gradient during back propagation becomes very small close to 0 or 1.

> **TanH Function (Hyperbolic Tangent)**

![tanh](tanh.png)

- Very similar to sigmoid activation function.
- Even has the same S-shape.
- In tanh, the larger the input(more positive), the closer the output value will be to 1.0, whereas the smaller the input (more negative), the closer the output will be to -1.0.

- But it's symmetric around 0 unlike sigmoid which is asymmetric.

> **Advantages of TanH**

![advantagesoftanh](advantage.png)

- Output values are zero centered.
- Computationally cheaper than sigmoid.

> **ReLU (Rectified Linear unit) Function**

![relu](image-3.png)

> **Formula for ReLU**

- **f(x) = max(0, x)**

- In this function, outputs for the postive inputs can range from 0 to infinity.
- Although, it gives an impression of a linear function. ReLU has a derivative function and allows for back propagation ehile simultaneously making it computaionally efficent.

- For negative input, it just gives 0 as an output.

> **Advantages of ReLU**

- Easy to compute and memory efficient.
- Easy to compute and hence computationally cheap.
- Helps in mitigating the vanishing gradients problem.

![adv](image-4.png)

> **Disadvantages**

![disadvantage](image-5.png) 

- Dead Neurons: If the neuron receives too much negative input during training,

- Then the neuron becomes "dead" i.e., always produces 0 as output

> **Softmax Activation function**

![softmax](image-6.png)

- the output of the sigmoid function was in the range of 0 to 1. Which can be thought of as probabillity.

- The softmax activation function is used when we have a multi class classification task where we want to predict one out of multiple classes.

> **Example of softmax**

![Alt text](image-7.png)

> **Advantages**

![advatange](image-8.png)

- It can be used for multiclass classification.
- It normalizes the outputs for each class between 0 and 1.

> **How to choose an activation function**

* Choosing an activation function often involves empirical testing, and there is no one-size-fits-all solution. Factors such as the nature of the problem, network architecture, and training data can influence the choice. 

* It's common to start with ReLU and its variants and experiment with different options based on your specific scenario. Additionally, using advanced techniques like batch normalization and adaptive learning rate methods can also impact the choice of activation functions.