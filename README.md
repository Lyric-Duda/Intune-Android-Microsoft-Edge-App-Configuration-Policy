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

# Demo Images

## Microsoft Edge Intune App Configuration Policy Settings

![Microsoft Edge Intune Settings](https://ldgithubstorageaccount.blob.core.windows.net/githubimages/Microsoft%20Edge%20App%20Configuration%20Policy%20Information/Microsoft%20Edge%20App%20Configuration%20Full%20Size.png)

* In addition. This policy "Auto Grants" Location permissions for Microsoft Edge

# Intune Configuration Information

## Adding the Microsoft Edge App Configuration Policy

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
        1. Add desiered Device Groups
    * Review + create
        * Review then click create

## Managed Favorites only showing "MyApps"

By default if you sign into Microsoft Edge on a smartphone it will create a bookmark folder that only containes "MyApps". This ovewrites the Managed Favorites Configuration in the App Configuration Policy. Selecting false on "EdgeMyApps" wont resolve the issue because this setting only works under "Managed Apps" and not "Managed Devices".

To create a "Managed Apps" cofiguration to disable "MyApps"
1. Navagate to Apps - Android - Configuration
2. Create a "Managed Apps" policy
    * Basic
        1. Name
            * Enter the Desiered Name
        2. Target policy to
            * Select Apps
        3. Public apps
            * Public apps
                + Microsoft Edge
            * Platform
                + Android
    * Settings
        1. Settings Catalog
            * Click Next
        2. General Configuration Settings
            * Name
                + com.microsoft.intune.mam.managedbrowser.MyApps
            * Value
                + false
    * Assignment
        1. Add desiered User Groups
    * Review + create
        * Review then click create


# Referenced Links

* [Configure Microsoft Edge for Android devices using Intune](https://learn.microsoft.com/en-us/mem/intune/apps/manage-microsoft-edge)