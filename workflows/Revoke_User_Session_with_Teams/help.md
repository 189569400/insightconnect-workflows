# Description

Revoke a user session forcing them to log in after their next page refresh with a command from Microsoft Teams. 

# Key Features

* Revoke a user session

# Requirements

* [Azure AD Admin](https://insightconnect.help.rapid7.com/docs/office365)
* [Microsoft Teams](https://insightconnect.help.rapid7.com/docs/microsoft-teams)

# Documentation

## Setup

Import the workflow from the Rapid7 Extension Library and proceed through the Import Workflow wizard in InsightConnect. Import plugins, create or select connections, and rename the workflow as a part of the Import Workflow wizard as necessary.

In each Microsoft Teams step set the Team and Channel you would like to send messages to. 

### Usage

This workflow uses the Microsoft Teams plugin to monitor a channel for a specific command. To trigger this workflow enter the following in that channel

`!revoke-session user@example.com`

## Technical Details

Plugins utilized by workflow:

|Plugin|Version|Count|
|----|----|--------|
|Microsoft Teams|2.0.2|5|
|String Operations|1.2.1|2|
|Azure AD Admin|2.2.0|1|
|HTML|1.2.1|1|


## Troubleshooting

_There is no troubleshooting information at this time_

# Version History

* 1.0.0 - Initial workflow

# Links

## References

* [Microsoft Office 365](https://www.office.com)
* [Azure](https://azure.microsoft.com)
* [Microsoft Teams](https://teams.microsoft.com)
* [Microsoft Teams Setup Guide](https://insightconnect.help.rapid7.com/docs/microsoft-teams)
* [Microsoft Office 365 Permissions and Setup](https://insightconnect.help.rapid7.com/docs/office365)
