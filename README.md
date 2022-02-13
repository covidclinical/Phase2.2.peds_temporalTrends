# Temporal trends of distinct phenotypes in the children population comparing before and during pandemic
Analysis of phecodes trends in the children population.

## Data
Analysis developed with the aim of using an extension of the 2.2 4CE consortium data, the "AllAdm" cohort that contains all the children population from January 2019 with the aim of comparing phenotype trends before and during pandemic.

## Repo organization
- `R/`: contains the files carrying out the analysis
- `public-data/: contains the phecode-icd mapping file
- `output`: location of the files saved with by the analysis 

## How to run this code?
First, clone the repository: git clone 

Then open the file temporal_trends.Rmd and go to the section “Variables that need to be checked/modified by each site”:
- change the folder_4ce_files to the directory where your phase 2.2 "AllAdm" data is located
- determine the obfuscation threshold: 
    - obfuscation = FALSE if no obfuscation
    - the numeric value of the obfuscation threshold if any; e.g. obfuscation = 3
    Make sure you comment the existing obfuscation line, set up as FALSE
- specify if the race information is collected or not at your site (raceAvailable: set up as TRUE or FALSE)
- change the dateFormat to the one followed in your site (e.g., if your date looks like 03-AUG-20 follows the format "%d-%b-%y"). Further details about how to specificy the format below:

%d day as a number (0-31)	01-31
%a abbreviated weekday (e.g., Mon )
%A unabbreviated weekday (e.g, Monday)
%m	month (00-12)	00-12
%b abbreviated month (e.g, Jan)
%B unabbreviated month (e.g, January)
%y 2-digit year (e.g., 07)
%Y 4-digit year (e.g., 2007)


After all these changes are done, run the temporal_trends.Rmd, as an output an html file named: temporal_trends.html and an RData file will be generated in the output folder. 
