# Deep Learning Ideas
An overview of deep learning concepts jotted down before they escape my evanescent memory.

### Layer normalization
Normalizing the activation values reduces training time of deep learning models. Batch normalization is dependent on the size of the batch and it is not obvious how to use it for recurrent networks like RNNs. Layer normalization computes mean and variance from all summed inputs to the neurons in a layer on a single training case. Each layer has its own bias as well as gain applied after normalization but before non linearity. Straighforward to apply to RNN by computing statistics at each step.


### Batch normalization
During training of a DNN, the distribution of each layer's inputs changes during training, as the parameters of the previous layers change. This slows down the training by requiring lower learning rates and careful parameter initialization, and makes it hard to train models with saturating nonlinearities. This paper makes normalization a part of the model architecture performing the normalization for each training mini-batch. It allows use of much higher learning rates and be less careful about initialization. It also acts as a regularizer, in some cases eliminating the need for Dropout. Batch Normalization achieves the same accuracy with 14 times fewer training steps, and beats the original model by a significant margin.
