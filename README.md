Time-series Analytical Study on the 
Fluctuations and Trends in Air pollution 
Levels in Kolkata 
Abstract 
Air pollution is a curse of the modern era. It has attained a dreadful situation. In highly populated urban areas, such as Kolkata, the problem is particularly for various reasons like industrial wastes and emissions, vehicular smoke, meteorological conditions, etc. Especially for air pollution, there is a huge impact on climate actions that cause abrupt changes in climate like global warming, droughts, unnecessary floods, imbalance ecological factors, etc. The present study is conducted to understand the impermanent and geographical variations of four major pollutants i.e. Particulate matter (PM)2.5, PM10, Sulfur dioxide (So2), and nitrogen dioxide (No2) in several monitoring stations of Kolkata between one year (April,2022-March,2023). The required dataset for this study is collected from the West Bengal Pollution Control Board (WBPCB). This case study deals with the prediction of the air quality model which is based on the Autoregressive Integrated Moving Average (ARIMA). 
Introduction 
Air pollution is a penetrating environmental challenge that has a huge impact on geographical aspects of life, and the health of millions and threatens the balance of the ecosystem. In the era of random and unplanned urbanization, rapid industrialization, and increasing vehicular emissions, the city of Kolkata stands as a representation of the global endeavour against crumbling air quality.  
In terms of pollution, Kolkata has surpassed Delhi. Kolkata is a metropolitan city and according to sources, it is ranked as the second most polluted city in the country and its air quality index is declining faster than that of Delhi.1  
The air pollution situation in Kolkata has been analysed from different perspectives, but this present study has taken into account the major pollutants, present in the air such as Particulate matter (PM)2.5, PM10, Sulfur dioxide (So2), and nitrogen dioxide (No2).2 Looking at the growing urban spaces associated with the increasing number of city inhabitants, demand for higher consumption, and the plan to build 100 new smart cities in India; it is needed to take the initiative with a vision and commitment to Sustainable Cities and Human Settlements objective (SHS) includes aims for urban planning, resilience preparation, urban sustainability, health and well-being, and the integration of housing, transportation, and open spaces. Future development of low-carbon cities based on nonpolluting energy resources should be a primary objective. With this background, the current paper's subject matter has been framed under three broad headings: the state of the urban environment in terms of air quality and addressing some appropriate measures aimed at mitigating the menace of air pollution in order to pave the way for bringing sustainable urban development to Kolkata.3 
The current technology for precise and reliable pollution measurement is expensive. Because of the significance of pollution monitoring, multiple organisations routinely use low-cost sensors for regular assessments in different regions. However, these sensors may not be reliable if they are not calibrated on a regular basis with a standardised monitor. It is also essential that the general public be able to understand the information derived from these measures. Public interest concerns often include the overall pollution levels at different areas in comparison to their respective regulatory limits, seasonal and daily variations in their levels, potential annual increases or decreases in pollution, correlations with recognised events, and so forth.4 
Materials 
Dataset:  The primary source of data under study is a dataset containing monthly measurements of ambient air quality indicators in the city of Kolkata from 2022-2023. The dataset is available and was taken from 
https://docs.google.com/spreadsheets/d/1W1JJep1OVgW-CWZOwafHlI0ztXzrs92pbGZsBtbK0fA/edit?gid=0#gid=0 
Data Characteristics:  The dataset under study encircles various components of air (air quality parameters) such as Particulate matter (PM2.5 and PM10), sulfur dioxide (So2) and nitrogen oxide (No2). 
Data Pre-processing :  The preprocessing steps include checking the robustness of the data, the conversion of the timestamp to a time series format and examination of outliers presents in the dataset or not. 
To ensure the suitability of the data for time-series analysis, Augmented Dickey-Fuller test was performed 
Software and Packages:  The modelling and analysis of the data were conducted using the R programming language. 
The important R packages engaged in this study include: 
•	‘forecast’: Used for time-series forecasting and modelling. 
•	‘tseries’: Optionally utilized for the Augmented Dickey-
Fuller test for stationarity. 
  
