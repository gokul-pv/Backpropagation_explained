# EVA6_Assignmets_Session4
EVA6 Assignmet for Session 4


# Part 1:
# Training of Feed-Forward Neural Networks

   Learning in feed-forward networks belongs to the realm of supervised learning, in which pairs of input and output values are fed into the network for many cycles, so that the network 'learns' the relationship between the input and output.
   
Let's consider a simple neural network, as shown below.
   <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part1/Images/Feedforward_Network.PNG?raw=true" width =500>
    <br>
    <em style="color: grey">Figure 1.a : A simple feed-forward neural network</em>
  </p> 
  
Where,

<b>Node</b>: The basic unit of computation (represented by a single circle)

<b>w</b>: The weight of a connection

<b>i</b>: Input node (the neural network input)

<b>h</b>: Hidden node (a weighted sum of input layers or previous hidden layers)

<b>a_h</b>: Hidden node activated (the value of the hidden node passed to a predefined function)

<b>o</b>: Outut node (A weighted sum of the last hidden layer)

<b>a_o</b>: Output node activated (the neural network output, the value of an output node passed to a predefined function)

<b>E</b>:difference between the output of the network and target value 

<b>E_total</b>:total error measured by L2 loss


The following are the steps that execute during training phase of above neural network:<br>
### Step 1: Initialization

The first step after designing a neural network is initialization. Initialize all weights W1 through W8 with random values.Also , assume  all bias values as zero for simplicity 

### Step 2: Feed-Forward<br>
In this step, calculate all the values for the hidden layers and output layers and move forward in the network

•	Set the values input nodes and targets

Consider input values as i1=0.05, i2=0.1 and target values as t1=0.01,t2 =0.99 throughout this training

•	Calculate hidden node values
 <p align="center" >
   <a href="https://www.codecogs.com/eqnedit.php?latex=h1=w1*i1&plus;w2*i2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?h1=w1*i1&plus;w2*i2" title="h1=w1*i1+w2*i2" /></a>

  <p align="center" >
   <a href="https://www.codecogs.com/eqnedit.php?latex=h2=w3*i1&plus;w4*i2" target="_blank" ><img src="https://latex.codecogs.com/gif.latex?h2=w3*i1&plus;w4*i2" title="h2=w3*i1+w4*i2" /></a>
      <br>
 </p> 
   
