# Telemetry-Data

## Overview

This code analyzes telemetry data from Formula 1 races using the FastF1 Python library. It processes raw session data (e.g., qualifying or race) to extract and compare driver telemetry such as speed, throttle, and sector times.

The main goal is to provide insightful visualizations of drivers’ on-track performance, helping to understand differences in racing lines, speeds, and lap times.

## Key Features

* **Data Loading:**
  Load session and telemetry data for specified race weekends and sessions (practice, qualifying, race).

* **Driver Selection:**
  Extract telemetry data for one or more drivers by their driver number or code.

* **Data Processing:**
  Clean and align telemetry streams to compare speed, throttle, brake, and delta time between drivers or laps.

* **Visualization:**
  Plot telemetry traces using Plotly for interactive speed and delta time comparison, sector time overlays, and lap-by-lap analysis.

* **Lap Selection:**
  Filter for specific laps (e.g., fastest qualifying laps) to ensure fair comparison.

## Code Walkthrough

1. **Session Initialization:**
   Connect to FastF1 API and load a specific race session by year, Grand Prix name, and session type (e.g., qualifying).

2. **Load Telemetry:**
   For each driver, load telemetry data for the lap(s) of interest using FastF1’s `get_telemetry()` function.

3. **Data Alignment:**
   Synchronize telemetry data streams by distance or time to enable direct driver comparison.

4. **Compute Deltas:**
   Calculate delta times between drivers at every telemetry point to highlight where one driver is faster or slower on track.

5. **Plotting:**
   Create interactive plots showing speed, delta time, and possibly throttle/brake overlays to visualize differences.



## Notes

* The code assumes internet access for FastF1 data download and caching.
* Telemetry data might take time to download on first run.
* Make sure to handle missing or incomplete laps gracefully.