Statistical and Machine Learning Methods: 
•	Time-series analysis techniques, including statistical methods, trend analysis, and seasonality decomposition, were applied to explore temporal patterns in air pollution levels in the city of Kolkata. 
•	The ‘auto.arima’ function was used to automatically determine the best ARIMA order for the time series data. 
•	The ARIMA model was fitted using the Arima function, and forecasting was conducted with the forecast function. 
Methodology 
Data Analysis ;  
Nature of the data:  By using ‘summary’ function in R we obtain the nature of the data i.e. the mean of the data, the mode of the data and the median of the data. Minimum value and maximum value are as important as the above-mentioned nature are. These are used to measure of dispersion of the data and to obtain the variances, standard deviation, quartile deviation and the various moments of the data. 
Correlation Analysis:  Correlation analysis was used to investigate the correlations between various pollutants and meteorological parameters. This step highlighted the interdependence of multiple factors affecting air quality. 
Data Visualization:  Data visualisation is a crucial part of data analysis since it helps people to examine patterns, trends, and correlations in a dataset in a clear and intuitive way. Diverse simulation techniques serve different functions in generating insights. Here are some instances of frequently used data visualisation techniques. 
Pie Chart:  Pie diagrams are easy for illustrating the proportion of several sections within a larger whole. It is used to estimate the distribution of pollutants or air quality indices, emphasize each component's proportion contribution to the total. 
Box Plot (Box-and-Whisker Plot):  Box plots illustrate a dataset's distribution by highlighting key statistical parameters such as median, quartiles, and probable outliers. It is useful for visualising the fluctuation in pollutant concentrations or other control parameters across time between many monitoring stations. 
Histograms: Histograms are used to visualise a continuous variable's distribution by partitioning it into bars and representing the frequency of observations in each box. It can help us to understand the distribution of pollutant concentrations by recognizing trends as skewness or multimodality. 
Line Diagram (Time Series Plot):  Line diagrams are indispensable for portraying trends and patterns through time. It is suitable for presenting hourly, daily, or monthly fluctuations in air pollution levels, assisting in the recognition of trends, peaks, and troughs. 
Frequency Polygon:  Frequency polygons, like histograms, indicate the percentage of a continuous variable. They do, however, utilise lines to link the centre-point of each box, resulting in a moresmooth representation of the distribution. It provides an in - depth picture of the structure of the distribution of air quality indicators, particularly when compared across various geographical regions or time periods. 
Scatter Plot:  Scatter plots, which illustrate individual data points, demonstrate the relationship between two continuous variables. It is effective in finding possible dependencies by largely determines correlation or trends between different air quality parameters.5  ARIMA Modelling:  Based on the differenced time series data, the Auto ARIMA method was used to automatically determine the optimal order for the ARIMA model. 
The ARIMA model was fitted with the specified order, and the forecast function was used to estimate potential pollution levels over a one-year time scale.7 
Mathematical Background of predictive modelling: 
ARIMA is a prominent time series forecasting model that integrates autoregression, differencing, and moving averages. ARIMA (p, d, q) denotes the model, where: 
•	The order of the autoregressive (AR) component is denoted by p. 
•	d denotes the degree of differentiation. 
•	The order of the moving average (MA) component is denoted by q. 
Autoregressive (AR) Component: The ARIMA model's autoregressive component is expressed as: 
Yt = c+ϕ1Yt−1+ϕ2Yt−2+…+ϕpYt−p+ϵt……………(I) 
Here, Yt is the time series at time t, ϕi denotes the autoregressive coefficients, c is a constant, and ϵt denotes white noise. 
Integrated (I) Component: The time series integration is expressed by the differencing factor. It is denoted by the symbol I(d) and is used to make the time series stationary. The differentiating function is defined as follows: 
Zt =(1−B)d Yt…………………………………………………(II) 
where B is the backshift operator (BYt=Yt−1). 
 
Moving Average (MA) Component: 
The moving average component is denoted as: 
Yt=μ+θ1ϵt−1+θ2ϵt−2+…+θqϵt−q+ϵt……………….(III) 
 
Here, θi are the moving average coefficients, μ is the mean of the series, and ϵt is white noise. 
ARIMA Model: 
When all of this is included, the ARIMA model is provided by: 
Zt =c+ϕ1Zt−1+ϕ2Zt−2+…+ϕpZt−p+(1−B)dYt =μ+θ1ϵt−1+θ2ϵt−2+…+θqϵt−q+ϵt 
….(IV) 
Estimation: The parameters (ϕi, θi, c, μ) of the ARIMA model is calculated using methods such as maximum likelihood estimation  (MLE).4 
ARIMA models are predicated on the assumption that the time series is stationary after contrasting. As a result, examining the autocorrelation and partial autocorrelation functions to determine optimum value of p, d, and q is critical.  
Forecasting: Once the model has been estimated, it may be used to anticipate future time series values. 
This is a high-level summary of the ARIMA model's mathematical analysis. The actual estimating and forecasting methods involve advanced statistical approaches and calculations.6 
Results 
By analysing the nature of the dataset we find the various aspects of data structure like from the table 1 we get PM2.5’s minimum concentration 8.57 µg/m³, maximum concentration: 152.95 µg/m³, median (50th percentile): 34.44 µg/m³, mean concentration:47.26µg/m³. Most of observations lie between 21.4 3 g/m3 (1st quartile) and 70.00 g/m3 (3rd quartile). 
  
Table 1: data summary of PM2.5. 
From table 2, we obtain PM10’s minimum concentration: 8.57 µg/m³, maximum concentration: 152.95 µg/m³, median (50th percentile): 34.44 µg/m³, mean concentration: 47.26 µg/m³. Majority of observations fall between 21.43 µg/m³ (1st quartile) and 70.00 µg/m³ (3rd quartile). 
  