•	Select an activation function.For example, Sigmoid function:

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\sigma&space;(x)=\frac{1}{1&plus;exp^{-x}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\sigma&space;(x)=\frac{1}{1&plus;exp^{-x}}" title="\sigma (x)=\frac{1}{1+exp^{-x}}" /></a>
<br>
</p> 
   
   
•	Calculate hidden node activation values:

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=a\_h1=\sigma(h1)&space;=\frac{1}{1&plus;exp^{-h1}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?a\_h1=\sigma(h1)&space;=\frac{1}{1&plus;exp^{-h1}}" title="a\_h1=\sigma(h1) =\frac{1}{1+exp^{-h1}}" /></a>
<br>
</p> 
<p align="center" >
   <a href="https://www.codecogs.com/eqnedit.php?latex=a\_h2=\sigma(h2)&space;=\frac{1}{1&plus;exp^{-h2}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?a\_h2=\sigma(h2)&space;=\frac{1}{1&plus;exp^{-h2}}" title="a\_h2=\sigma(h2) =\frac{1}{1+exp^{-h2}}" /></a>
<br>
</p>
  
•	Calculate output node values:
<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=o1=w5*a\_h1&plus;w6*a\_h2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?o1=w5*a\_h1&plus;w6*a\_h2" title="o1=w5*a\_h1+w6*a\_h2" /></a> 

<br>
</p>

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=o2=w7*a\_h1&plus;w8*a\_h2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?o2=w7*a\_h1&plus;w8*a\_h2" title="o2=w7*a\_h1+w8*a\_h2" /></a>
<br>
</p>
•	Calculate output node activation values:

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=a\_o1=\sigma(o1)=\frac{1}{1&plus;exp^{-o1}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?a\_o1=\sigma(o1)=\frac{1}{1&plus;exp^{-o1}}" title="a\_o1=\sigma(o1)=\frac{1}{1+exp^{-o1}}" /></a>
<br>
</p>

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=a\_o2=\sigma(o2)=\frac{1}{1&plus;exp^{-o2}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?a\_o2=\sigma(o2)=\frac{1}{1&plus;exp^{-o2}}" title="a\_o2=\sigma(o2)=\frac{1}{1+exp^{-o2}}" /></a>
<br>
</p>

•	Calculate the total error which is sum of  error E1 contributed by output o1 and error E2 contributed by output o2

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=E1=\frac{1}{2}(t1-a\_o1)^{2}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?E1=\frac{1}{2}(t1-a\_o1)^{2}" title="E1=\frac{1}{2}(t1-a\_o1)^{2}" /></a>
<br>
</p>

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=E2=\frac{1}{2}(t2-a\_o2)^{2}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?E2=\frac{1}{2}(t2-a\_o2)^{2}" title="E2=\frac{1}{2}(t2-a\_o2)^{2}" /></a>
<br>
</p>


<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=E\_t=E1&plus;E2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?E\_t=E1&plus;E2" title="E\_t=E1+E2" /></a>
<br>
</p>


After the first pass, the error will be substantial, backpropagation adjusts the weights to reduce the error between the output of the network and the target values 
### Step 3: Backpropagation
The goal of this step is to incrementally adjust the weights for the network to produce values as close as possible to the target values.Backpropagation can adjust the network weights using the stochastic gradient decent optimization method.

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=W_{i}^{k&plus;1}=W_{i}^{k}-\eta&space;\frac{\partial&space;E}{\partial&space;W_{i}^{k}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?W_{i}^{k&plus;1}=W_{i}^{k}-\eta&space;\frac{\partial&space;E}{\partial&space;W_{i}^{k}}" title="W_{i}^{k+1}=W_{i}^{k}-\eta \frac{\partial E}{\partial W_{i}^{k}}" /></a>
<br>
</p>
Where,<br>
k : iteration number<br>
η : learning rate 


<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E}{\partial&space;W_{i}^{k}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E}{\partial&space;W_{i}^{k}}" title="\frac{\partial E}{\partial W_{i}^{k}}" /></a> : derivative of the total error with regards to the weight adjusted


The example below shows the derivation of the update formula (gradient) for the weights in the network.

Derivative of the error e with regards to a weight w5 between a_h1 and o1 using the calculus chain rule can be written as follows :

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;w5}=\frac{\partial&space;(E1&plus;E2)&space;}{\partial&space;w5}=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}*\frac{\partial&space;a\_o1&space;}{\partial&space;o1}*\frac{\partial&space;o1&space;}{\partial&space;w5}&space;---(1)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;w5}=\frac{\partial&space;(E1&plus;E2)&space;}{\partial&space;w5}=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}*\frac{\partial&space;a\_o1&space;}{\partial&space;o1}*\frac{\partial&space;o1&space;}{\partial&space;w5}&space;---(1)" title="\frac{\partial E\_t }{\partial w5}=\frac{\partial (E1+E2) }{\partial w5}=\frac{\partial E1 }{\partial a\_o1}*\frac{\partial a\_o1 }{\partial o1}*\frac{\partial o1 }{\partial w5} ---(1)" /></a>
<br>
</p>


we leave out derivative of E2 with respect to w5 part because the E2 in the network does not depend on weight w5. This is clearly seen in figure 1.a

•	Start from the very first activated output node and take derivatives backward for each node.

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}=\frac{\partial&space;(\frac{1}{2}(t1-a\_o1)^{2})&space;}{\partial&space;a\_o1}=(t1-a\_o1)*(-1)=a\_o1-t1---(2)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E1&space;}{\partial&space;a\_o1}=\frac{\partial&space;(\frac{1}{2}(t1-a\_o1)^{2})&space;}{\partial&space;a\_o1}=(t1-a\_o1)*(-1)=a\_o1-t1---(2)" title="\frac{\partial E1 }{\partial a\_o1}=\frac{\partial (\frac{1}{2}(t1-a\_o1)^{2}) }{\partial a\_o1}=(t1-a\_o1)*(-1)=a\_o1-t1---(2)" /></a>
<br>
</p>

