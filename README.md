# QRT-Data-Challenge-2021

This Repo contains some simple examples for the QRT data challenge 2021. 

- The task involves predicting the prices of 100 LIQUID assets based on the prices of 100 ILLIQUID assets.
- To keep things simple, we are only looking at the price movements, and thus associate $\pm 1$ values to positive/negative price shifts.
- Note, however, that it is more important to predict correctly larger price shifts. Hence, we use a custom accuracy function:

<p align="center">
<img src="https://latex.codecogs.com/svg.image?&space;f(\boldsymbol{y},\hat{\boldsymbol{y}})=\frac{1}{||\boldsymbol{y}||_1}\sum^{n}_{i=1}|y_i|\times\boldsymbol{1}_{\hat{y}_i={\rm&space;sign}(y_i)}" title=" f(\boldsymbol{y},\hat{\boldsymbol{y}})=\frac{1}{||\boldsymbol{y}||_1}\sum^{n}_{i=1}|y_i|\times\boldsymbol{1}_{\hat{y}_i={\rm sign}(y_i)}"/>
</p>

Here $\boldsymbol{1}_{\hat{y}_i={\rm sign}(y_i)}$ is 1 if the $i^{\rm th}$ prediction $\hat{y}_i$ is of the same sign as the true value $y_i$.

- We use some simple models, and run some grid searches to optimize the parameters.
