# README

## Data Scraping Process Overview

1. **Target User Identification**
   - Initiated a search using the GitHub API to locate users based in **Chicago** with **over 100 followers**.
   - Captured profile URLs of all qualifying users and recorded them in a text file, `users.txt`, with each profile link on a separate line to streamline the data extraction process.

2. **Creating `users.csv` for User Profiles**
   - For each user link saved in `users.txt`, retrieved detailed profile information through the API.
   - Performed data cleaning on certain fields, specifically `company`, to ensure consistency:
     - Trimmed extra spaces, removed leading `@` symbols, and converted to uppercase for uniformity.
   - Saved all relevant user data into `users.csv`, which contains the following attributes:
     - `login`, `name`, `company`, `location`, `email`, `hireable`, `bio`, `public_repos`, `followers`, `following`, `created_at`

3. **Creating `repositories.csv` for User Repositories**
   - Retrieved up to **500 of the most recently pushed repositories** for each user listed in `users.csv`.
   - Recorded key repository details, focusing on fields that offer insights into the project’s popularity and development features:
     - Fields captured: `login`, `full_name`, `created_at`, `stargazers_count`, `watchers_count`, `language`, `has_projects`, `has_wiki`, `license_name`
   - Saved this data to `repositories.csv`, creating a structured dataset that facilitates analysis of user activity and repository characteristics.
