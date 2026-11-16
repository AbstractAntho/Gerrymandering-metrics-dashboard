# California Congressional Redistricting Dashboard

**[View the live dashboard](https://merry-cajeta-29af86.netlify.app)**  
Open the **Metrics** tab to compare the two maps.

## Overview

How might California’s 2024 congressional election results have changed under
the district boundaries adopted through Proposition 50?

This interactive dashboard uses R and Quarto to compare the map used in 2024
with the new congressional map. It compares estimated seat totals and two
measures of partisan advantage: the efficiency gap and the mean–median
difference in district vote shares.

## Data sources

| Source | What it provides |
| --- | --- |
| [California Statewide Database — November 2024 General Election](https://statewidedatabase.org/d20/g24.html) | Congressional vote counts compiled from county election returns and organized into standardized precinct records. These are the main inputs to the analysis. |
| Official 2024 congressional results by district | A district-level benchmark for checking the totals aggregated from precinct records. |
| [California Statewide Database — Geographic Conversion Files](https://statewidedatabase.org/d20/g24_geo_conv.html) | A crosswalk linking 2024 precincts to 2020 Census blocks, with voter registration counts used to estimate how votes were distributed within each precinct. |
| [California State Assembly — AB 604 Congressional Map](https://aelc.assembly.ca.gov/proposed-congressional-map) | The block-to-district assignments and boundary files for the new map. |
| [U.S. Census Bureau — 119th Congress District Boundaries](https://www2.census.gov/geo/tiger/GENZ2024/shp/cb_2024_us_cd119_500k.zip) | The district boundaries used to display the map in effect for the 2024 election. |

## Method

I cleaned the precinct returns, tracked excluded records, and checked
aggregated vote totals against official district results. I then used voter
registration counts to allocate a share of each precinct’s votes to its
Census blocks and summed those estimates within the new districts.

The comparison holds 2024 voting behavior fixed. Because the source reports
votes at the precinct level, the block-level allocations are estimates.
