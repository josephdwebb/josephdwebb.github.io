---
layout: post
title: What makes a Tick Tick?
caption: Evaluating the Impact of Climatic Factors on Tick-Borne Pathogen Prevalence - Insights from Ixodes scapularis and its Borrelia burgdorferi, Anaplasma phagocytophilum, and Babesia microti Pathogens

description: >
  Summarizing my work in UVM Honors Thesis Work.
date: 1 April 2024
image: 
  path: /assets/img/projects/TIckCollecting.jpg
  srcset: 
    1920w: /assets/img/projects/TIckCollecting.jpg
    960w:  /assets/img/projects/TIckCollecting.jpg
    480w:  /assets/img/projects/TIckCollecting.jpg

sitemap: false
featured: true
---

# What Makes a Tick Tick?

> This work represents a portion of my Honors Thesis. Stay tuned for further updates!

* toc
{:toc}

# Methods
We merged four types of data to conduct the regression analysis in this study: meteorological data from the National Oceanic and Atmospheric Administration (NOAA), ground-level observed PCR results of adult I. scapularis samples, annual state-level epidemiological data on Lyme disease, babesiosis, and anaplasmosis cases from the CDC, and climate projections from CHELSA. The CDC, NOAA, and CHELSEA databases are publicly available. 

## 1.1 Meteorological Data 
The Global Summaries dataset, referred to as GSOM for Monthly, provides monthly meteorological data spanning from 1763 to the present. It includes various parameters such as monthly mean maximum, mean minimum, and mean temperatures, total precipitation, snowfall, departure from normal temperature and precipitation, heating and cooling degree days, days with extreme temperatures and precipitation, foggy days, and thunderstorm occurrences. These data are sourced primarily from the Global Historical Climatology Network - Daily (GHCN-Daily) dataset (Lawrimore, 2016). 

### 1.1.1 Forest Matching 
New England state forests, in conjunction with established research sites affiliated with the UVM Wildlife Pathogens Laboratory, were aligned with NOAA weather stations by a spatial correspondence procedure. Leveraging the Haversine formula to account for the Earth’s curvature, a cohort of 146 weather stations was successfully paired with their corresponding forest locations, exhibiting an average spatial separation of 10 kilometers. However, the spatial disparity between forests and their matched weather stations exceeded one standard deviation for 77 forest locations, signifying a non-negligible level of spatial discrepancy. 

### 1.1.2 Preprocessing 
Among the matched weather stations, a total of 57 climatic variables were recorded; however, not we found not all weather stations were uniform in their data collection capabilities. Remarkably, 42% of the 146 stations failed to measure climatic variables, excluding DP01, DP10, DP1X, DSND, DSNW, DYSD, DYSN, DYXP, EMSD, EMSN, EMXP, PRCP, and SNOW, for the month of July 2022. Moreover, only 58% of stations provided measurements for average temperature. Forest sites paired with weather stations characterized by incomplete meteorological data were deemed inadequate for further analysis and thus excluded from subsequent investigations. 

### 1.1.3 Site Selection 
To identify representative forest sites for modeling New England climatic dynamics, two Principal Component Analyses (PCA’s) were conducted. PCA[1], which incorporated all variables except TAVG, and PCA[2], which excluded PRCP, were employed. The variables TAVG and PRCP were plotted against their respective PCA axes. Through a rigorous selection process, four forest sites were identified based on the following criteria: (1) representation of the four quartile ranges of average temperatures and precipitations in New England, (2) minimal summed residual across both regressions, and (3) accessibility and availability of scientific collection permits. The output of this selection process can be seen in Figure: 1. The sites deemed most representative for modeling New England climatic dynamics were: Mountain Laurel Estates, Goffstown, NH; Jericho Research Center, Jericho, VT; St. Mikes, Winooski, VT; and Ashburnham State Forest, Ashburnham, MA. 

## 1.2 Molecular Data 
### 1.2.1 Field Sampling 
Adult I. scapularis specimens were collected from designated sites between May and September of 2023, following landowner consent. Collection was conducted using a 1x1 meter white drag cloth. Each collected specimen was preserved in 250 mL plastic tubes containing 100 mL of 100% ethanol. To maintain and store specimens, each tube accommodated a maximum of 10 samples and was stored at room temperature until transferred to a freezer set at -17.8°C until future molecular analysis. Given that the sampling period coincided with a period of dormancy for adult I. scapularis, site revisits were conducted weekly until an approximate total of 50 samples per site were obtained. 

### 1.2.2 Molecular Methods 
To detect the presence of B. burgdorferi, B. microti, and A. phagocytophilum, all specimens were screened by PCR methods. DNA was first extracted from full body samples using the Qiagen DNeasy Blood and Tissue Kit following manufacturer’s instructions. Following the procedure for Multiplex PCR in Diagnostic Virology, we used the forward primers RecR, 5BM, and 5AP and the reverse primers RecF, 3BM, and 3AP (Elnifro et al., 2000). In the thermocycler, the samples were run in cycles of 94°C for 30 seconds, 56°C for 90 seconds, and 72°C for 90 seconds. A total of 40 cycles were completed, with a 15-minute denaturation at 95°C and a final extension of 72°C for 10 minutes. 

