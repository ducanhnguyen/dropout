# dropout
Dropout is one of the most popular regularization techniques to avoid overfitting. This is my implementation of dropout based on the original paper.

Paper: http://jmlr.org/papers/volume15/srivastava14a.old/srivastava14a.pdf

Data: https://www.kaggle.com/c/digit-recognizer

### Idea

The authors try to reduce the capacity of the neural network during training. In order to do that, the probability of keeping a node is proposed. In other words, dropout introduces a significant amount of noise in the gradients compared to standard stochastic gradient descent.

When applying dropout regularization, every layer (include input layer, not include output layer) has a probability of keeping node. According the paper, the keeping probability of the input layer should be 0.8. The other layers should be set to 0.5.

<img src="https://github.com/ducanhnguyen/dropout/blob/master/img/dropout.png" width="650">

The term "dropout" refers to dropping out units (both hidden and visible) in a neural network. We do not use dropout when testing.

<img src="https://github.com/ducanhnguyen/dropout/blob/master/img/pkeep.png" width="650">

### Environment
PyCharm 2018.3.4, jre 8, mac osx

### Experiments

<img src="https://github.com/ducanhnguyen/dropout/blob/master/img/accuracy.png" width="550">

<img src="https://github.com/ducanhnguyen/dropout/blob/master/img/error.png" width="550">
