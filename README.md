# TDS PROJECT 1

## Data Scrapping

•	I started by storing multiple GitHub API tokens in an array to help manage rate limits. To make sure I didn’t hit these limits, I set up a function to rotate through the tokens, spreading requests across them.
•	Next, I used fetch with the GitHub search endpoint to pull users from Delhi who have more than 100 followers. I then parsed the response to extract user IDs, which I would need for further details.
•	After that, I split the list of users into batches. For each batch, I created a function to fetch both user details and their repositories. By using Promise.all, I could request data for each batch concurrently, taking advantage of JavaScript's asynchronous capabilities to speed up data collection.

## Interesting Findings


