steel-plant-energy-dashboard
Interactive Power BI dashboard for steel pant energy consumption


An interactive Power BI dashboard for exploring electricity consumption patterns in a steel manufacturing facility using operational time-series data.

Dashboard Preview

![Steel Plant Energy Consumption Dashboard](Screenshot%202026-11-05%20143517.png)


 Project Overview

Energy consumption is an important operational metric in energy-intensive manufacturing. Understanding how electricity usage varies across load categories, time periods, and weekdays versus weekends can help support operational monitoring and energy management.

This project uses Power BI to analyze and visualize steel-industry energy consumption data collected at 15-minute intervals.

The dashboard provides an interactive overview of energy usage, load categories, power factor, and temporal consumption patterns.

 Dashboard Features

KPI Cards
  - Total Energy Consumption (kWh)
  - Peak 15-Minute Energy Consumption (kWh)
  - Average Lagging Power Factor
  - Total Number of Records

  Energy Consumption by Load Type
  - Compares energy usage across Light, Medium, and Maximum Load categories.

- Average Daily Energy: Weekday vs Weekend
  - Compares average total daily energy consumption across weekdays and weekends.

  Monthly Energy Consumption Trend
  - Visualizes changes in monthly energy consumption over the observed period.

- Interactive Filters
  - Date range slicer
  - Load Type slicer

Key Metrics

| Metric | Definition |
|---|---|
| Total Energy Consumption | Sum of `Usage_kWh` across the selected observations |
| Peak 15-Minute Energy Consumption | Maximum observed `Usage_kWh` value |
| Average Power Factor | Mean of `Lagging_Current_Power_Factor` |
| Total Records | Number of observations in the selected data |
| Average Daily Energy | Average of daily aggregated energy consumption |

Dataset

Source:UCI Machine Learning Repository — Steel Industry Energy Consumption

Dataset: [UCI Steel Industry Energy Consumption](https://archive.ics.uci.edu/dataset/851/steel+industry+energy+consumption)

The dataset contains 35,040 records collected from DAEWOO Steel Co. Ltd. in Gwangyang, South Korea. The data consists of 15-minute interval measurements covering 2018.

Selected Variables

| Variable | Description |
|---|---|
| `date` | Date and time of observation |
| `Usage_kWh` | Industry energy consumption |
| `Lagging_Current_Reactive.Power_kVarh` | Lagging current reactive power |
| `Leading_Current_Reactive_Power_kVarh` | Leading current reactive power |
| `CO2(tCO2)` | CO₂-related measurement in the source dataset |
| `Lagging_Current_Power_Factor` | Lagging current power factor |
| `Leading_Current_Power_Factor` | Leading current power factor |
| `NSM` | Number of seconds from midnight |
| `WeekStatus` | Weekday or Weekend classification |
| `Day_of_week` | Day of the week |
| `Load_Type` | Light Load, Medium Load, or Maximum Load |

Tools & Skills

- Microsoft Power BI
- Power Query
- DAX
- Data Cleaning and Transformation
- Data Visualization
- KPI Design
- Time-Series Analysis
- Descriptive Analytics

 Data Preparation & Analysis

The project involved:

- Importing and transforming the source CSV data in Power Query.
- Parsing the timestamp field for temporal analysis.
- Creating DAX measures for energy consumption, power factor, record counts, and peak interval consumption.
- Creating a date-only column to aggregate observations at the calendar-day level.
- Developing an average daily energy measure for weekday/weekend comparisons.
- Building interactive visuals and slicers for exploratory analysis.

Limitations

- The dataset represents a steel manufacturing facility in South Korea; the results should not be generalized to other plants without further validation.
- The dashboard is descriptive and does not establish causal relationships.
- The monthly trend represents aggregated energy consumption, which can be influenced by the number of observed days in each month.
- The dashboard is not a forecasting or optimization model.

 Repository Structure

```text
steel-plant-energy-dashboard/
│
├── dashboard/
│   └── Steel_Plant_Energy_Consumption.pbix
│
├── screenshots/
│   └── dashboard.png
│
└── README.md
```

Dataset Citation

V. E. Sathishkumar, C. Shin, and Y. Cho (2021). *Steel Industry Energy Consumption*. UCI Machine Learning Repository. https://doi.org/10.24432/C52G8C.

Dataset license: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

---


