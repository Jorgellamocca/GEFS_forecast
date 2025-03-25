NOAA GEFS forecast, 35 day
updating
Spatial domain	Global
Spatial resolution	0-240 hours: 0.25 degrees (~20km), 243-840 hours: 0.5 degrees (~40km)
Time domain	Forecasts initialized 2020-10-01 00:00:00 UTC to Present
Time resolution	Forecasts initialized every 24 hours.
Forecast domain	Forecast lead time 0-840 hours (0-35 days) ahead
Forecast resolution	Forecast step 0-240 hours: 3 hourly, 243-840 hours: 6 hourly
https://data.dynamical.org/noaa/gefs/forecast-35-day/latest.zarr?email=optional@email.com
 ⎘

* Email optional. Providing your email as a query param helps us understand usage and impact to keep dynamical.org supported for the long-term. For catalog updates follow here.

The Global Ensemble Forecast System (GEFS) is a National Oceanic and Atmospheric Administration (NOAA) National Centers for Environmental Prediction (NCEP) weather forecast model. GEFS creates 31 separate forecasts (ensemble members) to describe the range of forecast uncertainty.

This dataset is an archive of past and present GEFS forecasts. Forecasts are identified by an initialization time (init_time) denoting the start time of the model run as well as by the ensemble_member. Each forecast has a 3 hourly forecast step along the lead_time dimension. This dataset contains only the 00 hour UTC initialization times which produce the full length, 35 day forecast.

Storage for this dataset is generously provided by Source Cooperative, a Radiant Earth initiative.
