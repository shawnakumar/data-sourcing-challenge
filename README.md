## Objective 
### This project involves accessing and processing data from the New York Times Article Search API and The Movie Database (TMDB) API. The goal is to retrieve movie reviews from the New York Times and extract relevant information about the movies from TMDB.Project OverviewPart 1: Accessing the New York Times APIThe New York Times API is accessed to retrieve movie reviews meeting specific criteria, such as containing the word "love" in the headline and being categorized as movie reviews.

*   A query URL is constructed based on the API documentation.
    
*   A loop is created to iterate through multiple pages of results.
    
*   Results are retrieved using GET requests, and a 12-second interval is implemented between queries.
    
*   A try-except clause handles errors and retrieves reviews from the response.
    
*   The extracted data is previewed and converted into a Pandas DataFrame.
    
*   Titles and keywords are extracted from the DataFrame.
    

Part 2: Accessing The Movie Database APIThe TMDB API is accessed to retrieve additional details about the movies mentioned in the New York Times reviews.

*   Titles extracted from Part 1 are used to search for corresponding movies in TMDB.
    
*   Details about the movies, such as genres, languages, and production countries, are extracted and stored.
    
*   Data retrieval is handled in a try-except block to manage errors and ensure robustness.
    
*   Results are previewed and converted into a DataFrame for further analysis.
    

Part 3: Merging and Cleaning the DataThe data retrieved from both APIs are merged and cleaned before export.

*   Data from both APIs are merged on the movie titles column.
    
*   Columns containing lists are cleaned by removing brackets and quotation marks.
    
*   Duplicate rows are removed, and the index is reset.
    
*   The final DataFrame is exported to a CSV file without the index.
    

Project RequirementsThe project requirements include proper construction of query URLs, handling of API requests and responses, extraction of relevant data, merging and cleaning of data, and exporting the final DataFrame to a CSV file.Implementation DetailsFor detailed implementation steps and code samples, refer to the project script and the corresponding comments provided in the code. Each part of the project is structured with clear instructions and guidelines for implementation.Considerations

*   Ensure that API keys and query parameters are correctly set up to access the APIs.
    
*   Handle errors and exceptions gracefully to maintain code robustness.
    
*   Utilize appropriate libraries and methods in Python, such as requests, pandas, and time.
    
*   Debug code as needed, and use print statements to troubleshoot any issues encountered during development.

#### Conclusion - This project demonstrates the process of accessing and processing data from APIs, merging and cleaning datasets, and exporting the final results for further analysis or visualization. By following the provided instructions and guidelines, developers can replicate or extend this project to suit their specific needs or explore additional APIs and datasets for further analysis.

#### Sources
*  AskBCS
*  Tutor 
*  API NYT - https://api.nytimes.com/svc/search/v2/articlesearch.json?
*  API TMDB - https://api.themoviedb.org/3/search/movie?query=
#### Code Reference
* Main Python File: /Users/ashwinikumar/AI_Bootcamp/Student_AI_repos/data-sourcing-challenge/retrieve_movie_data.ipynb
* Output csv NYT_TMDB.csv
* Source Data collected_data.csv