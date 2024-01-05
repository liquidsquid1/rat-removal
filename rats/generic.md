# Removal
Most generic rats are easy to recover from.

Simply (IN THIS ORDER):

## 1. Remove all startup files to ensure no persistance:
Download AUTORUNS from [here](https://download.sysinternals.com/files/Autoruns.zip) and run the Autoruns64.exe file. After agreeing to the terms, you will be provided with a rather scary looking screen. This shows all of your autorun data from windows!
What you are mostly looking for is:
- Any *.SCR files
- Any options highlighted in red
- Any options with random names

and right click them to scan with VirusTotal. If you do find one that either has malicious results or is not recognised, disable it.

## 2. Unblock your AntiVirus:
BlankGrabber tries to disable and bypass UAC so its best to turn it back on. This includes websites like [VirusTotal](https://www.virustotal.com). It's so kind of BlankGrabber to provide us with an easy remove script:
[here](https://github.com/Blank-c/Blank-Grabber/blob/main/Blank%20Grabber/Extras/unblock_sites.py)

## 3. Remove and reset DISCORD:
Most RATs tries to hide and steal from DISCORD, so you want to:
- Uninstall DISCORD through control panel
- Remove all files related to discord from %localappdata%
- Reinstall

## 4. Remove and reset CHROME:
Most RATs authorise extensions to run in the background of your browser that control and redirect you to pages that you won't want to be on, so you want to:
- Uninstall CHROME through control panel
- Remove all files related to chrome from %localappdata%
- Remove the Google folder in %appdata%
- Navigate to HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome and remove any unwanted policies
- Reinstall Chrome

## 5. Refresh group policy:
Some RATs try to restrict your access to certain parts of your PC. To gain things like CMD back, run the following command in the terminal:
- gpupdate /force

## 6. RESET YOUR ONLINE PASSWORDS:
You may be safe from malware now, but your info isn't. You need to change your password for every single website you have saved on your PC, and any website where you have selected REMEMBER ME for.