•	From the activated output bounce to the output node:

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;a\_o1&space;}{\partial&space;o1}=\frac{\partial&space;(\sigma&space;(o1))&space;}{\partial&space;o1}=\sigma&space;(o1)(1-\sigma&space;(o1))=a\_o1*(1-a\_o1)---(3)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;a\_o1&space;}{\partial&space;o1}=\frac{\partial&space;(\sigma&space;(o1))&space;}{\partial&space;o1}=\sigma&space;(o1)(1-\sigma&space;(o1))=a\_o1*(1-a\_o1)---(3)" title="\frac{\partial a\_o1 }{\partial o1}=\frac{\partial (\sigma (o1)) }{\partial o1}=\sigma (o1)(1-\sigma (o1))=a\_o1*(1-a\_o1)---(3)" /></a>
<br>
</p>


•	From the output node, bounce to the weight of the connection to hidden layer:

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;o1&space;}{\partial&space;w5}=\frac{\partial&space;(w5*a\_h1&plus;w6*a\_h2)&space;}{\partial&space;w5}=a\_h1---(4)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;o1&space;}{\partial&space;w5}=\frac{\partial&space;(w5*a\_h1&plus;w6*a\_h2)&space;}{\partial&space;w5}=a\_h1---(4)" title="\frac{\partial o1 }{\partial w5}=\frac{\partial (w5*a\_h1+w6*a\_h2) }{\partial w5}=a\_h1---(4)" /></a>
<br>
</p>

•	From equations 1,2,3 and 4 

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;w5}=(a\_o1-t1)*a\_o1*(1-a\_o1)*a\_h1" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;w5}=(a\_o1-t1)*a\_o1*(1-a\_o1)*a\_h1" title="\frac{\partial E\_t }{\partial w5}=(a\_o1-t1)*a\_o1*(1-a\_o1)*a\_h1" /></a>
<br>
</p>


•For other similar weights 

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;w6}=(a\_o1-t1)*a\_o1*(1-a\_o1)*a\_h2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;w6}=(a\_o1-t1)*a\_o1*(1-a\_o1)*a\_h2" title="\frac{\partial E\_t }{\partial w6}=(a\_o1-t1)*a\_o1*(1-a\_o1)*a\_h2" /></a>
<br>
</p>


<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;w7}=(a\_o2-t2)*a\_o2*(1-a\_o2)*a\_h1" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;w7}=(a\_o2-t2)*a\_o2*(1-a\_o2)*a\_h1" title="\frac{\partial E\_t }{\partial w7}=(a\_o2-t2)*a\_o2*(1-a\_o2)*a\_h1" /></a>
<br>
</p>


<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;w8}=(a\_o2-t2)*a\_o2*(1-a\_o2)*a\_h2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;w8}=(a\_o2-t2)*a\_o2*(1-a\_o2)*a\_h2" title="\frac{\partial E\_t }{\partial w8}=(a\_o2-t2)*a\_o2*(1-a\_o2)*a\_h2" /></a>
<br>
</p>


•	Similarly, derivative of the error e with regards to weight between the input and hidden layer W1 using the calculus chain rule can be written as the following 

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w1}=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}*\frac{\partial&space;a\_o1&space;}{\partial&space;o1}*\frac{\partial&space;o1&space;}{\partial&space;a\_h1}*\frac{\partial&space;a\_h1&space;}{\partial&space;h1}*\frac{\partial&space;h1&space;}{\partial&space;w1}&plus;&space;\frac{\partial&space;E2&space;}{\partial&space;a\_o2}*\frac{\partial&space;a\_o2&space;}{\partial&space;o2}*\frac{\partial&space;o2&space;}{\partial&space;a\_h1}*\frac{\partial&space;a\_h1&space;}{\partial&space;h1}*\frac{\partial&space;h1&space;}{\partial&space;w1}--(5)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w1}=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}*\frac{\partial&space;a\_o1&space;}{\partial&space;o1}*\frac{\partial&space;o1&space;}{\partial&space;a\_h1}*\frac{\partial&space;a\_h1&space;}{\partial&space;h1}*\frac{\partial&space;h1&space;}{\partial&space;w1}&plus;&space;\frac{\partial&space;E2&space;}{\partial&space;a\_o2}*\frac{\partial&space;a\_o2&space;}{\partial&space;o2}*\frac{\partial&space;o2&space;}{\partial&space;a\_h1}*\frac{\partial&space;a\_h1&space;}{\partial&space;h1}*\frac{\partial&space;h1&space;}{\partial&space;w1}--(5)" title="\tiny \frac{\partial E\_t }{\partial w1}=\frac{\partial E1 }{\partial a\_o1}*\frac{\partial a\_o1 }{\partial o1}*\frac{\partial o1 }{\partial a\_h1}*\frac{\partial a\_h1 }{\partial h1}*\frac{\partial h1 }{\partial w1}+ \frac{\partial E2 }{\partial a\_o2}*\frac{\partial a\_o2 }{\partial o2}*\frac{\partial o2 }{\partial a\_h1}*\frac{\partial a\_h1 }{\partial h1}*\frac{\partial h1 }{\partial w1}--(5)" /></a>
<br>
</p>


