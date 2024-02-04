---
title: "Multivariate Time Series Prediction Based on GNN-GLU Model"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/model_archi.png'>"
collection: portfolio
---
# Introduction

Time series forecasting plays a vital role in a wide range of real-world applications, from economics and finance to 
transportation. Predicting future trends based on historical data can help us make better decisions. For example, if we
can get accurate forecasts of the stock and the commodity markets, we can make considerable profits from the forecasts.
Moreover, if we can forecast the trend of COVID-19 new cases, we can allocate medical resources to prevent the epidemic
outbreak in advance.

Multivariate time series data contains time series from multiple interlinked data. In addition to forecasting the trend
based on historical temporal patterns within each time series, we can utilize the correlations between different time series
to improve the accuracy of forecasting. For instance, as shown in Figure 1, the prices of crude oil and gasoline are highly
correlated and the rise in crude oil may indicate a rise in the price of gasoline in the near future. The observation motivates
that utilising the information from both time series would help us better forecast the trend of each one.

**Significance and Novelty** &emsp; Making accurate multivariate time series forecasting is challenging, especially in some
complicated scenarios such as the stock market, where the correlations between different stocks are not fixed and difficult
to capture. Some traditional statistical methods may fail because they assume there are linear correlations among time
series[1]. Besides, deep learning models involving LSTM [2] and GRU[3] do not perform well because it is difficult for
them to extract spatial and temporal features jointly[4]. Aiming to capture inter-series correlation and intra-series patterns
jointly, we proposed a GNN-GLU model to shuttle between the temporal and spectral domains and make forecasts based
on information from multivariate time series data. To verify the significance of our model, we also conduct experiments
on stock forecasting and COVID-19 new case forecasting with real-world data.

# Methodology

The illustration of our model is shown in Figure 2. Given multivariate time-series $ X $ as input, we first generate the
correlations among different time series and build the graph $ \mathcal{G}  $. Then we put $ \mathcal{G}  $ into the following three layers. Firstly, the **Spectral Layer** contains a Graph Fourier Transform, an Intra-series Layer, a Spectral Graph Convolution, and an
inverse Graph Fourier Transform. It mainly captures the inter-series relationship. Secondly, the **Intra-series Layer**
performs Discrete Fourier Transform, 1D Convolution, GLU, and inverse Discrete Fourier Transform. It mainly learns
the intra-series features. Thirdly, the **Temporal Layer** applies the GLU and Fully-connected layer (FC), making the
prediction.

$$ \mathcal{L}(\widehat{X}_{t}, X_{t} ; \Theta)=\sum_{t=K}^{T}\|\widehat{\boldsymbol{X}}_{\boldsymbol{t}}-X_{t}\|_{2}^{2}+\frac{\lambda}{2}\|\Theta\|_{2}^{2} $$

