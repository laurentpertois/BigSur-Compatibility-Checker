# BigSur-Compatibility-Checker

This script was designed to be used as an Extension Attribute on Jamf Pro server to ensure specific requirements have been met to deploy macOS Big Sur. With little modification it can probably be used on other systems (Jamf Pro server requires the output of an Extension Attribute to be `echo "<result>$FOO</result>`).

## General Requirements:
  - OS X 10.9.0 or later (It seems, as of the day I write this Apple has not yet made recommendations, this page and the script will be adapted if necessary when the information will become public)
  - 4GB of memory (It seems, as of the day I write this Apple has not yet made recommendations, this page and the script will be adapted if necessary when the information will become public)
  - 60GB of available storage, the required storage is different when upgrading from Catalina (33,5GB) or from older versions (44,5GB) and accounts for the size of the installer (almost 13GB)

These last 2 requirements can be modified in the first 2 variables (`MINIMUMRAM` and `MINIMUMSPACE`).
  - REQUIREDMINIMUMRAM: minimum RAM required, in GB
  - REQUIREDMINIMUMSPACE: minimum disk space available, in GB
 

## Mac Hardware Requirements and equivalent as minimum Model Identifier
	- MacBook (Early 2015 or newer), ie MacBook8,1
	- MacBook Pro (Late 2013 or newer), ie MacBookPro11,1
	- MacBook Air (Mid 2013 or newer), ie MacBookAir6,1
	- Mac mini (Late 2014 or newer), ie Macmini7,1
	- iMac (Mid 2014 or newer), ie iMac14,4
	- iMac Pro, ie iMacPro1,1
	- Mac Pro (Late 2013 or newer), ie MacPro6,1

Default compatibility is set to False if no test pass (variable `COMPATIBILITY`)

## Installation

Copy the content of the script (`.sh` file) to a new Computer Extension Attribute or just download the existing Extension Attribute (`.xml`) file and upload it to the Computer Extension Attributes of your Jamf Pro server.
