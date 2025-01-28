<style>

#left {
    left:-8.33%;
  text-align: left;
  float: left;
  width:50%;
  z-index:-10;
}

#right {
  left:31.25%;
  top: 75px;
  float: right;
  text-align: right;
  z-index:-10;
  width:50%;
}
#fs-size {
  font-size:2px;
}

</style>

# Sensitivity Analysis (SA)


## Local vs. Global Sensitivity Analysis

### Local Sensitivity Analysis

+ Considers the effect of variation of parameters locally in close vicinity of the point in consideration
+ Derivative based (numerically or analytically) sensitivity coefficients
+ Usually follows one-at-a-time (OAT) technique that analyses the impact of one parameter at a time, keeping other parameters fixed

### Global Sensitivity Analysis

+ Considers the effect of variation of parameters globally in whole domain under consideration
+ Generally requires Monte Carlo sampling of points within the domain


## Morris Sensitivity Analysis

<div id="left">

  - One-at-a-time (OAT) method
  - Based on method of trajectories
  - Gives qualitative information about importance of input parameters
  - Global Sensitivity Analysis method
  - Computations of Elementary Effects (EEs)
</div>

<div id="right">
  <img
    src="assets/morris_trajectory.svg"
    width="120%"
    height="150%"
  />
</div>

+ Elementary Effects:
$
EE_i(x) = \frac{[y(x_1, ..., x_{i-1}, x_i + \Delta, x_{i+1}, ..., x_k) - y(x)]}{\Delta}
$

where $\Delta$ is predetermined multiple of $1/(p-1)$ and point $x = (x_1, x_2,..., x_d) \in H^d$

<!-- .element: class="fragment fade-in" data-fregment-index="1" -->


## Morris Global Sensitivity Analysis

<img
  
/>



# Machine Learning (ML)


## General ML Process

<div class="r-stack">
  <img
    class="fragment current-visible"
    data-fregment-index="1"
    src="assets/ml-process/ml-process-1.svg"
  />
  <img
    class="fragment current-visible"
    data-fregment-index="2"
    src="assets/ml-process/ml-process-2.svg"
  />
  <img
    class="fragment current-visible"
    data-fregment-index="3"
    src="assets/ml-process/ml-process-3.svg"
  />
  <img
    class="fragment current-visible"
    data-fregment-index="4"
    src="assets/ml-process/ml-process-4.svg"
  />
<img
    class="fragment current-visible"
    data-fregment-index="5"
    src="assets/ml-process/ml-process-5.svg"
  />
<img
    class="fragment current-visible"
    data-fregment-index="6"
    src="assets/ml-process/ml-process-6.svg"
  />
</div>


## ML Classification

<div class="r-stack">
  <img
    class="fragment current-visible"
    data-fragment-index="1"
    src="assets/ml-class/ml-class-1.svg"
  />
  <img
    class="fragment current-visible"
    data-fragment-index="2"
    src="assets/ml-class/ml-class-2.svg"
  />
  
</div>


## Multi layer Perceptron (MLP)

<div class="r-stack">
  <img
    class="fragment current-visible"
    data-fragment-index="1"
    src="assets/nn-mlp/nn-1.svg"
  />
  <img
    class="fragment current-visible"
    data-fragment-index="2"
    src="assets/nn-mlp/nn-2.svg"
  />
  <img
    class="fragment current-visible"
    data-fragment-index="3"
    src="assets/nn-mlp/nn-3.svg"
  />
  <img
    class="fragment current-visible"
    data-fragment-index="4"
    src="assets/nn-mlp/nn-4.svg"
  />
</div>


## Perceptron / Neuron

<div id="right">
  <div class="r-stack">
   <img
      class="fragment fade-in-then-out"
      data-fragment-index="1"
      src="assets/nn-mlp/perceptron-1.svg"
   />
   <img
      class="fragment fade-in"
      data-fragment-index="2"
      src="assets/nn-mlp/perceptron-2.svg"
    />
  </div>
  <div class="r-stack">
    <img
      class="fragment fade-in-then-out"
      data-fragment-index="3"
      src="assets/af/ActivationFunctions.svg"
    />
    <img
      class="fragment fade-in-then-out"
      data-fragment-index="4"
      src="assets/af/af-step.svg"
    />
    <img
      class="fragment fade-in-then-out"
      data-fragment-index="5"
      src="assets/af/af-tanh.svg"
    />
    <img
      class="fragment fade-in-then-out"
      data-fragment-index="6"
      src="assets/af/af-relu.svg"
    />
    <img
      class="fragment fade-in"
      data-fragment-index="7"
      src="assets/af/af-sigmoid.svg"
    />
  </div>

  - credit: Wikimedia Commons 
  <!-- .element: class="fragment" data-fragment-index="3"-->