Table 2: data summary of PM10. 
From table 3, we obtain No2’s minimum concentration: 12.69 ppb (parts per billion), maximum concentration: 53.16 ppb, median (50th percentile): 27.05 ppb, mean concentration: 27.48 ppb. Majority of observations fall between 23.90 ppb (1st quartile) and 30.72 ppb (3rd quartile). 
  
Table 3: data summary of No2. 
From table 4, we obtain So2’s minimum concentration: 3.480 ppb, maximum concentration: 27.950 ppb, median (50th percentile): 7.740 ppb, mean concentration: 8.177 ppb. Majority of observations fall between 5.790 ppb (1st quartile) and 10.170 ppb (3rd quartile). 
  
Table 4: data summary of So2. 
These statistics give a basic understanding of the dataset's central tendency, dispersion, and variation of air pollutant concentrations. Further study, such as the use of histograms or box plots, could provide further information on the distribution of these pollutants. The graphs and diagrams are mentioned below to gain the practical experimentation of data, shown in the figures. 
  
Figure 1: Histogram of PM2. containing one year trend. 
 
 
 
Figure 2: Histogram of PM10 containing one year trend. 
 
Figure 3: Histogram of No2 containing one year trend. 
 
Figure 4: Histogram of So2 containing one year trend. 
 
 
Figure 6: Frequency polygon. 
 
Fitted Values:   
The fitted values are the values forecasted by the ARIMA model applying historical data. 
Residuals: 
The variations between the observed and fitted values are known to as residuals. The residuals must be tested to determine the goo dness of fit. 
Model Coefficients:  These are the ARIMA model's estimated parameters. Coefficients for autoregressive (AR) terms, variances, and moving average (MA) terms are also included. 
The outcomes include statistical measures and diagnostics for model fit, such as AIC (Akaike Information Criterion), BIC (Bayesian Information Criterion), and statistical sampling tests. 
The visualization can be shown in the graphs. 
  
Graph 1: ARIMA forecast for PM2.5. 
 
Graph 2: ARIMA forecast for PM10. 
 
Graph 3: ARIMA forecast for No2.  
 
Graph 4: ARIMA forecast for So2. 
Conclusion 
This time-series analytical study has provided valuable insights into the fluctuations and trends in Kolkata's air pollution levels, with a special emphasis on pollutants such as PM2.5, PM10, No2, and So2. We hoped to estimate future pollution levels and contribute to the improvement understanding of the dynamics of air quality in the neighbourhood by using ARIMA modelling techniques. 
The study revealed distinct patterns in the time series data for each pollutant, emphasising the significance of taking specific pollutants into account when evaluating air quality. The underlying temporal patterns were successfully captured by the ARIMA models, allowing us to make reasonable predictions for the upcoming year. 
 
Due to the impact on public health and the environment, the results demonstrated the need of addressing air quality concerns  in Kolkata. Because of the city's sensitivity to changes in pollution levels, regular monitoring and strategic measures are required to reduce negative effects. 
ARIMA modelling has been shown to be useful in creating forecasts, providing a foundation for proactive decision-making and the development of specific pollution control strategies. It is crucial to acknowledge the models' limitations, such as the assumption of serial correlation and the necessity for frequent assessment when environmental circumstances have changed. 
This finding contributes to the broader discussion about urban air quality management and serves as a basis for ongoing efforts to monitor, evaluate, and address air pollution challenges in Kolkata and other urban environments. Finally, a multidisciplinary approach and a commitment to environmental sustainability are required to provide cleaner and healthier living conditions for Kolkata residents. 
References 
1.	Air Pollution in Kolkata, Causes, Effects & Control 
Measures.pdf. 
2.	Biswas, K., Chatterjee, A. & Chakraborty, J. Comparison of Air 
Pollutants Between Kolkata and Siliguri, India, and Its Relationship to Temperature Change. J. Geovisualization Spat. 
Anal. 4, 25 (2020). 
 
3.	Haque, Md. & Singh, R. Air Pollution and Human Health in Kolkata, India: A Case Study. Climate 5, 77 (2017). 
4.	Roy, S., Sengupta, D., Rudra, K. & Saha, U. S. Analysis of Pollution Patterns in Regions of Kolkata. Calcutta Stat. Assoc. Bull. 72, 133–170 (2020). 
5.	Ventura, L. M. B., De Oliveira Pinto, F., Soares, L. M., Luna, A. S. & Gioda, A. Evaluation of air quality in a megacity using statistics tools. Meteorol. Atmospheric Phys. 130, 361–370 
(2018). 
6.	Kumar, U. & Jain, V. K. ARIMA forecasting of ambient air pollutants (O3, NO, NO2 and CO). Stoch. Environ. Res. Risk Assess. 24, 751–760 (2010). 
7.http://emis.wbpcb.gov.in/airquality/JSP/aq/districtwiseReport.jsp 
