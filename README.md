#  TASK 2: Phishing Simulation Using MIP22 and Social Engineering Toolkit

 **Objective:**
To simulate a phishing attack using social engineering techniques and real-world email spoofing methods by crafting a fake Netflix security alert and capturing victim credentials via a cloned login page. This is done for educational and internship demonstration purposes only.

# Tools Used:
Tool	Purpose
**MIP22** -	To generate the phishing URL (cloaked and secure)
**SET** - (Social Engineer Toolkit)	For sending HTML phishing emails
**Python HTTP Server** -	Hosting the phishing page
**Cloudflare Tunnel** - (trycloudflare)	Publicly exposing the phishing site
Linux Terminal	Command execution & file logging

# Steps Performed
1. Created Netflix Phishing Email
Designed a fake security alert email resembling Netflix UI.

Included:

Official Netflix logo

Matching font, color, and tone

A red “Verify Account” button with obfuscated hover text

#  Link in email: Generated using MIP22

2. Hosted Fake Netflix Login Page
HTML page cloned from Netflix’s login design

Captured:

Email/phone

Password

# Hosted via:

python3 -m http.server 8000
cloudflared tunnel --url http://localhost:8000

3. Generated Phishing URL with MIP22
MIP22 generated a masked URL that pointed to your Cloudflare tunnel:

**http://collar-comparable-patrick-astrology.trycloudflare.com**

#  Looks clean and deceptive like a real domain

4. Delivered Email Using SET
Configured email with:

Gmail spoof

TLS enabled

HTML body

#  Included the MIP22 phishing link inside the button

5. Captured Credentials
Inputs on the phishing site sent to a script or log file

Captured:

Email

Password

IP (if JS fingerprinting used)

#  Screenshots Included:
Phishing Email Preview

Fake Netflix Login Page

Terminal Logs Showing Captured Data