The PCR products were subjected to gel electrophoresis using 2% agarose gels to facilitate size differentiation. This technique enabled the identification of distinct bands corresponding to the amplified DNA fragments. Specifically, a band at approximately 550 base pairs signified a positive infection of B. burgdorferi, while a band at approximately 310 base pairs indicated a positive infection of B. microti. Additionally, the presence of a band at approximately 1200 base pairs was indicative of a positive infection of A. phagocytophilum. The recorded infections were documented, and the samples were properly disposed of in accordance with established laboratory protocols.

## 1.3 Empirical Strategy
Using an incidence model derived from an exponential growth model and climatic dependent multiple linear regression, the regression model to examine the impact of the change in climatic variables Ci - in our case, the change in average temperature and total precipitation in July—on an outcome of interest Yt - in our case, the prevalence of pathogens - takes the form:

𝑌_𝑡=𝑌_0 (1+"ρ" )^𝑡+∑24_(𝑖=1)^𝑛〖"∂Y" /("∂" 𝐶_𝑖 )("β" _𝑖 𝐶_𝑖+"ε" _𝑖)〗


where i indexes different climatic variables, t indexes time, and ρ indexes the growth rate of Y independent of the change in climatic variables defined by Ci. The error process ϵi is modeled using standard errors, allowing for arbitrary correlation over time and space in the covariance matrix clustered at the state level. 

Recognizing the random variations in climatic variability, akin to weather changes that draw from the broader state climate distribution, Ci considers the change in such variables with the assumption that variability will be reduced across dimensions. The future projection for C is collected from v2.1 CHELSA monthly projections across the models SSP126, SSP370, and SSP575 (Karger, 2017). Consequently, Ci pinpoints the causal impact of climatic variations on disease incidence. The inclusion of the observed growth rate, denoted as ρ, effectively absorbs unobservable spatial characteristics. 

The selection of temperature and precipitation as primary climatic variables in our study is rooted in their profound impact on the activity and abundance of I. scapularis. Temperature regulates the mobility of these ticks, influencing their ability to seek hosts, while humidity governs their questing behavior. While relative humidity is an optimal measure, its limited availability necessitated the use of precipitation, which also significantly affects tick behavior. Thus, comprehending the intricate interplay between temperature, precipitation, and tick activity is paramount for understanding disease dynamics and devising effective preventive strategies.

A fundamental issue with Equation 1 is regarding the functional form of C. Based off the noted trends in collected data, it was determined to consider the variables across a continuous spectrum, as opposed to bins for temperature and precipitation. As a result, the output is considered across a continuous spectrum. In this context, the functional form of C is determined by the nature of the climate data and how it varies continuously over time or space, that adequately captures the continuous variation in temperature or precipitation over the relevant time period or geographic area. The choice of employing β values for each variable, represents an effort to allow the data, rather than polynomial assumptions, to determine the incidence-variable relationship. This degree of flexibility and freedom from assumption as the sites were selected as highly representative of New England ecology. 

The second aspect to consider regarding Equation 1 pertains to the necessity of an accurate and precise ρ. The observed rate of growth is defined as the annual change in the prevalence of the disease-causing pathogens, accommodating unobserved variations across sites. The underlying assumption posits that ρ represents the average rate of change over each time step, t, and remains independent of the climatic variables, C. As time (t) progresses, the significance of ρ increases exponentially. Furthermore, the assumption is made that pathogen prevalence follows an exponential growth model. This assumption finds partial support from CDC observations of annual incidence cases and the absence of evidence suggesting a carrying capacity beyond the presence of ticks and reservoir species. Consequently, this equation is applicable solely in scenarios where ixodid ticks are anticipated to be present. The methodology for computing ρ is elaborated upon in the subsequent section. 

## 1.4 Epidemiological Data 
In order to calculate ρ, we collected CDC incidence reports for Lyme disease, Babesiosis, and Anaplasmosis, and applied a rigorous function that seeks to fit an exponential model to the dataset. The function begins by initializing parameters for time, where each data point is indexed sequentially. Subsequently, it defines an objective function, which computes the sum of squared differences between the observed data and the predicted values based on the exponential growth model. The function then utilizes optimization techniques to minimize this objective function, effectively estimating the parameters of the exponential model, including the R value. This method employs the Nelder-Mead method for nonlinear optimization. 

An inherent limitation of the current methodology lies in its temporal scope. Despite the redefinition of Lyme Disease in 2008, available data from the CDC spans only the past 16 years, providing an annual record of its incidence across states. Conversely, babesiosis and anaplasmosis are diseases of emerging concern, with data on Babesiosis incidence by state spanning from 2014 to 2020 and Anaplasmosis incidence recorded from 2017 to 2021. Consequently, the estimation of respective ρ values suffers from a degree of statistical underpowering, thereby compromising the precision of our projections. 

The last assumption inherent in this model pertains to the equivalence between disease incidence and the prevalence of corresponding pathogens within tick populations. This assumption implies a consistent frequency of human-tick interactions, and consequently, tick bites on humans, over time therefore, any alteration in pathogen prevalence is presumed to yield a proportional change in disease incidence. It is assumed that state-level incidence data can serve as a surrogate measure for pathogen prevalence within the respective state. In that respect, ρ can be derived from incidence data. 

