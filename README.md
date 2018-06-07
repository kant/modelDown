# modelDown

[![Travis-CI Build Status](https://travis-ci.org/kromash/modelDown.svg?branch=master)](https://travis-ci.org/kromash/modelDown)

`modelDown` generates a website with HTML summaries for predictive models.
Is uses [DALEX](https://github.com/pbiecek/DALEX) explainers to compute and plot summaries of how given models behave. We can see how exactly scores for predictions were calculated (Prediction BreakDown), how much each variable contributes to predictions (Variable Response), which variables are the most important for a given model (Variable Importance) and how well out models behave (Model Performance).

Documentation and examples of use: [docs/index.html](https://htmlpreview.github.io/?https://raw.githubusercontent.com/kromash/modelDown/master/docs/index.html)

## Index page

![Index page](https://github.com/MI2DataLab/modelDown/blob/master/misc/index.PNG)

Index page presents basic information about data provided in explainers. You can also see types of all explainers given as parameters. Additionally, summary statistics are available for numerical variables. For categorical variables, tables with frequencies of factor levels are presented.

## Model performance

![Model performance](https://github.com/MI2DataLab/modelDown/blob/master/misc/performance.PNG)

Module shows result of function `model_performance`. 

## Variable importance

![Variable importance](https://github.com/MI2DataLab/modelDown/blob/master/misc/importance.PNG)

Output of function `variable_importance` is presented in form of a plot as well as a table.

## Variable response

![Variable response](https://github.com/MI2DataLab/modelDown/blob/master/misc/response.PNG)

For each variable, plot is created by using function `variable_response`. Plots can be easily navigated using links on the left side. One can provide names of variables to include in the module with argument `vr.vars` (if argument is not used, plots for all variables of first explainer are generated).

## Prediction breakdown

![Prediction breakdown](https://github.com/MI2DataLab/modelDown/blob/master/misc/prediction.PNG)

Module presents plot generated with function `prediction_breakdown` for particular observations. Observations to be presented can be provided by user as input parameter (named `pb.observations`), otherwise, for each explainer, observation with highest residual value is presented. You can also see exact values of the observation in the generated table.