</div>

<div id="left">
  
  - A perceptron takes in few inputs, with corresponding weights.
  <!-- .element: class="fragment" data-fragment-index="1"-->

  - It computes the outputs as: 

    $\hat{y_i} = \sum_{i=1}^d x_i * w_i + b_i$

    where $x$ is input, $w$ is weight, and $b$ is the bias.
  <!-- .element: class="fragment" data-fragment-index="2"-->

  - Activation Functions 
  <!-- .element: class="fragment" data-fragment-index="3"-->
    + It adds non-linearity to the model.
     <!-- .element: class="fragment" data-fragment-index="3"-->

    + Different kinds of activation functions:
      1. Binary step function 
      <!-- .element: class="fragment" data-fragment-index="4"-->
      2. Tanh function
      <!-- .element: class="fragment" data-fragment-index="5"-->
      3. ReLU / leaky ReLU function
      <!-- .element: class="fragment" data-fragment-index="6"-->
      4. Sigmoid function
      <!-- .element: class="fragment" data-fragment-index="7"--> 
</div>


## Training 

<div id="left">

  + Dataset: collect a set of labeled training data:
  
  $\mathcal{D} = \left{(x_i,y_i) \right}^N $

  + Forward pass: pass the input values from model

  + Cost/loss function: compute the loss function e.g. mean-square error(MSE)

  $\mathcal{L}(\theta) = \Sum_{i=1}^N ||y_i - \hat{y_i}(x_i)||^2$

</div>

<div id="right">
  
</div>



# ML in Morris Method


## Axial Turbine: a Test Case

<div id="left">
  <img
      class="fragment fade-in"
      data-fragment-index="1"
      src="assets/TT.svg"
      height="450"
    />  
</div>
<div id="right">
  <img
      class="fragment fade-in"
      data-fragment-index="2"
      src="assets/PM.svg"
      height="450"
    />
</div>

+ 3 sections at hub, mid-span, and shroud.
<!-- .element: class="fragment" data-fragment-index="3"-->
+ 10 parameters at each section
<!-- .element: class="fragment" data-fragment-index="3"-->
+ Total 30 number of parameters for designing
<!-- .element: class="fragment" data-fragment-index="3"-->


## Classical Result

<div id="left">
  <img
      class="fragment fade-in"
      data-fragment-index="1"
      src="assets/results/bar_salib.png"
  />
</div>
<div id="right">
  <img
      class="fragment fade-in"
      data-fragment-index="2"
      src="assets/results/scatter_salib.png"
  />
</div>


## Deep Learning Result

<div id="left">
  <img
      class="fragment fade-in"
      data-fragment-index="1"
      src="assets/results/bar_surrogate.png"
  />
</div>
<div id="right">
  <img
      class="fragment fade-in"
      data-fragment-index="2"
      src="assets/results/scatter_surrogate.png"
  />
</div>


## Combined results

<img
    class="fragment fade-in"
    data-fragment-index="1"
    src="assets/results/A4_final.png"
/>


# Sources

+ Saltelli, A.: Global Sensitivity Analysis: the Primer, John Wiley & Sons, 2008.
+ Morris, M. D.: Factorial sampling plans for preliminary computational experiments. Technometrics, 33(2), 161-174, 1991.
+ Raj, R.; Tismer, A.; Gaisser, L:, Riedelbauch, S.: A deep learning approach to calculate elementary effects of morris sensitivity analysis, Proceeding in Applied Mathematics and Mechanics, 2024.
+ Fraas, S.; Tismer, A,; Riedelbauch, S.: Sensitivity study of numerical and geometrical parameters for structural mechanical analyses in the automatic design process of hydraulic machines, Proceeding of the 31st IAHR Symposium on Hydraulic Machinery and Systems, 2022.
+ Oh, M. H.; Kwon, M. W.; Park, K.; Park, B. G.: Sensitivity analysis based on neural network for optimizing device characteristics, IEEE Electron Device Letters, 41(10), 1548-1551, 2020.
