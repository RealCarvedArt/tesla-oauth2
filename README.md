# Tesla OAuth Token Generation
A script on how to interact with the recent OAuth2 changes from Tesla and the new `/oauth2/` endpoint.

## PREREQUISITES:​
Python 3.x (Download Python)
ChromeDriver (http://chromedriver.storage.googleapis.com/index.html) (select the version that matches your Chrome version)
auth.tokens.py (https://raw.githubusercontent.com/teslascope/tokens/master/auth.tokens.py)
requirements.txt (enode-engineering/tesla-oauth2) -OR- create a text file named “requirements.txt” and add the following two lines:

    Code:
    requests==2.24.0
    selenium==3.141.0

## STEPS:​
Download the prerequisites
Create a project folder to store your files; e.g., “C:\Users\Username\Desktop\TeslaTokens”
Place: ChromeDriver, auth.tokens.py, and requirements.txt in “C:\Users\Username\Desktop\TeslaTokens”
Install Python FOR ALL USERS and add to PATH (If you need help installing Python there are plenty of great videos out there explaining the process for each system)
Launch a command window/terminal (e.g., PowerShell, Command Prompt, Terminal, etc.)
Type:
    Code:
    CD C:\Users\Username\Desktop\TeslaTokens
Press: ENTER
Type:
        Code:
        pip install -r requirements.txt
Press: ENTER
At this point everything should be installed, configured and ready to go
Then enter one of the below strings at the command prompt and hit ENTER:

If your Tesla account has MFA enabled:
        Code:
        python3 ./auth.tokens.py -u 'email' -p 'password' -c 'passcode'

If your Tesla account does not have MFA enabled:
        Code:
        python3 ./auth.tokens.py -u 'email' -p 'password'

-u = Tesla account email
-p = Tesla account password
-c = Passcode generated by your authenticator app

MFA example:
        Code:
        python3 ./auth.tokens.py -u myTeslaEmail@someDomain.com -p someSuperSecurePassword -c 123456

Non-MFA example:
        Code:
        python3 ./auth.tokens.py -u myTeslaEmail@someDomain.com -p someSuperSecurePassword

## TIPS:​
If python3 does not work try using just python
To check your Python install you can type:
        Code:
        python --version

```
>python3 ./TeslaTokenV3.py -h
usage: TeslaTokenV3.py [-h] -u EMAIL -p PASSWORD [-v] [-c CODE]

optional arguments:
  -h, --help            show this help message and exit
  -u EMAIL, --email EMAIL
                        • Tesla account email
  -p PASSWORD, --password PASSWORD
                        • Tesla account password
  -v, --verbose         • Verbose output
  -c CODE, --code CODE  • Passcode generated by your authenticator app
```

## Troubleshooting
If you are looking for documentation we suggest you check out https://github.com/timdorr/tesla-api
