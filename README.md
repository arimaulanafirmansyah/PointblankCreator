# Point Blank Account Creator

This Python script automates the creation of accounts on the Point Blank website. It uses reCAPTCHA solving with the 2Captcha service and generates random usernames and emails.

### Features:
- Automatic username and email generation.
- Solves reCAPTCHA challenges using the 2Captcha API.
- Configurable with API keys and passwords from a `config.json` file.
- Logs successfully created accounts into a `result.txt` file.

---

## Prerequisites

Before running the script, you need to install the required dependencies. You can install all necessary packages using the provided `requirements.txt`.

### Installation

1. Clone this repository or download the script to your local machine.
2. Install the required libraries by running:

```bash
pip install -r requirements.txt
