SaaS Review Scraper - Streamlit Application
A Streamlit-based Python application that fetches real-time SaaS product reviews from Capterra, G2, and Trustpilot using the Wextractor API.
This tool allows users to filter reviews by date range, download data in JSON format, and supports pagination for large datasets.

Features
Fetches real-time reviews from Capterra, G2, and Trustpilot
Extracts correct identifiers from product URLs
Filters reviews based on a date range
Handles pagination for large datasets
Error handling for API failures and incorrect inputs
Secure API token management with .env file
Allows users to download reviews as JSON
Technologies Used
Python
Streamlit
Requests
Pandas
dotenv
Installation & Setup
Clone the Repository
sh
Copy
Edit
git clone https://github.com/your-username/saas-review-scraper.git
cd saas-review-scraper
Install Required Dependencies
sh
Copy
Edit
pip install -r requirements.txt
Set Up API Authentication
Create a .env file in the root directory and add your Wextractor API token:

ini
Copy
Edit
WEXTRACTOR_AUTH_TOKEN=your_api_key_here
Run the Streamlit App
sh
Copy
Edit
streamlit run app.py
How to Use
Enter the company name
Paste the product review URL
Capterra: https://www.capterra.com/p/135003/Slack/
G2: https://www.g2.com/products/asana
Trustpilot: https://www.trustpilot.com/review/slack.com
Select the review source (Capterra, G2, or Trustpilot)
Choose a date range
Set pagination offset (for large datasets)
Click “Fetch Reviews”
View & Download Reviews in JSON format
API Integration Details
The app uses the Wextractor API to fetch reviews.

Platform	API Endpoint	ID Format
Capterra	/api/v1/reviews/capterra	Extracts id from /p/135003/ in URL
G2	/api/v1/reviews/g2	Extracts product name from /products/asana in URL
Trustpilot	/api/v1/reviews/trustpilot	Extracts domain name from /review/slack.com in URL
Troubleshooting
API Request Failed (403, 500, etc.)
Ensure Wextractor API key is correct in .env
Check if Wextractor API is down
Verify the product URL format
No Reviews Found
Try adjusting the date range
Ensure correct product URL is used
Error processing review date
The issue has been fixed by handling different date formats in the API response.
License
This project is licensed under the MIT License.
