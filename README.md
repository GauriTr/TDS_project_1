# TDS PROJECT 1

## Data Scrapping

•	I started by storing multiple GitHub API tokens in an array to help manage rate limits. To make sure I didn’t hit these limits, I set up a function to rotate through the tokens, spreading requests across them.

•	Next, I used fetch with the GitHub search endpoint to pull users from Delhi who have more than 100 followers. I then parsed the response to extract user IDs, which I would need for further details.

•	After that, I split the list of users into batches. For each batch, I created a function to fetch both user details and their repositories. By using Promise.all, I could request data for each batch concurrently, taking advantage of JavaScript's asynchronous capabilities to speed up data collection.

## Interesting Findings

•	There is a slight negative correlation (-0.018) between the number of followers and public repositories, suggesting that simply having more repositories does not guarantee more followers.

•	The regression slope for followers per repository is -0.051, indicating that, on average, additional public repositories do not significantly increase follower counts.

•	A significant number of users are affiliated with MASAI SCHOOL, indicating a concentrated community of developers from this institution, which may influence collaboration and networking.

•	The regression analysis shows a positive impact (slope of 11.906) of bio length on followers, suggesting that more detailed bios can attract more followers.

•	Users with high leader strength include well-known figures like Anuj-Kumar-Sharma and shradha-khapra, highlighting the importance of perceived authority in gaining followers.

## Actionable Recommendation 

•	Enhance Your Bio: Invest time in crafting a detailed and informative bio. Highlight your skills, projects, and interests. 

•	Focus on Quality Over Quantity: Instead of merely increasing the number of public repositories, prioritize the quality and relevance of your projects. 

•	Leverage Community Connections: Connect with influential users, especially those with high leader strength. Engage with their projects, contribute to discussions, and seek mentorship. 

•	Participate Actively on Weekends: Consider dedicating time on weekends to work on personal projects or contribute to open-source initiatives. 

•	Choose Popular Technologies: Stay updated with the most popular programming languages and technologies (e.g., JavaScript, HTML) as identified in the analysis.

•	Engage with the MASAI SCHOOL Community: If you are affiliated with MASAI SCHOOL or similar institutions, leverage this network for collaboration and support.
