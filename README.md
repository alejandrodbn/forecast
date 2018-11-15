# Forecast_x
> A pure python toolkit with Naive models for time series.

Forecast_x provides different models for fitting time series, applying a naive approach, making easy to forecast several time series.



## Installation

```sh
pip install -U forecast-x
```


## Examples

``` python
from forecast_x import forecast_x as fx

#time series
time_series = [12, 10,17,41,74,12,74,25,85,42]
#frequency
q = 4
#number of periods ahead
h = 12

f = fx.forecast(t, q,h)

#automatically selects the best fit from 13
#different models
model = f.best_model()

#gets the forecast best on model selected
fcst = f.get_forecast(model)
```

## Release History

* 0.11
    * FIX: Missing installation file.
* 0.10
    * The first proper release
* 0.0.1
    * Work in progress

## Meta

Alejandro De Barros – (https://twitter.com/alejandrodbn) – alejandrodbn@gmail.com

Distributed under the MIT license. See ``LICENSE`` for more information.

[https://github.com/alejandrodbn/forecast](https://github.com/alejandrodbn/)

## Code of Conduct
Everyone interacting with this project's codebases, issue trackers, and mailing lists is expected to follow the Code of Conduct.
