# Installation

## MEM Installation

MEM (Microsoft Endpoint Manager, aka Intune) is the tool that we use to manage devices.
This document provides a step-by-step guide on how to install it on your device.

### MacOS

1.	Create a new Apple ID using your company email. Use it during the configuration phase of your MacBook
2.	During the configuration phase, you’ll be asked to enable disk encryption: don’t do it. It will be enforced automatically by MEM
3.	When setup is complete, install MEM through this [link](https://login.microsoftonline.com/common/oauth2/authorize?client_id=74bcdadc-2fdc-4bb3-8459-76d06952a0e9&redirect_uri=https%3a%2f%2fportal.manage.microsoft.com%2fsignin-oidc&response_type=code&prompt=select_account&scope=openid+profile&response_mode=form_post&nonce=637577968972513038.ZGY0M2MyNjQtZjYzOC00ZDBkLTljNGMtYzBlNjYyMWYyMDdhMjljYjBmN2MtZTI1ZC00ZjAzLTgyMTMtOThmZDU1NzE2NGJh&claims=%7b%22id_token%22%3a%7b%22deviceid%22%3a%7b%22essential%22%3afalse%7d%7d%7d&state=CfDJ8J4r-mZRMYNLmTtS3FK9vFWNAC7mVAj46i3i7uwBADXC6GINlfpet-yTD3nEG-JyeLltbbp6DsgYv2744xpjtb51UlWQhOtR0MuO3v8YATejApmKCiHOsl2qNZRAYP8YeA1n3yLE4e4EI-C6MtfDuHNa9RsAWImFp1iz2QIjDIp4EozonL1pyBzp2-2DlgKMJxKeDmHlQs30KX0tphRjQSAObQLj3aaoZfHtNqBk4g5p21hy3zSuvEzbHaq9zRvOChtZIux-MoOTEcJWTR-uKb5MbzTk76EdGSGGdFeE-HfzWxjHoCClWN8udxtr8FOo3gJ8_dZOUOCIkTENMktVcnB_XLX5yOGD6kKLv87Nma6KpgTke-KeI8sLixwkJBqtM-20pRNFuNtohuu0OH62Q_c&x-client-SKU=ID_NET461&x-client-ver=5.3.0.0&sso_nonce=AwABAAAAAAACAOz_BAD0_xnW82ByDFlOiyPVmhP3T7lZIOG5b9tpIVLCDRqKWz9A6Slp4zK7_ZONxGJWtjfRy9-nQBPdXaCSJgtOZj2OzQwgAA&client-request-id=1071aff1-d1f4-41d5-ad1b-39e0c650f15a&mscrid=1071aff1-d1f4-41d5-ad1b-39e0c650f15a) log in with your company credentials: at this point you will inherit company policies.
4.	We suggest to reboot your laptop for some policies to kick in.
5.  Install the desktop Teams app from [microsoft-teams website](https://www.microsoft.com/microsoft-teams/download-app).

> [!Note] When prompted with the login kechain access request, make sure to check "always allow" instead of "allow", otherwise you'll be prompted back to the same request.


Reach out Internal IT to check that installation is complete or if you need help.

### Windows

It may be necessary to unplug all USB devices (charger, keyboard, mouse, etc.) until the procedure is complete, in order to avoid device compliance issues.

1.	Click on start, and look for windows store and click inside
2.	Search for company portal, download and install
3.	Enter the company portal, log in with your company credentials and follow the procedure accepting all the permissions.
4.	We suggest to reboot your laptop for some policies to kick in.
5.  Install the desktop Teams app from [microsoft-teams website](https://www.microsoft.com/microsoft-teams/download-app).

For windows users, TPM must be enabled to be policy compliant. If your laptop is still marked as non-compliant, this is likely to be the cause. TMP is a feature that is enabled in the BIOS, therefore it’s enablement depends on the manufacturer.
Here the procedure the two most common PCs used in AgileLab.

**Dell**

How to access the bios:
    -	Turn off the system
    -	Turn on the system.
    -	When the Dell logo screen appears, press the F2 key to enter System Setup.
    -	Once you have accessed the system BIOS, go to security, go to the PTT Security section and uncheck Intel Platform Trust Technology.
    -	At this point always go to security, TMP Security and select TPM Security.
    -	Apply and save the settings.
    -	Exit the BIOS and boot the operating system normally.

**Asus**

-	Turn off the system, turn on the system.
-	When the Asus logo screen appears, press the F2 key to enter system setup.
-	Once you have logged into the BIOS system, go to security, go to TMP Security and select TPM Security.
-	Apply and save the settings.
-	Exit the BIOS and boot the operating system normally.

Reach out Internal IT to check that installation is complete or if you need help.

### Android

For android mobile phones, you just need to install the app “Company portal/Portale Aziendale” from your device default store.

Once the installation is complete you’ll be able to install new apps (teams, outlook, etc.) from a new play store. All apps (including the play store) can be recognized by a “lock” icon.
Play store contains only approved apps. If you need an app which is not listed there, please reach out Internal IT.

### iOS

For iOS mobile phones, you just need to install the app “Company portal/Portale Aziendale” from your device default store.

The Select device and enrollment type screen appears and prompts for your device type:
-	Tap Agile Lab owns this device if you received your device from Agile Lab.
-	Tap Secure entire device if it’s your personal iphone.

From this point on, office365 apps will be protected by 

