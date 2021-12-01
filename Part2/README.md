# Training a MNIST digit recognizer

The aim here is to achieve the following results with MNIST digit recognizer

- 99.4% validation accuracy

- Less than 20k Parameters

- Less than 20 Epochs

- Used Batch Normalization, Dropout, a Fully connected layer after **have used Global Average Pooling.** 

  

## Model

The summary of the model defined is shown below

  <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/Backpropagation_explained/blob/main/Part2/Images/Model_summary.png?raw=true" width =600>
    <br>
    <em style="color: grey">Figure 1.a : Model Summary</em>
  </p> 


Data Augmentation is very important to regularize your network and increase the size of your training set. Data Augmentation strategy used here is **random affine transformation**. This is done to ensure that the model does not overfit on the training data set and can generalize well on testing data set. In Euclidean geometry, an affine transformation, is a geometric transformation that preserves lines and parallelism (but not necessarily distances and angles). 

<iframe src="//commons.wikimedia.org/wiki/File:Affine_transformations.ogv?embedplayer=yes" width="480" height="480" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

## Training Log

  <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/Backpropagation_explained/blob/main/Part2/Images/Training_Log.png?raw=true" width =1000>
    <br>
    <em style="color: grey">Figure 1.b : Training log</em>
  </p> 

## Result 


An accurarcy of 99.46 is achieved in 19th epoch with model of 12,674 parameters for the MNIST data

 <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/Backpropagation_explained/blob/main/Part2/Images/Loss_plot.png?raw=true" width =650>
    <br>
    <em style="color: grey">Figure 1.c : Loss and accuracy plots</em>
  </p> 

