# Description

This workflow enriches indicators of compromise with threat intelligence from VirusTotal using the IDR Alert Trigger and sends information to the Microsoft Teams channel.

# Key Features

* Perform a domain, hash, URL and IP address lookup automatically from any IDR alert
* Send the report to the Microsoft Teams channel

# Requirements

* InsightIDR License
* InsightConnect License
* VirusTotal API Key
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow leverages InsightConnect's Parameters feature. This feature allows variables used multiple times throughout a workflow to be entered once and then referenced throughout the workflow.

There are two parameters you will need to configure in order to complete setup of your workflow:

* Team Name: The Microsoft Teams team name in your environment where the workflow should be triggered and respond
* Channel Name: The Microsoft Teams channel name in your environment where the workflow should be triggered and respond (the channel should exist in the aforementioned team)

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow and create an alert trigger in InsightIDR by following these steps:

1. Open the Automation tab in InsightIDR 
2. Navigate to the Alert Triggers tab 
3. Click Create Alert Trigger 
4. Select Custom InsightConnect Workflows from the Action Category dropdown menu 
5. Select this workflow 
6. Select one or more alerts
7. Click Add Alert Trigger

### Usage

The workflow will run automatically any time the selected alert(s) open a new investigation in InsightIDR. Lookup results for each indicator will be posted on the provided channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VirusTotal|8.1.0|4|
|HashIt|2.0.4|1|
|Math|1.2.1|4|
|Microsoft Teams|3.1.5|9|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [VirusTotal](https://virustotal.com)
* [Microsoft Teams](https://teams.microsoft.com)