•	 As in the previous case, start with the very first activated output weight in the network and take derivatives backward all the way to the desired weight, and leave out any nodes that do not affect that specific weight

For simplicity equation 5 can be written as,

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;w1}=\frac{\partial&space;E\_t&space;}{\partial&space;a\_h1&space;}*\frac{\partial&space;a\_h1&space;}{\partial&space;h1}*\frac{\partial&space;h1&space;}{\partial&space;w1}---(6)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;w1}=\frac{\partial&space;E\_t&space;}{\partial&space;a\_h1&space;}*\frac{\partial&space;a\_h1&space;}{\partial&space;h1}*\frac{\partial&space;h1&space;}{\partial&space;w1}---(6)" title="\frac{\partial E\_t }{\partial w1}=\frac{\partial E\_t }{\partial a\_h1 }*\frac{\partial a\_h1 }{\partial h1}*\frac{\partial h1 }{\partial w1}---(6)" /></a>
<br>
</p>

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E\_t&space;}{\partial&space;a\_h1}=\frac{\partial&space;E1&space;}{\partial&space;a\_h1}&plus;\frac{\partial&space;E2}{\partial&space;a\_h1}---(7)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E\_t&space;}{\partial&space;a\_h1}=\frac{\partial&space;E1&space;}{\partial&space;a\_h1}&plus;\frac{\partial&space;E2}{\partial&space;a\_h1}---(7)" title="\frac{\partial E\_t }{\partial a\_h1}=\frac{\partial E1 }{\partial a\_h1}+\frac{\partial E2}{\partial a\_h1}---(7)" /></a>
<br>
</p>
From equations 2,3

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E1&space;}{\partial&space;a\_h1}=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}*\frac{\partial&space;a\_o1&space;}{\partial&space;o1}*\frac{\partial&space;o1&space;}{\partial&space;a\_h1}=(a\_o1-t1)*a\_o1*(1-a\_o1)*w5---(8)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E1&space;}{\partial&space;a\_h1}=\frac{\partial&space;E1&space;}{\partial&space;a\_o1}*\frac{\partial&space;a\_o1&space;}{\partial&space;o1}*\frac{\partial&space;o1&space;}{\partial&space;a\_h1}=(a\_o1-t1)*a\_o1*(1-a\_o1)*w5---(8)" title="\frac{\partial E1 }{\partial a\_h1}=\frac{\partial E1 }{\partial a\_o1}*\frac{\partial a\_o1 }{\partial o1}*\frac{\partial o1 }{\partial a\_h1}=(a\_o1-t1)*a\_o1*(1-a\_o1)*w5---(8)" /></a>
<br></p>



<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;E2&space;}{\partial&space;a\_h1}=\frac{\partial&space;E2&space;}{\partial&space;a\_o2}*\frac{\partial&space;a\_o2&space;}{\partial&space;o2}*\frac{\partial&space;o2&space;}{\partial&space;a\_h1}=(a\_o2-t2)*a\_o2*(1-a\_o2)*w7---(9)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;E2&space;}{\partial&space;a\_h1}=\frac{\partial&space;E2&space;}{\partial&space;a\_o2}*\frac{\partial&space;a\_o2&space;}{\partial&space;o2}*\frac{\partial&space;o2&space;}{\partial&space;a\_h1}=(a\_o2-t2)*a\_o2*(1-a\_o2)*w7---(9)" title="\frac{\partial E2 }{\partial a\_h1}=\frac{\partial E2 }{\partial a\_o2}*\frac{\partial a\_o2 }{\partial o2}*\frac{\partial o2 }{\partial a\_h1}=(a\_o2-t2)*a\_o2*(1-a\_o2)*w7---(9)" /></a>
<br>
</p>

