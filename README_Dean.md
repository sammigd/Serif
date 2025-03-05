## Overview of approach
I followed the modeling mantra "garbage in, garbage out" and spent a lot of my allotted 
time making sure I understood the variables in the input data sets and how they might 
fit together. I probably could have spent days on this alone if I wanted to! I made 
a quick and dirty data dictionary, which I referred back to many times while trying 
to decide how to fit these data sets together. I did some data cleaning and then 
sought to understand the most granular level of data available in each of the data 
sets. Once I aggregated results down to the hospital, payer, plan, code, code type 
and care setting level, I had a single value for most hospital rates and a distribution 
of possible values for rates from the TIC data. Ideally, I would have been able to 
further select down to a more specific set of possible TIC values, but in the time 
allotted I decided the most principled approach was to present side by side the 
hospital level HPT rates and the corresponding distribution of values from the TIC
data, allowing for comparisons between the hospital rates and the median TIC rate. 
Future steps would focus on improving mapping between care settings, provider types, 
and other rate-relevant features of the two data sets. 

## Directory of files
- DS_README.md - instructions for data science take home
- README_Dean.md - description of Samantha Dean take home response
- DeanTakeHome.Rmd - markdown with code and comments
- DeanTakeHome.html - rendered version of DeanTakeHome.Rmd
- rawdata folder - contains original TIC and HPT data downloads
    - hpt_extract_20250213.csv - raw data from HPT
    - tic_extract_20250213.csv - raw data from TIC
- outputdata folder - contains output data sets
    - output_all.csv - dataset including all hospital/payer/code/codetype combos 
    present in at least one input dataset
    - output_overlap.csv - dataset including hospital/payer/code/codetype combos 
    present in both input datasets
- datadicts - csv's with data dictionaries for each input and output dataset
    - hpt_datadict.csv
    - tic_datadict.csv
    - outputs_datadict.csv

## Instructions for running code
To run the code, I recommend you have R and RStudio installed. You will need to 
install the R markdown package (https://rmarkdown.rstudio.com/authoring_quick_tour.html). 
Check that the working directory is set to the parent folder of the script. Then 
you should be able to run the DeanTakeHome.Rmd file to generate 1) output_all.csv 
2) output_overlap.csv and 3) DeanTakeHome.html.

I have already run the code and included these outputs in the git repo for convenience.

## Other notes
I documented my workflow within the RMarkdown document with my code. Without running 
any code, you can open up the file DeanTakeHome.html to see my code and commentary. 