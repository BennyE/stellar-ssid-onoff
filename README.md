# stellar-ssid-onoff
stellar-ssid-onoff is a small tool that toggles the operational status of a given SSID on Stellar Wireless (Enterprise mode)

## Dependencies
- requests (Thanks to Kenneth Reitz - http://www.python-requests.org/)
- Python3.5 (This is what comes with my Debian release, no support for Python 2.x)
- A separate system to run this code, as you can't host this on Alcatel-Lucent Enterprise OmniVista 2500 today
 
## Example

```
$ python stellar-ssid-onoff.py 

Stellar SSID on/off - a simple script to toggle the operational status of Stellar Wireless SSIDs
Written by Benny Eggerstedt in 2018
This is free software not provided/shipped by Alcatel-Lucent Enterprise. Use it at your own risk!

[+] Reading settings.json file
[*] Attempting to connect to OmniVista server @ https://omnivista.home
[*] Connection to omnivista.home successful!
[*] Found instanceID 59ab1cb7e4b010f83b3d47f0 for AP group Home
[*] Found deviceId 5a7d02b6e4b0582ec054a882 for SSID dynpsk
[+] Toggled the operational status of SSID dynpsk to disabled

```

## Demo Video
[![Demo Video](https://img.youtube.com/vi/VXllxh8jaGU/0.jpg)](https://www.youtube.com/watch?v=VXllxh8jaGU)

## Usage
Edit the **settings.json.template** and save it as **settings.json**
```
{
        "ov_hostname": "omnivista.example.com",		# The OmniVista 2500 server to connect to
        "ov_username": "admin",				# Username
        "ov_password": "switch",			# Password
        "validate_https_certificate": "yes",		# Validate the HTTPS certificate?
        "ap_group": "ap-group-name-case-sensitive",	# AP-Group of APs that you want to update (case-sensitive!)
        "ssid": "ssid-name"				# Name of the SSID that you want to enable/disable
}
```