Also,

<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;a\_h1&space;}{\partial&space;h1}=a\_h1*(1-a\_h1)---(10)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;a\_h1&space;}{\partial&space;h1}=a\_h1*(1-a\_h1)---(10)" title="\frac{\partial a\_h1 }{\partial h1}=a\_h1*(1-a\_h1)---(10)" /></a>
<br>
</p>



<p align="center" >
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial&space;h1&space;}{\partial&space;w1}=\frac{\partial&space;(&space;w1*i1&plus;w2*i2&space;)&space;}{\partial&space;w1}=i1---(11)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial&space;h1&space;}{\partial&space;w1}=\frac{\partial&space;(&space;w1*i1&plus;w2*i2&space;)&space;}{\partial&space;w1}=i1---(11)" title="\frac{\partial h1 }{\partial w1}=\frac{\partial ( w1*i1+w2*i2 ) }{\partial w1}=i1---(11)" /></a>
<br>
</p>



Finally, the total derivative for the first weight W1 in our network is the sum of the product the individual node derivatives for each specific path. 


From equations 6,7,8,9,10,11
<p>
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w1}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w5&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w7)*a\_h1*(1-a\_h1)*i1---(12)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w1}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w5&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w7)*a\_h1*(1-a\_h1)*i1---(12)" title="\tiny \frac{\partial E\_t }{\partial w1}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w5+(a\_o2-t2)*a\_o2*(1-a\_o2)*w7)*a\_h1*(1-a\_h1)*i1---(12)" /></a>
<br>
</p>


We follow the same procedure for all the weights one-by-one in the network.

<p>
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w2}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w5&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w7)*a\_h1*(1-a\_h1)*i2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w2}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w5&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w7)*a\_h1*(1-a\_h1)*i2" title="\tiny \frac{\partial E\_t }{\partial w2}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w5+(a\_o2-t2)*a\_o2*(1-a\_o2)*w7)*a\_h1*(1-a\_h1)*i2" /></a>
<br>
</p>


<p>
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w3}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w6&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w8)*a\_h2*(1-a\_h2)*i1" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w3}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w6&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w8)*a\_h2*(1-a\_h2)*i1" title="\tiny \frac{\partial E\_t }{\partial w3}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w6+(a\_o2-t2)*a\_o2*(1-a\_o2)*w8)*a\_h2*(1-a\_h2)*i1" /></a>
<br>
</p>


<p>
<a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w4}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w6&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w8)*a\_h2*(1-a\_h2)*i2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{200}&space;\tiny&space;\frac{\partial&space;E\_t&space;}{\partial&space;w4}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w6&plus;(a\_o2-t2)*a\_o2*(1-a\_o2)*w8)*a\_h2*(1-a\_h2)*i2" title="\tiny \frac{\partial E\_t }{\partial w4}=((a\_o1-t1)*a\_o1*(1-a\_o1)*w6+(a\_o2-t2)*a\_o2*(1-a\_o2)*w8)*a\_h2*(1-a\_h2)*i2" /></a>
<br>
</p>


