# election_analysis

## Project Overview
The purpose of this project was to take a CSV document containing voting records, and help Seth and Tom determine the election results. The desired results were the total number of votes, a summary of the county results, the county with the largest voter turnout, a summary of the candidate results, and the winner of the election. In order to perform this analysis, I wrote a python script to read the data in the CSV document and calculate the results.The purpose of this project was to take a CSV document containing voting records, and help Seth and Tom determine the election results. The desired results were the total number of votes, a summary of the county results, the county with the largest voter turnout, a summary of the candidate results, and the winner of the election. In order to perform this analysis, I wrote a python script to read the data in the CSV document and calculate the results.

## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1, Visual Sudio Code, 1.38.1

## Election-Audit Results

The results of the election are as follows:

•	There was a total of 369,711 votes cast in the election. This was determined by using a for loop to cycle through all of the rows in the CSV document, increasing the total vote count by 1 every time there was data in a row. See below the section of code that performs this calculation.

<img width="249" alt="Total_votes" src="https://user-images.githubusercontent.com/88349443/132954744-550b8416-987a-4c59-915a-5fd975ce2e47.png">

•	The breakdown of the votes per county is outlined below. It includes the county name, the percent of the total votes each county contributed, and the total number of votes cast in each county. 
  o	Jefferson: 10.5% (38,855)
  o	Denver: 82.8% (306,055)
  o	Arapahoe: 6.7% (24,801)
Below is a snapshot of both the section of code that calculates the number of votes per county, as well as the calculation for determining the percentage of total votes per county.

<img width="466" alt="County_votes" src="https://user-images.githubusercontent.com/88349443/132954750-d2efb8d9-41d8-45de-a08a-24a39e300152.png">
<img width="501" alt="County_votes_percentage" src="https://user-images.githubusercontent.com/88349443/132954752-eeb57413-7b89-48a9-b523-e3fa0437db25.png">

•	Denver County cast the largest number of votes by far at 306,055. You can see here the if statement that I wrote to determine which county cast the largest number of votes.

<img width="619" alt="Largest_county" src="https://user-images.githubusercontent.com/88349443/132954756-631e5f77-f2d7-4918-8493-2e8122d56c8b.png">

•	The breakdown of votes per candidate is outlined below. For each candidate, you can see the percentage of total votes that they won, as well as the total number of votes cast for each candidate
  o	Charles Casper Stockham: 23.0% (85,213)
  o	Diana DeGette: 73.8% (272,892)
  o	Raymon Anthony Doane: 3.1% (11,606)
You can see here the section of code that calculates the number of votes each candidate received and the percentage of the total vote that each candidate received.

<img width="490" alt="Candidate_votes" src="https://user-images.githubusercontent.com/88349443/132954757-22876603-262e-4619-88d3-d3c6616618f9.png">

•	As you can gather from the candidate vote outline, Diana DeGette won the election by winning 73.8% of the vote, with a total of 272,892 votes. This determination was done using the following if statement.

<img width="518" alt="Winning_candidate" src="https://user-images.githubusercontent.com/88349443/132954786-b6981f8d-6e34-43f7-84d6-388959ea75ca.png">

## Election-Audit Summary

The python script I wrote for this analysis can be easily adjusted and used to analyze other election CSV documents. The first thing you would need to do is edit line 9 to contain the file path and file name of the new CSV document and edit line 11 to contain the file path and file name of the output document you want to create with the results. The second thing you would need to do is to open the CSV document containing the election results and make note of which columns contain the candidate names and the county names. With this, edit the number inside the parentheses in line 48 to contain the column number with candidate names and line 51 to contain the column number with the county names. Keep in mind that the columns start at zero, so use the number 1 to indicate column 2 for example. With these minor changes the code should be ready to run for other elections.
