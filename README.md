# Microsoft Edge App Configuration Policy Information

* This is my Microsoft Edge App Configuration Policy for Fully Managed Company Owned Devices

# JSON Configuration Information

## Microsoft Edge Custom Template

* I took the template that you can download from intune when you make a "App Configuration Policy" for "Microsoft Edge" and structured it to be "3 Space Tab"

## Microsoft Edge JSON Structure

This JSON file is structured to

* Enable Browser Sign In Settings
* Add Company Favorites to Microsoft Edge
* Disable Incognito Mode
* Set the homepage to the company SharePoint homepage
* Set the default search engine to google
* Disable unneeded Microsoft Edge features

## Adding the JSON to Intune

To create the Microsoft Edge App Configuration Policy
1. Navagate to Apps - Android - Configuration
2. Create a "Managed Device" policy
    * Basic
        1. Name
            * Enter the Desiered Name
        2. Platform
            * Android Enterprise
        3. Profile Type
            * Select
                + All Profile Types
                + Fully Managed, Dedicated, and Corporate-Owned Work Profile Only
                + Personally-Owned Work Profile Only
        4. Targeted App
            * Microsoft Edge
    * Settings
        1. Configuration Settings
            * Enter JSON data
                + Enter the JSON Data from JSON Configurations or JSON Template
    * Assignment
        1. Add desiered Users, Devices, or Groups
    * Review + create
        * Review then click create

# Demo Images

## Microsoft Edge Intune App Configuration Policy Settings

![Microsoft Edge Intune Settings](https://ldgithubstorageaccount.blob.core.windows.net/githubimages/Microsoft%20Edge%20App%20Configuration%20Policy%20Information/Microsoft%20Edge%20App%20Configuration%20Full%20Size.png)

* In addition. This policy "Auto Grants" Location permissions for Microsoft Edge

# Referenced Links

* [Configure Microsoft Edge for Android devices using Intune](https://learn.microsoft.com/en-us/mem/intune/apps/manage-microsoft-edge)