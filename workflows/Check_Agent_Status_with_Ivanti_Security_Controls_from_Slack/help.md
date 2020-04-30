# Description

This workflow provides a convenient way to retrieve the status of an Ivanti Security Controls agent directly from the comfort of Slack. When triggered, the workflow fetches agent details by hostname from Ivanti Security Controls and posts the results in a Slack thread. Agent information includes hostname, agent ID, status, and last check-in time.

Sample Slack Trigger Command: 

`@Rapid7 InsightConnect check-agent-status hostname-1`

# Key Features

* Quickly identify if the Ivanti Security Controls agent is installed on a host
* Retrieve the status of the agent
* Find out the last time the agent checked in

# Requirements

* Ivanti Security Controls hostname or IP address
* Ivanti Security Controls account credentials
* InsightConnect License
* [Slack](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops)

# Documentation

## Setup

Once the workflow has been imported, edit the workflow and configure connections and orchestrators in each step.

If you do not already have a Slack connection configured, please refer to our [Help documentation](https://insightconnect.help.rapid7.com/docs/configure-slack-for-chatops).

### Usage

To trigger this workflow, @ the *Rapid7 InsightConnect* bot in Slack or send the bot a DM in the following format:

`check-agent-status hostname-1`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Ivanti Security Controls|1.0.0|1|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Ivanti Security Controls](https://www.ivanti.com/products/security-controls)
* [Slack](https://slack.com)
