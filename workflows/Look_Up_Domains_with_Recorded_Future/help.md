# Description

This workflow enriches an IDR alert by performing a lookup on all domains in the investigation with Recorded Future.

# Key Features

* Perform a domain lookup automatically from any IDR alert

# Requirements

* InsightConnect License
* Recorded Future API Key and Account Credentials

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

After configuring the workflow, activate it and create an alert trigger in InsightIDR by following these steps:

1. Open the Automation tab in InsightIDR 
2. Navigate to the Alert Triggers tab 
3. Click Create Alert Trigger 
4. Select Custom InsightConnect Workflows from the Action Category dropdown menu 
5. Select this workflow 
6. Select one or more alerts
7. Click Add Alert Trigger

## Usage

The workflow will run automatically any time the selected alert(s) open a new investigation in InsightIDR.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Recorded Future|5.0.1|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.1.2 - Add more detailed information about domain from Recorded Future lookup | Update Recorded Future plugin to version 5.0.1 | Update documentation | Update screenshots
* 1.1.1 - Change references link | Add workflow screenshot
* 1.1.0 - Update Recorded Future plugin
* 1.0.0 - Initial workflow

# Links

## References

* [Recorded Future API Documentation](https://support.recordedfuture.com/hc/en-us/articles/115001351947-Connect-API-Overview)