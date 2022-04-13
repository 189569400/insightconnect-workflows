# Description

This workflow is meant to introduce InsightIDR users to workflows using the Orchestrator, Connections, Loop Steps, and Join Steps. It uses the IDR UBA Alert trigger and automatically identifies the type of indicator of compromise (IP address, URL, domain, or hash) that is present in the alert, looks up the indicator in VirusTotal, and produces an Artifact card that provides a summary of the findings, including a link back to the results in VirusTotal. Finally reports are send to Slack channel or person provided by user in Workflow Parameters.

To use this workflow, import and activate it in InsightConnect. Then, open an Investigation in InsightIDR and use the Take Action menu to find your Custom InsightConnect Workflow and run it! Note the workflow will only be available in investigations that include either an external IP address, URL, Domain, or process.

# Key Features

* Perform a domain, hash, URL and IP lookup automatically from any IDR alert, send results on Slack

# Requirements

* InsightIDR License
* InsightConnect License
* VirusTotal API Key
* [Slack](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops)

# Documentation

## Setup

**This workflow requires an Insight Orchestrator and an API Key from VirusTotal!**

If you have not yet deployed and activated an Orchestrator, then you'll need to either deploy the OVA or run the install script on a vanilla server. Start by [visiting our Help docs](https://docs.rapid7.com/insightconnect/install-and-activate-the-orchestrator).

Once you have activated an Orchestrator, you'll need an API key from VirusTotal.

1. [Sign up for a free VirusTotal account](https://www.virustotal.com/gui/join-us)
2. Log in and click on your user profile in the top right, then click on `API key`
3. Copy your API key

Now, import the workflow, import the VirusTotal plugin, create a connection using your VirusTotal API Key, and activate the workflow in InsightConnect!

Furthermore to use this workflow and send Slack messages you need to install and configure the [InsightConnect Slack App](https://docs.rapid7.com/insightconnect/configure-slack-for-chatops/).

As workflow is using InsightConnect's Parameters feature which allows to enter a variable once and use it multiple times throughout the workflow, you need to configure one of them in `Parameters` section on the main page of imported workflow:

* Slack Channel or Person Identifier: 
Slack channel or person identifier to send Virus Total report. E.g:
@jdoe - to send a message to person named jdoe
#integration - to send a message to channel named integration

### Usage

To run the workflow, follow the below steps:

1. Open an Investigation in InsightIDR that includes an external IP address, URL, domain, or process hash
2. Click the `Take Action` button in the Investigation to open the response panel
3. Select `Custom InsightConnect Workflows` from the `Action Category` list
4. Select the `Enrich InsightIDR Alerts with Threat Intelligence from VirusTotal to Slack` workflow (Note: If you changed the name of the workflow during the import process, then you will see a different workflow name!)
5. Select the indicator(s) of compromise to enrich
6. Click `Take Action`!

An event will be automatically added to your Investigation Timeline in InsightIDR. Click on it to see the results of your workflow!

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|VirusTotal|8.1.0|4|
|HashIt|2.0.4|1|
|Math|1.2.1|4|

## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References
* [VirusTotal](https://virustotal.com)
* [Slack](https://slack.com)
