# Email Header Analyser

A Python tool that analyses email headers to extract key information 
and detect potential phishing and spoofing attempts.

## Features
- Extracts sender (From) email address
- Extracts Reply-To email address
- Extracts all relay IP addresses from Received headers
- Extracts Message ID
- Extracts all timestamps from the email chain
- Checks SPF result and flags if not passing
- Compares From and Reply-To domains to detect spoofing

## How to Use
1. Replace the `header` variable with your email header
2. Run the script:
```bash
python3 EmailAnalyzer.py
```

## Example Output
From email: ['vieria@aol.com']
To email: ['carrr444@yahoo.com']
Received IP: ['10.255.104.164', '10.255.104.165', '65.55.88.116', '59.125.100.113']
Message ID: ['201301172333.r0HNXZSI028539@mail.shako.com.tw']
Timestamp: ['23:35:35', '23:35:34', '23:35:34']
From domain: ['@aol.com']
Reply-To: ['@yahoo.com']
WARNING: From and To domains do not match - Possible spoofing!
Received SPF: ['neutral'] - Flagged as suspicious!

## Built With
- Python 3
- re (built-in)
