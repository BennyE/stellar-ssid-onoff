# stellar-ssid-onoff
stellar-ssid-onoff is a small tool that toggles the operational status of a given SSID on Stellar Wireless (Enterprise mode)

## Dependencies
- requests (Thanks to Kenneth Reitz - http://www.python-requests.org/)
- Python3.5 (This is what comes with my Debian release, no support for Python 2.x)
- A separate system to run this code, as you can't host this on Alcatel-Lucent Enterprise OmniVista 2500 today
 
## Example

```
$ python stellar-ssid-onoff.py 

TODO: ADD OUTPUT

```

## Demo Video
TODO: ADD VIDEOLINK
[![Demo Video](https://img.youtube.com/vi/cx0n13rECW0/0.jpg)](https://www.youtube.com/watch?v=cx0n13rECW0)

## Usage
TODO: UPDATE
Edit the **settings.json.template** and save it as **settings.json**
```
{
        "ov_hostname": "omnivista.example.com",		# The OmniVista 2500 server to connect to
        "ov_username": "admin",				# Username
        "ov_password": "switch",			# Password
        "validate_https_certificate": "yes",		# Validate the HTTPS certificate?
        "ap_group": "ap-group-name-case-sensitive",	# AP-Group of APs that you want to update (case-sensitive!)
        "ssid": "ssid-name",				# Name of the SSID on which you want to update the PSK
        "psk_length": 12				# The length of the PSK to generate
        "send_psk_via_mail": "yes",			# If you want to send a mail with the PSK/QR Code
        "email_from": "FROMaddress@mailprovider.com",	# mailFrom
        "smtp_server": "smtp.gmail.com",		# SMTP server
        "smtp_auth": "yes",				# Please specifiy if you need authentication
        "smtp_port": 587,				# If "auth" is set, we currently always do TLS
        "smtp_password": "passwordforsmtp",		# SMTP password
        "language": "de",				# Language for the mail (de, en) 
        "email_to": "TOaddress@mailprovider.com"	# mailTo
}
```
