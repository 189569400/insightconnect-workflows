# Description

This workflow blacklists or unblacklists indicators with Trend Micro Apex via Slack command and reports information back to Slack.
Indicators supported in this workflow are SHA1 hashes and IP addresses.

Sample Slack Trigger Commands:

`@Rapid7 InsightConnect blacklist-indicator 02699626f388ed830012e5b787640e71c56d42d8`

`@Rapid7 InsightConnect blacklist-indicator 198.51.100.100`

`@Rapid7 InsightConnect unblacklist-indicator 198.51.100.100`

`@Rapid7 InsightConnect unblacklist-indicator 02699626f388ed830012e5b787640e71c56d42d8`

The indicators will show up in the "User Defined Suspicious Objects" list in the Trend Micro Apex console.
The UDSO tab is located on the Custom Intelligence page under Threat Intel from the main menu.

# Key Features

* Blacklist indicators

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* Trend Micro Apex account with Automation API Access Settings configured

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

Once the workflow has been imported, **each Slack step will need the channel name updated to suit your Slack environment!** Edit the input with the preset text of `change_me` in each Slack step in the workflow.

After configuring the Slack steps, activate the workflow in order to trigger it.
 
## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Trend Micro Apex|3.0.0|2|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Fix decision path and set change_me values for Slack steps
* 1.0.0 - Initial workflow

# Links

## References

* [Trend Micro Apex](https://www.trendmicro.com/en_us/business/products/user-protection/sps/endpoint.html)
* [Trend Micro Apex plugin](https://extensions.rapid7.com/extension/trendmicro_apex)
* [Slack](https://slack.com)
