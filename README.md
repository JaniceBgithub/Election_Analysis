# Election_Analysis

## Purpose

The purpose of this election analysis was to analyze congressional electing voting data to determine the winners and other statistics related to county, percent of votes by candidate etc. 

## Election Audit Results

### County data

There were 369,711 votes cast in this congressional election.  There were three counties in this election.  They are shown along with their respective portion of votes and number of votes: 
  - Jefferson: 10.5% (38,855)
  - Denver: 82.8% (306,055)
  - Arapahoe: 6.7% (24,801)
  
 Denver had the largest portion of votes with 82.8%.
 
 ### Candidate data
 
 There were three candidates in this election.  Their results are shown along with their respective portion of votes and number of votes:
   - Charles Casper Stockham: 23.0% (85,213)
   - Diana DeGette: 73.8% (272,892)
   - Raymon Anthony Doane: 3.1% (11,606)
   
   Dianna DeGette won the election with 73.8% of the vote and 272,892 votes. 
   
   ## Execution of python script to the terminal
   
   The election results were run in a python terminal as well as written to a text file.  In this case, I used jupyter notebook for executing the code.  
   The screenshot of results is:
   
   ![screen_shot](https://github.com/JaniceBgithub/Election_Analysis/blob/master/analysis/Screen_shot.png)
   
   ## Results plot
   
   The results from the election were plotted:
   
   ![results_plot](https://github.com/JaniceBgithub/Election_Analysis/blob/master/analysis/results_figure.png)
   
   
   ## Election Audit Summary
   
  The script developed for this election can be used for any election.  Most of the code is already applicable for any situation.  
  For example, the python script reads the file and finds the candidate names.   There is a similar piece of code for finding the county names. 
 
      # For each row in the CSV file.
      for row in reader:
        
        # Get the candidate name from each row.
        candidate_name = row[2]    
        
        # If the candidate does not match any existing candidate add it to the candidate list
        if candidate_name not in candidate_options:

            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)
     
     
The raw input data files and output files are hard coded into python as follows.  
     
        # Add a variable to load a file from a path.
        file_to_load = os.path.join("Resources", "election_results.csv")

        # Add a variable to save the file to a path.
        file_to_save = os.path.join("analysis", "election_analysis.txt")
     
An additional python script could be created to read in the name of the election results csv file in a specific folder and then run the analysis.  The program could be modified to process mulitple text files in the same folder one at a time. 

The following code could be used to run through all the csv files in a specific folder and run multiple analysis:

      import glob 
      for file_name in glob.iglob('Election_Results/**/*.csv', recursive=True):

 Similarly, python could create an election analysis text file for each result using: 
 
        filehandle = open('file_name.txt', 'w+')
        
The "W" means write to the file and the "+" means that the file must be created. 
 
 
