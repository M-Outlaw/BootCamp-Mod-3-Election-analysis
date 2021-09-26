# BootCamp-Mod-3-Election-analysis
Performing analysis to take in a large number of election votes and determine the outcome of the election.

## Overview of Project
### Purpose
The purpose of this analysis is to use Python and VSC to help Tom, a Colorado Board of Elections employee, perform an election audit of the results of a U.S. Congressional election for a precinct in Colorado.

## Analysis and Challenges
### Data
The data provided the ballot ID, the county in which the voter lives, and the candidate they chose for U.S. Congress for 369,711 votes.

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
- The other great thing is that python can write to files, so it conveniently creates a file that can be easily understood and shared.

#### Counting Votes
- A "for" loop was used to create:
  * the total count.
  * the list of candidates that received votes.
  * the total number of votes for each candidate.
- A second "for" loop was used to determine the percentage of votes for each candidate and print out the number and percentage of votes for each candidate
- After running through the loops to gather all of the votes, the code output the winner of the election based on both the number of votes and the percentage of votes
- Below is an image of the election output.

<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-3-Election-analysis/blob/main/Resources/PyPoll_Challenge_Output_without_county.png" width="740" height="360"/></p>

#### Counting Counties
- After the audit successfully determined the winner of the election, the election commission requested additional information to conclude the audit.
  * The number of voters from each county.
  * The percentage of voters from each county.
  * The county with the highest number of voters.
- The process for this was very similar to counting the votes.
  * The difference was to count the votes based on the county instead of the candidate.
- This information was placed below the total votes and the breakdown of how the each candidate did in the code output, since the final conclusion the board of Elections needs is the winner with the total number of votes and the percentage of votes they received.

<p align="center"><img src="https://github.com/M-Outlaw/BootCamp-Mod-3-Election-analysis/blob/main/Resources/PyPoll_Challenge_Terminal_Output.png" width="800" height="496"/></p>

#### Text File
- After the audit was complete, the code output was written and saved to a new file so that there was a document of the winner and that the winner could be shared through various medias.

The generated text file can be viewed [here](https://github.com/M-Outlaw/BootCamp-Mod-3-Election-analysis/blob/main/analysis/election_analysis.txt).


### Challenges and Difficulties Encountered
- When I ran the code initially in the interactive window, it ran without any errors and the output was correct. However, when I went to run the code in the terminal, it kept returning an error and would not run.
  * In figuring out the problem, I realized that I had not set the path of the terminal to the correct folder causing an error in the code because it could not access the files to read or write to.
  * This was a really good reminder to me that when the terminal shuts down it resets to open back up in the home directory and not the folder the terminal was last in.

## Election-Audit Results
- The total number of voted received for this congressional election was 369,711 votes.
- The number of votes for each county was as follows:
  * Jefferson county had 38,855 voters and generated 10.5% of the votes.
  * Denver county had 306,055 voters and generated 82.8% of the votes.
  * Arapahoe county had 24,801 voters and generated 6.7% of the votes.
- Denver by far had the largest turnout of voters, which is interesting since the counties are fairly evenly populated. 
  * Denver county as of July 1, 2019 had a population estimate of 727,211 people.
  * Arapahoe county as of July 1, 2019 had a population estimate of 656,590 people.
  * Jefferson county as of July 1, 2019 had a population estimate of 582,881 people.
   - Information was taken from [census.gov](https://www.census.gov/quickfacts/fact/table/denvercountycolorado,arapahoecountycolorado,jeffersoncountycolorado/LFE305219).
- The number of votes for each county was a follows: 
  * Charles Casper Stocham received 85,213 votes corresponding to 23.0% of the votes.
  * Diana DeGette received 272,892 votes corresponding to 73.8% of the votes.
  * Raymon Anthony Doane received 11,606 votes corresponding to 3.1% of the votes.
- Diana DeGette by far received the most votes with 272,892 votes, which was 73.8% of the votes.

- **Note:** If the candidate percentages are totaled, it only equates to 99.9% of the votes. This is not an error and is not an issue for concern. It is a product of rounding for the output to look cleaner. If the rounding were taken off, the percentages would total to exactly 100%.

## Election-Audit Summary
- In summary, this Python code provided accurate information about this U.S. Congressional election for a precinct in Colorado. Through a few easy changes the code can be changed to work for any election.
- The easiest way to alter the code to audit a different election is to make sure that csv file containing all the votes is set up in 3 columns with ballot id in the first column, county in the second column, and candidate in the third column. Then the file path just needs to change to read this file.
- Another way to alter the code to audit a different election if the csv file is not set up in the same format, is change which columns the code picks up for the county and candidate.
  * On line 48, change "candidate_name = row[2]" to "candidate_name = row[column index of the candidates]".
  * On line 51, change "county_name = row[1]" to "county_name = row[column index of the candidates]".
- A third way to alter the code to audit a national election is to do a find and replace and change all instances of county to state.
![image](https://user-images.githubusercontent.com/89364082/134795258-dfe70d6e-f53a-477f-9c78-d208039691b4.png)
