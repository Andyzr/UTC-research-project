Table of contents
* TOC
{:toc}
## Introduction 


This page is used to document the data sets used and produced in the University Transportation Centers (UTC) project: [Proactive management of mobility impact of interdependent subsurface utility and roadway construction through incentives](https://ppms.cit.cmu.edu/projects/detail/198).


## Documentation
This section documented the input (raw data) and output (processed data) of the models proposed in this study.
### Raw data

The following items are raw data sets used in this research project. 

1. Records of traffic crashes in Pennsylvania during 2015 - 2017 [(link)](https://pennshare.maps.arcgis.com/apps/webappviewer/index.html?id=8fdbf046e36e41649bbfd9d7dd7c7e7e).
2. Observations of hourly weather conditions in Pennsylvania during 2015 - 2017 from Federal aviation administration stations [(link)](http://climate.met.psu.edu/data/ida/).
3. Roadway network information of Pennsylvania from the Pennsylvania Department of Transportation (PennDOT) [(link)](https://data-pennshare.opendata.arcgis.com/datasets/rmsseg-state-roads).
4. Records of road incidents in Pennsylvania during 2015 - 2017 from the Road Condition Reporting System of PennDOT [(link)](http://www.penndot.gov/Doing-Business/OnlineServices/Pages/Developer-Resources-DocumentationAPI.aspx).
5. Records of hourly traffic speed for roadway segments in Pennsylvania during 2015 - 2017 from the INRIX company [(link)](https://inrix.com/products/speed/).

### Processed data
The following items are processed data produced in this research project.

- **Records of work zones in Pennsylvania and corresponding control group**

In this study, we identified 5,352 work zones occurred in roadway network of Pennsylvania from 2015 to 2017. The beginning and ending locations of each work zone are located on high-granular road segments. The localization errors of work zone is at the magnitude of meters. The beginning and ending time of each work zone is at the magnitude of minutes.

For each work zone, we capture control groups as a series of observations on the same road segment(s) of work zone on the same period of weeks before and after the week of roadwork. For instance, assume there is a work zone perform during Monday, May 14th, 1 pm – 5 pm. The control groups would include observations on the same road segments of the work zone during Monday, May 7th, 1 pm – 5 pm (one week before the roadwork) and May 21st, 1 pm-5 pm (one week after the roadwork), Monday, April 30th, 1 pm – 5 pm (two weeks before the roadwork) and May 28st, 1 pm-5 pm (two weeks after the roadwork),…. 1 pm -5 pm at M weeks before the roadwork and 1 pm – 5 pm at m weeks after the roadwork. Here we denote M as the maximum number of weeks before or after the week of roadwork captured. In this study, we set M =10. In other words, the control groups are the observations on the same road segment(s) of the 5,352 work zones on the same period of weeks from ten weeks before the week of roadwork and ten weeks after the week of roadwork.  

For each work zone and each control case, we divide each period into smaller periods that have durations of thirty minutes. This high temporal resolution setting of data permits us capturing the fast-changing traffic conditions and weather conditions.

For each thirty-minute period in each work zone and control case, we capture the following variables as one complete observation: the corresponding deployment configurations,  crash occurrence , weather conditions, traffic speed, and roadway characteristics. The details of these variables will be illustrated in the following part. 

- **Work zone deployment configurations**

The deployment configurations for each thirty-minute period in each work zone and control cases include duration of the work zone (in seconds), length of the work zone (in meters), whether the studied period is on weekdays (from Monday to Friday), whether the studied period is during daytime (from 6 AM to 6 PM), and whether the corresponding work zone is full closed (instead of partially closed). 

- **Crash occurrence**

For each thirty-minute period in each work zone and control cases, the crash occurrence is a binary variable indicating whether there is a crash occurred in the investigated period at the corresponding road segment(s).

- **Weather conditions**

For each thirty-minute period in each work zone and control cases, the weather conditions in the processed data set include the hourly average wind speed (in mile per hour), the hourly average temperature (in Fahrenheit scale), and the hourly average precipitation (in inch).


- **Traffic speed**

For each thirty-minute period in each work zone and control cases, the traffic speed in the processed data set is the average traffic speed from 210 min to 30 min before the start of investigated period and from the nearest Traffic Message Channel (TMC) segments.

- **Roadway characteristics**

For each thirty-minute period in each work zone and control cases, the roadway characteristics include annual average daily traffic (AADT), number of lanes on the roadway, speed limit, number of intersections within the given road segments, and whether the road segment is identified as major roads on National Highway System (NHS).


## People
**Principal Investigators:** Burcu Akinci, Sean Qian

**Student:** Zhuoran Zhang
## Copyright
MIT License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 

## Acknowledgement
This project is funded in part by Traffic 21 Institute, Carnegie Mellon University’s Mobility21, and US Department of Transportation. The contents of this project reflect the views of the authors, who are responsible for the facts and the accuracy of the information presented herein. The U.S. Government assumes no liability for the contents or use thereof.


