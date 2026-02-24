Complete Reddit Lead Generation Workflow

1. Schedule Trigger: Automatically wakes up and starts the automation every 5 minutes.

2. Search Parameters: Defines the broad target search keyword ("AI") to cast the widest net possible.

3. Reddit Post Scraping: Connects to Reddit and strictly pulls the 100 newest posts matching the broad keyword.

4. XML to JSON: Converts the raw, messy RSS feed data from Reddit into a clean, readable data format.

5. Split Out: Takes the large batch of 100 posts and splits them into 100 individual items so n8n can process them one by one.

6. Post Info: Extracts the most important data points from each post, including the Title, Body Content, Author, Date, and URL.

7. Custom IF Filter (The Bouncer): Uses advanced JavaScript to bypass hidden HTML tags and line breaks, aggressively scanning the text for 28 highly specific buyer phrases (e.g., "best free AI", "free LLM"). It immediately drops any post that does not contain an exact match.

8. Get row(s) in sheet: Connects to Google Sheets and reads the database of leads that have already been collected.

9. Check If there is duplicate value: Acts as a cross-referencing checkpoint. It compares the brand-new Reddit matches against the existing Google Sheet data and stops any duplicate posts from moving forward.

10. Append row in sheet: Takes the 100% unique, newly verified leads and automatically writes them into a new row in the Google Sheet.

11. Aggregate: Bundles the newly added lead data together into a clean package.

12. Send a message: Connects to Gmail and sends a real-time email alert containing the new lead information directly to the inbox.
