# Assignment-3-Getting-and-Cleaning-Data

# Storm Events Data Analysis README

This repository contains code and instructions for performing data analysis on storm events data and generating visualizations using R.

## Prerequisites

To run the code and replicate the analysis, you will need the following:

- R programming language installed on your system
- Required R packages: tidyverse, ggplot2

## Data Import and Preparation

1. Start by downloading the storm events data file in CSV format. The file should be named "StormEvents_details-ftp_v1.0_d2016_c20220719.csv" and placed in the same directory as the R script.

2. Run the R script and make sure to set the working directory to the location where the data file and the R script are located.

3. The script imports the necessary packages and loads the storm events data using the tidyverse package. It also performs data cleaning and manipulation to prepare it for analysis.

## Data Analysis and Visualization

4. The script limits the dataframe to specific columns of interest, including BEGIN_YEARMONTH, EPISODE_ID, STATE, STATE_FIPS, CZ_NAME, CZ_TYPE, CZ_FIPS, and EVENT_TYPE.

5. The dataframe is then arranged by state name (STATE) using the arrange() function from the tidyverse package.

6. The state and county names are changed to title case using the str_to_title() function from the stringr package.

7. The dataframe is filtered to include only events listed by county FIPS (CZ_TYPE of "C"), and the CZ_TYPE column is removed.

8. The state and county FIPS are padded with a "0" at the beginning using the str_pad() function from the stringr package. The two columns are then united to create a new FIPS column.

9. All column names are converted to lowercase using the rename_all() function from the dplyr package.

10. The script merges the storm events dataframe with the state information dataframe, which includes state name, area, and region.

11. The merged dataframe is further processed to remove any states that are not present in the state information dataframe.

12. Finally, a plot is generated using ggplot2 to visualize the relationship between land area, region, and the number of storm events in 2016.

## Usage

To replicate the analysis, follow these steps:

1. Ensure you have the necessary prerequisites installed.

2. Download the storm events data file and place it in the same directory as the R script.

3. Set the working directory in the R script to the location where the data file and the R script are located.

4. Run the R script to perform the data import, cleaning, analysis, and visualization.

## Troubleshooting

If you encounter any issues or errors during the data analysis process, please check the following:

- Verify that the data file is present in the correct location.
- Ensure that the required R packages are installed.
- Check for any missing or incorrect data in the input file.
- Review the code and make sure all steps and functions are properly implemented.

For further assistance or questions, please reach out to me.

