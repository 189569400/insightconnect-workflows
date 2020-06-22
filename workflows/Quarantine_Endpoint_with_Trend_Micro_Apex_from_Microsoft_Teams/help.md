# Description

This workflow quarantines or unquarantines endpoints with Trend Micro Apex via Microsoft Teams command and reports information back to Microsoft Teams.
This workflow supports endpoints in the form of Agent IDs, hostnames, MAC addresses, or IP addresses.

Sample Slack Trigger Commands:

`@!quarantine-endpoint 08-00-27-96-86-8E`

`@!quarantine-endpoint 198.51.100.100`

`@!unquarantine-endpoint 198.51.100.100`

`@!unquarantine-endpoint 08-00-27-96-86-8E`

To view quarantine logs, click "Directories" and then "Users/Endpoints" from the main menu in the Trend Micro Apex console.
Next, select the endpoint you would like to view and click the "Notes" tab. The quarantine logs are found there.

# Key Features

* Quarantine endpoints

# Requirements

* [Microsoft Teams setup](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* Trend Micro Apex account with Automation API Access Settings configured

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Microsoft Teams step will need the channel name and a team name updated to suit your Microsoft Teams environment!** Edit the input with the preset text of `change_me` in each Microsoft Teams step in the workflow.

After configuring the Microsoft Teams steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.5|7|
|Trend Micro Apex|3.0.1|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Trend Micro Apex](https://www.trendmicro.com/en_us/business/products/user-protection/sps/endpoint.html)
* [Trend Micro Apex plugin](https://extensions.rapid7.com/extension/trendmicro_apex)
* [Microsoft Teams](https://teams.microsoft.com)
