
<!-- README.md is generated from README.Rmd. Please edit that file -->

# EPAC model

<!-- badges: start -->
<!-- badges: end -->

This package implements the Early Pandemic Age-Structured Compartmental
(EPAC) model developed by [@wzmli](https://github.com/wzmli) and
[@papsti](https://github.com/papsti) at
[@phac-nml-phrsd](https://github.com/phac-nml-phrsd) using
[`macpan2`](https://github.com/canmod/macpan2) modelling software.
**This package is still in development.**

The goals of this package are to document the model, provide tools for
simulating and calibrating the model, as well as visualizing model
outputs.

## Installation

You can install the development version of EPACmodel like so:

``` r
# FILL THIS IN! HOW CAN PEOPLE INSTALL YOUR DEV PACKAGE?
```

## Getting started

``` r
library(EPACmodel)
```

First, load a model. You can list the available model names here:

``` r
list_models()
#> [1] "two-age-groups"
```

``` r
model_name = "two-age-groups"
model = get_model(model_name)
```

This object encodes only the model *structure*. In order to simulate
from this model, we need to attach parameters, as well as an initial
state.

The default parameters and initial state for each model can be loaded
with:

``` r
params = get_params(model_name)
state = get_state(model_name)
```

Once these vectors are loaded, you can modify manually in-session if you
like before constructing the model simulator.

Once we have the model pieces, we need to put them together to construct
a **simulator**, which is an object that we can use to numerically
simulate the model:
