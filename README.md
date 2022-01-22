# Election Analysis

## Project Overview
A Colorado Board of Elections has requested an election audit of a recent local congressional election. The results were submitted and the election commission has requested additional data.

The original request included:
1. Calculate total votes
2. Calculate the total votes and percentage of overall votes for each candidate
3. Declare the election winner based on their winning vote count and winning percentage of overall votes

The additional data request included:
1. Calculate county total votes and percentage of total overall votes
2. Determine the county with the largest turnout

## Resources
- Data source: election_results.csv
- Software: Python 3.9.7, Visual Studio Code 1.63.2

## Election Audit Results
The analysis of the election shows that:
- There were 369,711 total votes cast in the election
- The county breakdown is as follows:  
    ![County_Breakdown](/Resources/county_breakdown.png)
- The county with the largest number of votes was Denver
- The candidate results were:
    - Charles Casper Stockham received 23.0% of the votes with 85,213 total votes
    - Diana Degette received 73.8% of the votes with 272,892 total votes
    - Raymon Anthony Doane received 3.1% of the votes with 11,606 total votes
- The winner of the election was Diana Degette with 272,892 votes, a landslide 73.8% of the total votes

## Election Audit Summary
The script used in this election audit can grow or be modified as needed to accommodate additional elections. The possibilities are nearly endless. The current script analyzes counties and candidate totals.

One example of a modification that could be made would be to accommodate a single county election.  In this case the total votes would represent votes for the specific county.  The references to county in the code could be updated to provide insight into district turnout within the county.

The following list and dictionary could be edited to switch names from "county" to "district":
```
county_list = []
county_votes_dict = {}
```
The IF statement below would also need to be modified to represent the districts:
```
if county_name not in county_list:
    county_list.append(county_name)
    county_votes_dict[county_name] = 0
county_votes_dict[county_name] += 1
```
Other changes where county is referenced, such as the print to terminal or results would follow suit, and the code would be ready to analyze smaller county elections with district turnout detail.

Similarly, this code could be updated to audit a city election with modifications to the names of variables, lists, dictionaries, and outputs.  In this case you would want to just comment out or delete any of the code referencing counties since you wouldn't need a finer detail to the turnout.  You'd be left with a more basic code that could help audit the results of a mayoral election.