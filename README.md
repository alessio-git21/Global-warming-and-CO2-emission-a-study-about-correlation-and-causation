# Global-warming-and-CO2-emission-a-study-about-correlation-and-causation

This project is about the global warming and the role of carbon dioxide and the solar cycle. 
The current scientific community agrees that the increase in carbon dioxide emissions is the cause of global warming, 
so my goal is to have a confirmation of this through my personal analysis.
The analysis demonstrated the causal relationship between the CO2 emission from human activities and the anomalous increase 
in the Earth’s average temperature with 90% confidence.
Concepts used:
* Spearman rank order correlation test
* mutual information
* time series stationarity: the Dickey-Fuller test
* Granger test for causality

The definition of Granger causality can be summarized in two statements:
* the cause precedes the effect
* the cause contains an information on the effect which is unique and is not
   contained in any other variable.


## Data
### TEMPERATURE ANOMALIES
This is the time series for the temperature. It represents the temperature anomalies from the 1880 and 2016. 
Temperature anomalies are the values for the temperature with respect a mean of a certain base period: the base period for this time series is from 1951 to 1980. 
Data come from the GISS (Goddard Institute for Space Studies) Surface Temperature Studies, a NASA project.
![download](https://github.com/alessio-git21/Global-warming-and-CO2-emission-a-study-about-correlation-and-causation/assets/100300894/9f825199-1f01-4dd4-9368-b05220a0260b)


### CO2 EMISSION
This time series represent the annual carbon dioxide emission from the burning of fossil fuel energy and cement production. 
It is evident that with the industrial revolution the emission drastically increased.
![download](https://github.com/alessio-git21/Global-warming-and-CO2-emission-a-study-about-correlation-and-causation/assets/100300894/321d3249-a6d5-428b-b92a-7ad998dc833c)


### SOLAR ACTIVITY
The clearest visible sign of solar activity are these sunspots. A sunspot looks like a ragged hole in the solar surface. 
These are some characteristics of sunspots. Their temperature is 1500 K below that of its surrounding, that is about 6000 K 
and that’s the reason why we see this region as dark regions. The low temperature in due to the fact that in these regions there is a strong magnetic field  that inhibits convective energy transport from the central region. When solar surface shows a large number of spots the Sun is going through a phase of greater activity and emits more energy into the surrounding space. The number of sunspots varies with an average period of about 11 years. 
This is the time series that shows the annual mean number of sunspots. The period of 11 year is evident. Data come from the Solar Influences Data analysis Center, a part of Royal observatory of Belgium.

![download](https://github.com/alessio-git21/Global-warming-and-CO2-emission-a-study-about-correlation-and-causation/assets/100300894/108a56d6-d011-449f-8720-b4d2a6380256)

## Results
In this section the results about the correlation and causation tests are shown.

### Spearman rank order correlation test

CO2 EMISSION AND TEMPERATURE ANOMALIES CORRELATION:
* Spearman correlation degree: 0.87
* p value: 5.866665028465032e-44

SOLAR ACTIVITY AND TEMPERATURE ANOMALIES CORRELATION
* Spearman correlation degree: 0.13
* p value: 0.12

### Mutual information
The mutual information between the CO2 emission and the temperature anomalies results to be significative:
* Mutual info value: 1.1
* Significance level: 1%


### Delay mutual information
In this figure, positive values of time delay means that we are considering the correlation between the past values of the co2 emission and the future values of 
the temperature anomalies, while for negative values of time delay we are considering the correlation of the past values of temperature anomalies and the future 
values of the co2 emission. The correlation is unbalanced toward the positive time delay values: this results may lead us to suspect that there is a causality 
between co2 and temperature anomalies.

![download](https://github.com/alessio-git21/Global-warming-and-CO2-emission-a-study-about-correlation-and-causation/assets/100300894/155b1948-1ef4-4e13-b22c-a41a26d9940f)

### Granger test for causality
Granger test for causality shows that CO2 emission "Granger causes" temperature anomalies.
![granger_res](https://github.com/alessio-git21/Global-warming-and-CO2-emission-a-study-about-correlation-and-causation/assets/100300894/603351ea-b475-4655-907b-495dcc31907d)




## Packages
* numpy
* pandas
* scikit-learn
* statsmodels


## References
[Krarkov et al. «Estimating mutual information» in Physical Review E 69, (2004)](https://arxiv.org/abs/cond-mat/0305641)

[C. Ross «Mutual Information between Discrete and Continuous Data Sets» in PLOS one, (2014)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0087357)
