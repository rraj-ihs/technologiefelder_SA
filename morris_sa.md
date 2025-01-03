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