Once we have calculated the derivatives for all weights in the network ,we can simultaneously update all the weights in the net with the gradient decent formula, as shown below.
 <p align="center" style="padding: 10px">
    <a href="https://www.codecogs.com/eqnedit.php?latex=\dpi{150}&space;\begin{bmatrix}&space;W_{1}^{k&plus;1}\\&space;W_{2}^{k&plus;1}\\&space;..\\&space;..\\&space;W_{n}^{k&plus;1}\\&space;\end{bmatrix}=\begin{bmatrix}&space;W_{1}^{k}\\&space;W_{2}^{k}\\&space;..\\&space;..\\&space;W_{n}^{k}\\&space;\end{bmatrix}-\eta&space;\begin{bmatrix}&space;\frac{\partial&space;e}{\partial&space;W_{1}^{k}}\\&space;\frac{\partial&space;e}{\partial&space;W_{2}^{k}}\\&space;..\\&space;..\\&space;\frac{\partial&space;e}{\partial&space;W_{n}^{k}}\\&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dpi{150}&space;\begin{bmatrix}&space;W_{1}^{k&plus;1}\\&space;W_{2}^{k&plus;1}\\&space;..\\&space;..\\&space;W_{n}^{k&plus;1}\\&space;\end{bmatrix}=\begin{bmatrix}&space;W_{1}^{k}\\&space;W_{2}^{k}\\&space;..\\&space;..\\&space;W_{n}^{k}\\&space;\end{bmatrix}-\eta&space;\begin{bmatrix}&space;\frac{\partial&space;e}{\partial&space;W_{1}^{k}}\\&space;\frac{\partial&space;e}{\partial&space;W_{2}^{k}}\\&space;..\\&space;..\\&space;\frac{\partial&space;e}{\partial&space;W_{n}^{k}}\\&space;\end{bmatrix}" title="\begin{bmatrix} W_{1}^{k+1}\\ W_{2}^{k+1}\\ ..\\ ..\\ W_{n}^{k+1}\\ \end{bmatrix}=\begin{bmatrix} W_{1}^{k}\\ W_{2}^{k}\\ ..\\ ..\\ W_{n}^{k}\\ \end{bmatrix}-\eta \begin{bmatrix} \frac{\partial e}{\partial W_{1}^{k}}\\ \frac{\partial e}{\partial W_{2}^{k}}\\ ..\\ ..\\ \frac{\partial e}{\partial W_{n}^{k}}\\ \end{bmatrix}" /></a>
    <br>
  </p> 


Figure 1.b (refer to source excel [here](../main/Part1/BackPropagation.xlsx)) shows complete training process explained above . We can observe total error E_t reducing with each iteration and output values a_o1 and a_o2 coming closer to target values .

   <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part1/Images/Training_Feedforward_Network.png?raw=true" width =2000>
    <br>
    <em style="color: grey">figure 1.b : Training of feed-forward neural network</em>

  </p> 


## Effect of learning rate in training
The learning rate controls how quickly the model is adapted to the problem. Smaller learning rates require more training epochs given the smaller changes made to the weights each update, whereas larger learning rates result in rapid changes and require fewer training epochs. A learning rate that is too large can cause the model to converge too quickly to a suboptimal solution, whereas a learning rate that is too small can cause the process to get stuck.
Following figures shows effect in error graph learning rate changes from [0.1, 0.2, 0.5, 0.8, 1.0, 2.0] 
   <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part1/Images/Error_graph_LR.png?raw=true" width =500>
    <br>
    <em style="color: grey">Figure 1.c : Effect of different learning rates on error </em>
  </p> 

# Part 2:
The part 2 of the assignment is to re write the MNIST digit recognizer such that the following conditions are satisfied. 
   <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part2/Images/Problem_statement.png?raw=true" width =700>
    <br>
    <em style="color: grey">Figure 1.a : Problem Statement</em>
  </p> 
The summary of the model defined is shown below
  <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part2/Images/Model_summary.png?raw=true" width =600>
    <br>
    <em style="color: grey">Figure 1.b : Model Summary</em>
  </p> 

Data Augmentation is very important to regularize your network and increase the size of your training set. Data Augmentation strategy used here is **random affine transformation**. This is done to ensure that the model does not overfit on the training data set and can generalize well on testing data set. In Euclidean geometry, an affine transformation, is a geometric transformation that preserves lines and parallelism (but not necessarily distances and angles). 
<iframe src="//commons.wikimedia.org/wiki/File:Affine_transformations.ogv?embedplayer=yes" width="480" height="480" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

**Training Log**
  <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part2/Images/Training_Log.png?raw=true" width =1000>
    <br>
    <em style="color: grey">Figure 1.c : Training log</em>
  </p> 

**Result**

  

---

  
  

An accurarcy of 99.46 is achieved in 19th epoch with model of 12,674 parameters for the MNIST data
 <p align="center" style="padding: 10px">
    <img alt="Forwarding" src="https://github.com/gokul-pv/EVA6_Assignmets_Session4/blob/main/Part2/Images/Loss_plot.png?raw=true" width =650>
    <br>
    <em style="color: grey">Figure 1.d : Loss and accuracy plots</em>
  </p> 
