## 1 NYPD-911-Calls-Analysis-
This is an analysis of NYPD 911 call data (2023–2024) to identify workload imbalances and inefficiencies in emergency response. Using KPIs and Tableau dashboards, it highlights non-criminal call volume, peak patterns, and borough disparities to support smarter resource allocation and planning.

## 2. Objective
a. Identify patterns in NYPD-handled 911 calls
b. Determine which calls require non-police responders
c. Support budget planning decisions
d. Reduce NYPD workload by diverting non-criminal calls
e. Improve coordination across responder agencies (NYPD, FDNY, EMS, etc.)

## 3. Dataset
https://data.cityofnewyork.us/Public-Safety/NYPD-Calls-for-Service-Historic , 
Focusing on 2023-2024 , 
15 million columns , 
Key Fields-CAD_EVNT_ID,INCIDENT_DATE,INCIDENT_TIME,BORO_NM,PATRL_BORO_NM,GEO_CD_X,GEO_CD_Y,TYP_DESC,CIP_JOBS,DISP_TS,CLOSNG_TS,Latitude, Longitude

## 4. Data Cleaning & Preparation
Column titles were revised for clarity and relevance, and call descriptions were similarly updated. Duplicate entries were removed, as were columns containing incomplete or non-essential data for the analysis. Incident date and incident time were consolidated into a single datetime field to facilitate more detailed temporal analysis (year, month, week, day, hour). Calculated fields were created, including handling time (derived from dispatch and closing times), and CIP_JOBS were utilized to categorize the nature of each call.

## 5. Key KPIs
- Total call volume
- Non-criminal vs criminal ratio
- Peak hour
- Borough workload comparison
- Handling time proxy
- Load index

## 6. Key Insights
Borough with highest call volume ,
Call types with highest frequency ,
Response time variations ,
Peak call hours and months ,
Percentage of repeat callers ,
Workload distribution across patrol boroughs

## 8. Tools Used
Tableau 

## Recommendations
The analysis supports the implementation of a Multi-Agency Response System (MARS) to improve operational efficiency by diverting wellness checks, domestic incidents, and other low risk calls to EMS, social services, or trained community response teams where appropriate. A complementary community awareness campaign could help educate residents on the appropriate use of 311 versus 911, reducing unnecessary emergency dispatches. Resource allocation should be adjusted to reflect demand patterns, including redistributing officers or adding patrol capacity in high demand boroughs such as the Bronx. Staffing schedules should also be aligned with identified hourly and seasonal peak periods to better match service demand. Operational improvements could focus on reducing bottlenecks associated with high duration call types, as well as streamlining processes such as rotational towing and suspect holding through AI enabled triaging systems to improve workflow efficiency and response times.

## 10. Limitations
-Limited Time Coverage: The dataset contains complete information only for 2023–2024. Data for 2025 was not available at the time of analysis, limiting the ability to evaluate longer-term trends or recent changes in call patterns.
-No Call Pickup Time Data: The dataset does not include information on call answer or dispatcher pickup times. As a result, it was not possible to assess caller wait times or evaluate call center responsiveness.
-Inaccurate Call Duration Proxy: The dataset does not provide a definitive timestamp for when an incident was fully resolved. Analysis relied on the reported closing time as a proxy, which may not accurately reflect the true duration of the incident.
-Operational Context Missing: The dataset lacks information on staffing levels, unit availability, and resource deployment, limiting the ability to directly attribute workload imbalances to operational constraints.
-Computational Constraints: The dataset contains millions of records, which created memory and performance limitations when processing on a personal computer. Full dataset loading caused system freezes and tool instability. As a result, data processing required aggregation, sampling, and memory-optimized workflows to ensure successful analysis.

## 11. Future Improvements
Forecasting-Predict future call volume to support staffing and budget planning.
Anomaly detection-Identify unusual spikes or drops in call activity.
Predictive modeling-Predict characteristics of future incidents or operational outcomes
