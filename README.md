Point Blank Account Creator
This script automates the creation of Point Blank accounts. It uses the 2Captcha service to solve the reCAPTCHA challenge and registers new accounts using randomly generated usernames and email addresses.

Features
Automatically generates a username and email for new accounts.

Uses the 2Captcha API to bypass reCAPTCHA.

Saves successfully created accounts to result.txt.

Configurable via config.json.

Prerequisites
Before running the script, you need to ensure you have the following installed:

Python 3.x

Required Python libraries (requests, json, re, names, random, 2Captcha)

A valid 2Captcha API key for reCAPTCHA solving.

Installation
Clone this repository to your local machine:

bash
Copy
Edit
git clone https://github.com/arimaulanafirmansyah/PointblankCreator.git
cd PointblankCreator
Install the required Python libraries:

bash
Copy
Edit
pip install -r requirements.txt
Configuration
Before running the script, edit the config.json file to include your 2Captcha API key and password for account registration.

config.json Format
json
Copy
Edit
{
  "api_key": "YOUR_2CAPTCHA_API_KEY",
  "password": "YOUR_PASSWORD"
}
Replace YOUR_2CAPTCHA_API_KEY with your valid 2Captcha API key.

Replace YOUR_PASSWORD with the password you'd like to use for all created accounts.

Example:
json
Copy
Edit
{
  "api_key": "a38d375f3158bf548f947d9c7049b28b",
  "password": "yourpassword123"
}
Usage
Run the script:

bash
Copy
Edit
python account_creator.py
The script will prompt you for the number of accounts you want to create. For example:

bash
Copy
Edit
[?] Berapa Account : 5
After entering the number of accounts, the script will attempt to register that many accounts. It will try to register each account up to 3 times in case of failure.

After processing, successfully created accounts will be saved to result.txt in the following format:

pgsql
Copy
Edit
username|password|email
Example output:

graphql
Copy
Edit
JohnDoe123|yourpassword123|JohnDoe123@amfcode.my.id
License
This script is free to use. However, you should respect the website's terms of service and not abuse this tool. Use at your own risk.

Notes:
API Key: Be sure to replace YOUR_2CAPTCHA_API_KEY with your actual 2Captcha API key in the config.json file.

Password: Replace YOUR_PASSWORD with your desired password for all accounts.

Retries: The script will attempt up to 3 retries for each account if there are failures in username generation, email generation, or registration.

