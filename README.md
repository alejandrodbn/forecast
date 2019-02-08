# Forecast_x: Toolkit with Naive models for time series.
![Forecast_x logo](https://www.alejandrodebarros.com/forecast_x.png)

[![PyPI version](https://badge.fury.io/py/forecast-x.svg)](https://badge.fury.io/py/forecast-x)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://github.com/alejandrodbn/forecast/blob/master/LICENSE)
[![Downloads](https://pepy.tech/badge/forecast-x)](https://pepy.tech/project/forecast-x)
[![Downloads](https://pepy.tech/badge/forecast-x/month)](https://pepy.tech/project/forecast-x)
[![Downloads](https://pepy.tech/badge/forecast-x/week)](https://pepy.tech/project/forecast-x)

__Forecast_x__ is a pure python package that provides different naive models for fitting multiple time series,
especially in batch process, due to its powerful flexibility and easy usage.

This library can be used in several industries with focus on manufacturing processes, where forecasting models
 with low cost of error are needed to plan raw material consumption.


## Models

Forecast_x uses the following models to produce forecast:

- Model Naive
- Model Seas Naive
- Model Mean Two Periods
- Model Mean Three Periods
- Model Half Seas Mean
- Model Seas Period Mean
- Model Double Seas Mean
- Model Seas Growth
- Model Expo Weighted
- Model Threefith Mean
- Model Multi Seas Mean
- Model Seas Double Mean Growth
- Model Grand Mean
- Model Smooth Grand Mean
- Model Last Seas Mean
- Model Current Mean Seas
- Model Smooth Double Seas Naive
- Model Truncated Mean
- Model Harmonic Mean
- Model Heronian Mean

## Getting started: 10 seconds to Forecast_x

Here is how-to use `Forecast_x` models:

```python
from forecast_x import forecast_x as fx

# time series observation
time_series = [51, 17, 28, 37, 52, 21, 34, 47, 38, 35, 7, 27]
freq = 12 # monthly
h = 12 # forecast months ahead

# Creating the forecast object
f = fx.forecast(time_series, freq, h)

# Applying any the model from the package
model = f.model_naive()

# The model variable would produce a list of three elements:
# - Fitting Values
# - Error
# - Forecast
model

```
To get only forecast of a given model you should use:

```python

f.get_forecast('model_naive')

```

To allow the package to select the best fit based on multiple cross validation you should use:

```python

model = f.best_model()
# forecast_x would select 'model_seas_period_mean' as best model based on test results
model
# Getting forecast from best model
forecast = get_forecast(model)

```

## Installation

```sh
# conda
conda install pandas
```

```sh
# or PyPI
pip install pandas
```


## Dependencies
- None.


## Python Version

Supported on 3.5, 3.6 and 3.7.


## License
[MIT](LICENSE)


## Documentation
The official documentation will be available soon.


## Release History

* 0.2: FIX: Bug on error selector, INCLUDE: Partial model documentation through `__doc__` command
* 0.11.1: FIX: Missing installation file.
* 0.10: The first proper release
* 0.1: Work in progress


## Citation

Citations or acknowledge on any work or project are very welcome:

> Alejandro De Barros. 2018.
> _Forecast_x: An open source forecasting tool for time series library for Python_

## Meta

Alejandro De Barros – (https://twitter.com/alejandrodbn) – alejandrodbn@gmail.com

Distributed under the MIT license. See ``LICENSE`` for more information.

[https://github.com/alejandrodbn/forecast](https://github.com/alejandrodbn/)

## Code of Conduct

Everyone interacting with this project's codebases, issue trackers, and mailing lists is expected to follow the Code of Conduct.


