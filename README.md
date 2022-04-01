# Election Analysis

## Project Overview

An employee from the Colorado Board of Elections has assigned the task of completing an audit of the results of a recent, local congressional election. He has requested the following:
  - The total number of votes cast.
  - The total votes cast in each county.
  - The percentage of the total vote cast in each county.
  - The county with the largest number of votes cast.
  - A list of all candidates receiving votes.
  - The total votes each candidate received.
  - The percentage of votes each candidate received.
  - The winner of the election based on the popular vote along with their total votes and percentage of the total vote.

## Resources

The raw data can be found in the file: https://github.com/skgolden13/Election_Analysis/blob/main/Resources/election_results.csv

The software used for the analysis was Python 3.6.1 and Visual Studio Code 1.66.0.

The code used to generate the analysis results can be found at: https://github.com/skgolden13/Election_Analysis/blob/main/PyPoll_Challenge.py.py

## Election Audit Results

The code used to generate results on a county basis and on a candidate basis are similar in structure. The only difference is the column referenced for each data set and the variable names used in calculations. The list for each category was initialized and the largest number of votes was initially set to 0. A for loop was used to extract the county or candidate name from the column and determine if the value was included in the vote counter. If a value was not included, it was appended to the data set and the count for that value was initialized as 0. The counter for that value was then increased by 1 for every occurence in the column.

The value for each county or candidate was then compared with the variable containing largest number of votes for each category. The code rewrites the value if the total votes for a county or candidate are greater than the current existing value.

The results for total votes cast, each county, the county with the most votes cast, the results for each candidate, and the results for the winning candidate are then printed in the command window and written to a text file.

The results show that:
  - 369,711 total votes were cast in the election.
  - Votes were cast in 3 counties:
    - Jefferson County: 38,855 votes (10.5% of votes cast.)
    - Denver County: 306,055 votes (82.8% of votes cast.)
    - Arapahoe County: 24,081 votes (6.7% of votes cast.)
  - Denver County had the largest number of votes cast.
  - The candidates receiving votes were:
    - Charles Casper Stockham: 85,213 votes (23.0% of votes cast.)
    - Diana DeGette: 272,892 votes (73.8% of votes cast.)
    - Raymon Anthony Doane: 11,606 votes (3.1% of votes cast.)
  - Diana DeGette won the election with 73.8% of the votes cast and 272,892 total votes.

The resulting text file output from the analysis can be found at: https://github.com/skgolden13/Election_Analysis/blob/main/analysis/election_analysis.txt

## Election Audit Summary

This code could be run for a data set containing the results from multiple elections. A new column in the data set that contains the office each race is for could be used to create a for loop. This for loop would run through each unique elected office and the counties and candidates involved. The curent code would be nested inside this for loop.

This code could also be used to audit the results of a nation wide presidential election. A column would be added that contains the state a vote was cast in. The winner of the popular election in each individual state would then be assigned a value equal to the electoral votes for that state. Counties and congressional districts would need to be evaluated for the states of Maine and Nebraska. These two states assign electoral votes based on the congressional districts won by each candidate. The other 48 states assign electoral votes based on the winner of the popular vote for that state.
