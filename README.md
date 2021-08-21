# Surfs Up - Surf Shop Weather Analysis

## Overview
The purpose of this analysis is to analyze weather data from Oahu to determine if a surf and ice cream shop business is sustainable year round.

## Results

![June Temperature Summary](https://github.com/deklund76/surfs_up/blob/main/resources/june_temps.png)

![December Temperature Summary](https://github.com/deklund76/surfs_up/blob/main/resources/december_temps.png)

* June fairly consistently about 4 degrees warmer than December
* December has greater variability in temperature as seen by its larger standard deviation
* December's coldest weather is significantly colder than June's (8 degress)

## Summary

With temperatures consistently in the 70s year round, and plentiful waves, Oahu is a great location for a combination surf and ice cream shop. The only thing we would still want to be sure of is that it doesn't rain most of the time. The two queries below using sqlalchemy can get us that information.

### Precipitation data for June
session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

### Precipitation data for December
session.query(Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
