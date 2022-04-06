# Description

This workflow enriches an IDR alert by performing a lookup on all domains, hashes, URLs and IPs in the investigation with Recorded Future and send results on Slack.

# Key Features

* Perform a domain, hash, URL and IP lookup automatically from any IDR alert, send results on Slack

# Requirements

* InsightConnect License
* Recorded Future API Key and Account Credentials
* [Slack](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

This workflow is using InsightConnect's Parameters feature. This allows to enter a variable once and use it multiple times throughout the workflow. 

There is one parameter which user needs to configure in order to complete workflow setup:

* Slack Channel or Person Identifier: 
Slack channel or person identifier to send RecordedFuture report. E.g:
@jdoe - to send a message to person named jdoe
#integration - to send a message to channel named integration

To begin, select "Parameters" either from the Workflow Control Panel or from the Builder to begin configuration.

After configuring the parameters, activate the workflow and create an alert trigger in InsightIDR by following these steps:

1. Open the Automation tab in InsightIDR 
2. Navigate to the Alert Triggers tab 
3. Click Create Alert Trigger 
4. Select Custom InsightConnect Workflows from the Action Category dropdown menu 
5. Select this workflow 
6. Select one or more alerts
7. Click Add Alert Trigger

Furthermore to use this workflow you need to install and configure the [InsightConnect Slack App](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops/).

## Usage

The workflow will run automatically any time the selected alert(s) open a new investigation in InsightIDR. Lookup results for each indicator will be send to provided Slack person or channel.

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Recorded Future|5.0.1|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Recorded Future API Documentation](https://support.recordedfuture.com/hc/en-us/categories/115000803507-Raw-API)
* [Slack](https://slack.com)
