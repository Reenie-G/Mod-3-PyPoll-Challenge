# **Analysis of the Election Audit**

## **Overview of Election Audit:**
	The purpose of this election audit is to provide the following:
		* The voter turnout for each county and candidate
		* The percentage of votes for each county and candidate from the total count
		* The county and candidate with the highest turnout, thus declaring a winner

	To get these results, I utilized Pandas libraries in Jupyter notebook. This allows for the use of for loops and conditionals to iterate through large amounts of data 	and pull the requested information and provide an outcome of just the information that is needed.  

##**Election-Audit Results**
	
<<<<<<< HEAD
**Congressional Election Total Votes**
=======
	### Congressional Election Total Votes
>>>>>>> b1d80610474d3e2b0d8d4058f2f9a0761ebbabbd
	
		Before getting the results of the county votes and the candidate votes, the overall votes for both is needed. This will be used to get the percentage of votes 	for each county and candidate. The following steps will provide the total votes.  
			
			1. Use the for loop: 
	
						 `for row in reader:`
			
			2. Add to the total vote count: 

						 `total_votes = total_votes + 1`
			
			3. Get the candidate name from each row: 

						 `candidate_name = row[2]`
			
			4. Extract the county name from each row: 

						 `county_name = row[1]`
			
			5. If conditional for the candidate name: 

						 `if candidate_name not in candidate_options:`
			
			6. The append function is used to get the candidate name : 

						 `candidate_options.append(candidate_name)`
			
			7. The candidate's voter count is tracked: 

						 `candidate_votes[candidate_name] = 0`
			
			8. *The steps are repeated for the county votes* 
			
			9. The result is saved to the election analysis text file: 

						 `print(election_results, end="")`
    						 `txt_file.write(election_results)`
			
			10. The total votes in the congressional election is 369,711
			
		
<<<<<<< HEAD
**County Results**
=======
	### County Results
>>>>>>> b1d80610474d3e2b0d8d4058f2f9a0761ebbabbd

		Now that we have this information we can move forward to getting the votes for each county and percentages. This will also give the county with the 			largest voter turn out. 
			
			1. Use a for loop to iterate through the csv file: 
						 
						 ` for county_name in county_votes: `
			
			2. Retrieve the county vote count: 
						 
						 `votes = county_votes.get(county_name)`
			
			3. Calculate the percentage fo votes for the county: 
			
						 `vote_percentage = float(votes)/float(total_votes)*100`
			
			4. Print the county results to the election analysis text file: 
						 
						 `county_results = (f"{county_name}: {vote_percentage:.1f}% ({votes:,})\n")`
    									
						 `print(county_results)`
			5. Use an if conditional to get the winning county: 
						 
						 `f (votes > winning_county) and (vote_percentage > winning_percentage):`
			
			6. Print the county with the largest turnout: 
						 
						 `largest_county_turnout = (
            					 f"-------------------------\n"
            					 f"largest_county_turnout {winning_county}\n"
            					 f"--------------------------\n")
    
    											`print(largest_county_turnout)`
			7. Save the results in the election analysis text file: `txt_file.write(largest_county_turnout)`
		
		This should provide the following outcome: image.
		Looking at the county votes, Denver had the largest turnout of votes, 306,055 82.8%. Then Jefferson with 38,855 votes, 10.5% and lastly, Arapahoe with 24,801 		which is 6.7% percent.

<<<<<<< HEAD
**Candidate Results**
=======
	### Candidate Results
>>>>>>> b1d80610474d3e2b0d8d4058f2f9a0761ebbabbd
	
		To get the candidate results, we use the same functions that were used for the county votes, a for loop and if conditional.

			1. for loop: `for candidate_name in candidate_votes:`
			
			2. Retrive the vote count and percentage: 
						 
						 `votes = candidate_votes.get(candidate_name)`
								 
						 `vote_percentage = float(votes) / float(total_votes) * 100`
						 
						 ` candidate_results = (f"{candidate_name}: {vote_percentage:.1f}%({votes:,})\n")`
			
			3. Get the county results: 
						 
						 `candidate_results = (f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")`
			
			4. print and save the results in the election analysis file: 
						 
						 `print(candidate_results)` `txt_file.write															 (candidate_results)`
			
			5. Use an if conditional to determine the winning vote, percentage and candidate and print: 
					
						`if (votes > winning_count) and (vote_percentage > winning_percentage):`
            
						winning_count = votes
            					winning_candidate = candidate_name
            					winning_percentage = vote_percentage
							 
			
			6. The winning candidate information is placed in a summary and printed:
  
						winning_candidate_summary = (
        					f"-------------------------\n"
        					f"Winner: {winning_candidate}\n"
        					f"Winning Vote Count: {winning_count:,}\n"
        					f"Winning Percentage: {winning_percentage:.1f}%\n"
        					f"-------------------------\n")
    
    					print(winning_candidate_summary)

		If done properly, the winner will be Diane DeGette with total votes 272,892 which is 73.8% of the total votes. In second place is Charles Casper Stockham with 		total votes 85,231 which is 23.0% and lastly, Raymon Anthony Doane with 11,606 votes which is 3% of the votes. 	  			
   
				 
## Election-Audit Summary:

		Now that a script has been proven to give county and candidate vote results election, this can be used for future elections. Something to consider is the 		county vote totals, further analysis could be done for the counties with the lower voter turnouts. What could be causing a low turnout, is it due to population 		size, is this a lower income area? This is something a future candidate can consider when planning where they will be campaigning. One piece of information 			that was missing was the political party affiliation of each candidate. Using the same script we can add a category for different political parties and use a 			for loop and if conditional to iterate through the data and pull the counts of each different political party. This can be useful for determining a candidate 			winner and who will be the county with the most voter turnout. 
<<<<<<< HEAD




		


		



=======
>>>>>>> b1d80610474d3e2b0d8d4058f2f9a0761ebbabbd
