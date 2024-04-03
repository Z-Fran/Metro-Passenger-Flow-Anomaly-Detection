# Metro-Passenger-Flow-Anomaly-Detection
Reimplemention and improvement of the paper "[Real-Time Passenger Flow Anomaly Detection Considering Typical Time Series Clustered Characteristics at Metro Stations](https://ascelibrary.org/doi/abs/10.1061/JTEPBS.0000333)"

## Dataset

The AFC system records the number of passengers who are inbound to and outbound from stations. The passenger flow dataset collected from a metro station during 402 days, are utilized. The AFC data were collected at 5-min intervals.

Due to the varying operating hours of metro stations on different dates, in order to ensure unification of data, using daily data from 6:00 to 23:00.

The following figtures show the curves of the passenger flow data.

<div align=center>
<img src="./resources/all_inbound_flow.jpg"/>
</div>

<div align=center>
<img src="./resources/all_outbound_flow.jpg"/>
</div>

<div align=center>
<img src="./resources/all_total_flow.jpg"/>
</div>

> The dataset is not public.

## Data pre-processing

### Remove abnormal data

Find abnormal data by clustering, and then we investigate the reason.
+ 20210418: A marathon race was held.
+ 20210701: A big event was held.
+ 20210726: Typhoon.
+ 20220129,20220130,20210210: Approaching important festivals

The following figtures show the curves of abnormal passenger flow data.

<div align=center>
<img src="./resources/abnormal_in_flow.jpg"/>
</div>

<div align=center>
<img src="./resources/abnormal_out_flow.jpg"/>
</div>

<div align=center>
<img src="./resources/abnormal_total_flow.jpg"/>
</div>

After removing, the dataset consists of 396 days of data and 205 pieces of data every day.

### Moving average smoothing

Use moving averages to smooth data.

The following figtures show the curves of the smoothed data.

<div align=center>
<img src="./resources/smoothed_in_flow.jpg"/>
</div>

<div align=center>
<img src="./resources/smoothed_out_flow.jpg"/>
</div>

<div align=center>
<img src="./resources/smoothed_total_flow.jpg"/>
</div>

The following figture compares the original data and the smoothed data on a certain day.

<div align=center>
<img src="./resources/compare_smoothed.jpg"/>
</div>

## Methodology
### Overall
