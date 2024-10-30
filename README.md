
Here’s an improved version of your README documentation for scraping GitHub users and repositories:

1. Explanation of How I Scraped the Data
Identify Target Users

Queried the GitHub API for users located in Chicago with over 100 followers.
Extracted profile links of eligible users and saved them to users.txt, one link per line for efficient processing.
Generate users.csv

For each user in users.txt, retrieved detailed profile information via the GitHub API.
Cleaned and standardized company names (e.g., trimmed whitespace, removed leading @ symbols, and converted to uppercase).
Saved the processed data to users.csv, with the following fields:
login, name, company, location, email, hireable, bio, public_repos, followers, following, created_at
Generate repositories.csv

For each user in users.csv, fetched up to the 500 most recently updated repositories.
Extracted repository details, including:
login, full_name, created_at, stargazers_count, watchers_count, language, has_projects, has_wiki, license_name
Saved the repository information to repositories.csv to enable deeper analysis and comparisons.
