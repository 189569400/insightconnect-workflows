# Description

This workflow forwards IDR alerts to a Slack channel.

# Key Features

* Send IDR alert to Slack channel

# Requirements

* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)
* [InsightIDR](https://www.rapid7.com/products/insightidr/)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

There is one workflow parameter you will need to configure in order to complete setup of your workflow:
* `Slack Channel`: The Slack channel name in your environment where the workflow should send InsightIDR Alerts

After the workflow is activated [create a new alert trigger in InsightIDR](https://docs.rapid7.com/insightidr/alert-triggers#configure-alert-triggers) and select all alert types that should be forwarded to Slack.

### Usage

You can also manually trigger this workflow from the investigation. To do this click the **Take Action** button and choose **Custom InsightConnect Workflows**. From the list select the imported workflow.

## Technical Details

This workflow forwards IDR Alerts to the Slack channel configured on the Parameters tab.

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.1 - Added Parameters
* 1.0.0 - Initial workflow

# Links

## References

* [Slack](https://slack.com)
* [InsightIDR](https://www.rapid7.com/products/insightidr/)
