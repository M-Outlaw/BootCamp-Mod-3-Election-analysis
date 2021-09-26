# BootCamp-Mod-3-Election-analysis
Performing analysis to take in a large number of election votes and determine the outcome of the election.

## Overview of Project

### Purpose
The purpose of this analysis is to use Python and VSC to help Tom, a Colorado Board of Elections employee, perform an election audit of the results of a U.S. Congressional Precinct in Colorado.

## Analysis and Challenges
### Data
The data provided the ballot ID, the county in which the voter lives, and candidate they chose for U.S. Congress for 369,711 votes.

### Winning Candidate
- The first goal of the audit was to determine which candidate had the most votes.
- This included:
  * determining the total number of votes.
  * determining a list of candidates that received votes.
  * determining the total number of votes for each candidate.
  * determining the percentage of votes for each candidate.
  * determining the winner of the election based on the popular vote.

### Python Code
#### Advantages
- The great thing about python code is that it reads the votes from a csv file, so this code would work and calculate the winner of any election as long as the csv file is set up as ballot ID, county (or this could be by state), and then the candidate voted for.
- The other great thing is that python can write to files, so it conviently creates a file that can be easily understood and shared.

#### Counting Votes
- A for loop was used to create:
  * the total count.
  * the list of candidates that received votes.
  * the total number of votes for each candidate.
- A second for loop was used to determine the percentage of votes for each candidate and print out the number and percentage of votes for each candidate

#### Counting Counties


<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-3-Election-analysis/blob/main/Resources/PyPoll_Challenge_Terminal_Output.png" width="800" height="496"/></p>

<img src="https://github.com/M-Outlaw/BootCamp-Mod-2-Stock-Analysis/blob/main/Resources/Stocks_2017.png" width="342" height="344"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://github.com/M-Outlaw/BootCamp-Mod-2-Stock-Analysis/blob/main/Resources/Stocks_2018.png" width="342" height="344"/></p>

### Challenges and Difficulties Encountered
- In refactoring the code, initially it would not run because I continued to receive an overflow error for the return values. I was confused by this and tried to use the CLng() function to help with this, however the error continued.

- After debugging the code, I figured out that the if statements for the starting and ending prices were missing the second conditional. Once that was fixed, everything ran very smoothly.

## Results
### Further Analysis
- To further analyze the data to determine which stock performed the best over the two years, the percent increase from 2017 to 2018 for both the total daily volume and return were determined and is shown below.
  * Seven of the stocks had a positive percent increase for their total daily volume.
  * However, only one stock (RUN) had a positive percent increase for their return.

<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-2-Stock-Analysis/blob/main/Resources/Stock_2017_to_2018_Comparison.png" width="411" height="359"/>

### Recommendation
- My recommendation is for Steve to recommend that his parents invest in RUN.
  * RUN had a positive return for both 2017 and 2018.
  * RUN had a positive percent increase for both total daily volume and return between 2017 and 2018.

### Refactoring
#### Advantage
- A great advantage of refactoring the code is greater efficiency in running your codes, especially when the code will be used again in the future.
  * Refactoring the code for my original VBA script greatly enhanced the code, because this can be used for future years of stock and include many more stocks. The added efficiency will really help when the data is increased to accommodate the additional years and stocks.

- Another advantage is that refactoring allows you to re-evaluate your code to ensure that everything is running correctly and that you haven't forgotten any nuances that could be included to better enhance your analysis.
  * Refactoring the code allowed me to put all of the parts together. The original code had the results and formatting in different subdirectories, required the user to run two different codes. Now they are all in one.
  
#### Disadvantage
- One disadvantage of refactoring the code is the amount of time taken to redo code that does work, even though it is slow, and it is possible to introduce errors that were not in the original code.
  * As discussed in the challenges, I did introduce an error in my code while refactoring. It was corrected, but it did take a bit of time to determine what the error was.





The written analysis has the following:

Overview of Election Audit

The purpose of this election analysis audit is well defined. (3 pt)
Election Audit Results

There is a bulleted list where each election outcome is addressed. (7 pt)
Election Audit Summary

There is a statement to the election commission that explores how this script can be used for any election, with two examples for modifying the script. (4 pt)
