# An Exploratory Data Analysis of California Donors to the 2012 Presidential Election

## Executive Summary
Data from the FEC on political contributions from California residents to 2012 presidential candidates was analyzed and visualized. 

**Memo for Republicans**  
Results of Analysis
* Republicans donate at a higher level than democrats across the most common occupations and locations. 
* Contrary to common belief, Republican contributors exist in SF and Silicon Valley in noteworthy numbers. (Ignore Berkeley and Oakland).

Key Takeaways
* Republican politicians can still raise vast sums of money in California just based on the sheer population size and significant number of wealthy individuals. 
* Focus on southern California, especially San Diego and wealthy beach enclaves nearby.

**Memo for Democrats**
Results of Analysis
* What Democratic contributors lack in donation size they make up in population numbers
* Key strongholds are in the Bay Area and Hollywood. 

Key Takeaways
* Court not just the wealthy contributors, but the mass population as well.
* Spend time in the Bay Area and LA. Consider skipping San Diego.

**Future Work** 
Coupling this with demographic data could prove powerful in predicting contributions in future election cycles. 

------------------------------------------------------------------------------------------------

# Data
Data was downloaded from the FEC [through this link](ftp://ftp.fec.gov/FEC/Presidential_Map/2012/P00000001/P00000001-CA.zip). (Direct download of 128 MB zip file. ) Note: one must add a comma after the header  to make it readable in R.

As given, the data is clean. I removed data on Republican primary candidates and negative donation amounts (i.e. were refunded or allocated elsewhere). This affected only a tiny number of donations (far less than 1%).  

I created some variables to help in summarizing the data. For example, the "Republican" variable is a binary variable indicating whether the donation is to the Republican candidate. Similarly, "Democrat Amount" is the amount donated to democrats, therefore defined to be $0 if the money is donated to the Republican. 

# Methods and Analysis
I ran my analysis in R Studio. This was due to the high value placed on packages that are well-developed for R, namely  `ggplot` for graphics and `plyr` for data manipulation. 

In doing my analysis I looked to answer questions about the data in relation to  money donated at the individual  and  aggregate levels. In my analysis, I performed a deep dive  of looking at how donations varied with occupation and city. These factors were chosen because they likely have the most homogeneity within groups of people (e.g., attorneys tend to be similar, people who live in Berkeley tend to be liberal , etc.).  I first looked to understand the  data graphically and then added summary statistics when relevant. 

Some questions I answered:
* Which occupations donate the most money? 
* Do certain occupations tend to donate more to one party vs. the other? 
* Which cities donate the most money in total? Which cities donate the most per contribution?  
* What are the most partisan cities by percentage of donations? Percentage of money donated? 

# Future Work
One of the downsides of this data set is that it is lacking demographic context. Specifically, one needs to know how California compares to the rest of the country and how  these various cities compare amongst themselves. For example, are there more lawyers in San Francisco than NYC? Do they tend  to donate more on average than those in other parts of the country? Without context, it's hard to know what's at the root cause of a trend. With this data, it could often be sheer scale (e.g., Los Angeles has a lot of people), but otherwise there could be unique factors driving numbers. 

Coupling this dataset with 1) demographic data and 2) past examples of this same dataset could prove valuable in building predictive models for future election cycles.  
