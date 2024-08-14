# Bigfoot, Big Data

Contributors: Kat Chu, Quinn Daley, Mackenzie Deets, Oumar Diakite, Jacob Woolley

## Project Summary
Bigfoot sightings are bizarre but common stories found in tabloids and campfire stories across America, but where and when and how to these mysterious sightings occur?
We sought to use the techniques and methods taught to us in class to analyze data from the Bigfoot Field Reaserchers Organization (BFRO) to make some key analyses broken down by time, location, and weather.

We approached this collaborative effort by independently doing analysis on one or two broader questions each, and coming together at the end to combine our results.

## Project Analysis

### Summary


### Kat
In this section, I explore how Sasquatch sightings are distributed across the different regions of the United States. I processed the bfro_reports_geocoded.csv dataset by focusing on the state and classification columns and assigned states to one of four regions: West, Midwest, South, or Northeast. This involved creating a custom function to map states to regions, which I then applied to the dataset to generate a new region column.

During this process, I encountered several challenges. Some data points were incorrectly categorized as 'Other' due to errors in the state assignments. To address this, I reviewed and corrected the region assignment function. Additionally, I faced difficulties with converting the region_classification_counts Series into a DataFrame and ensuring accurate graph references for visualization. I resolved these issues by carefully checking the region assignments and properly transforming the Series into DataFrames to maintain data integrity.

My analysis reveals that the West and South are hotspots for Sasquatch activity, especially with the most credible sightings, while the Midwest shows a more balanced distribution. The Northeast, however, has far fewer reports, suggesting that Sasquatch encounters are much rarer in this region. This data highlights the geographic spread of sightings and raises intriguing questions about why certain areas seem more conducive to Sasquatch sightings than others. Such as the variety of terrain and geography may be more condusive than others to the theory of Bigfoot. 

### Quinn
In this section, we wanted to understand the overall number of Bigfoot sightings by year, focusing on how the number of reports has evolved over the years in respect to  differences in sighting types to gain deeper insights into the nature and timing of these reports. The code reads in JSON and CSV data files using Pandas, then displays the first few rows to preview. From there, the data was cleaned  by dropping NaN values in the 'YEAR' column, converting the 'YEAR' to an integer, and filtering the data for valid years. The code then groups the data by 'YEAR' and 'REPORT_CLASS', counts the occurrences, and pivots the data for plotting. Finally, it plots the number of Bigfoot sightings by year and report class using ,atplotlib, saving the plot as a PNG file. The figure that was created by the code illustrates the trends in Bigfoot sightings over time, categorized by different types of reports, allowing us to explore how these sightings have changed and varied across different classes over the years.

### Mackenzie
In this section, we wanted to show the distribution of sightings throughout the months of the year and the different seasons to see if there was a correlation between the time of year and the number of sightings of Bigfoot. I very little issue in cleaning the data and putting into a bar chart. The biggest challenge I had was to putting the months into chronological order based on the calendar year, which was easily found on StackOverflow. I did also have to debug on ChatGPT.

### Oumar


### Jacob
I was tasked with making analyses on the weather conditions during sightings. I began by reducing the geocoded data to only relevent columns and cleaning the data of rows with missing values. Columns with excessive amounts of missing data were excised entirely as to keep the data set at a suitable size.

My first analysis would be on the condition of the weather (e.g rain, snow, overcast) on sightings as maybe more hazy weather would make people easier to confuse something innocuous for a sasquatch. I did this by first relabeling the many listed conditions down to five based on the most extreme condition listed. (Snow > Rain > Overcast) and putting these in a bar chart which revealed rain to be the most common weather and overcast without precipitation to be the least common.

Then I decided to do a linear regression on cloud cover versus visibility to see if weather was impacting peoples perception as much as I expected. After doing so and charting it, I found no significant relationship between the two. I then decided to seperate the data points on this scatter chart by classification, but this also showed no obvious pattern.

Finally, I decided to run T-tests on some key conditions between Class A and Class B to see if weather would impact people's confidence in their sightings. I found that only humidity, cloud cover, and barometric pressure showed any significant difference, and when comparing summary stats, found that Class A was  slightly higher across all three categories.

## Credits

Original data from BFRO.net

Initial data scrape and project inspiration by Timothy Renner: https://data.world/timothyrenner/bfro-sightings-data

https://www.cdc.gov/nchs/hus/sources-definitions/geographic-region.htm

