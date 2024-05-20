file:///C:/Users/aneskovic/Downloads/Detailed_Google_Sheets_API_Script_Guide.pdf
https://docs.google.com/spreadsheets/d/1umbUyiHTzGjrYCfQddMazRHh54oAGkqPGLRdCfBNifE/edit#gid=0

1. Introduction
This document provides detailed instructions on setting up the Google Sheets API and using a Python script to update a Google Sheet with data extracted from a website using Playwright.

2. Setting Up Google Sheets API
Create a Project in Google Cloud Console
Go to the Google Cloud Console.
Click on the project dropdown at the top and select "New Project".
Enter a name for your project and click "Create".
Enable Google Sheets API
In the Google Cloud Console, navigate to APIs & Services > Library.
Search for "Google Sheets API".
Click on the "Google Sheets API" result and then click "Enable".
Create Service Account Credentials
Go to APIs & Services > Credentials.
Click on "Create Credentials" and select "Service Account".
Enter a name for the service account and click "Create and Continue".
In the "Grant this service account access to the project" section, select "Editor" and click "Continue".
Skip granting users access and click "Done".
Click on the created service account, go to the "Keys" tab, and click "Add Key" > "Create New Key".
Select "JSON" and click "Create". The JSON file will be downloaded to your computer.
Share Google Sheet with Service Account Email
Open your Google Sheet.
Click on the "Share" button.
Enter the email address from the downloaded JSON key file (found in the "client_email" field).
Give the service account "Editor" permissions and click "Send".

3. Installing Necessary Python Packages
Install the required Python packages using pip:

pip install gspread google-auth playwright
Install Playwright browsers by running:
playwright install

4. Running the Script
Ensure that your Google Sheet is shared with the service account email.
Place the downloaded JSON key file in the same directory as the script.
Replace "Client1.json" in the script with the actual name of your JSON key file.

