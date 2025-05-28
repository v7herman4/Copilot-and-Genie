# F1 Racing Agent Genie Databricks Installation Guide

## Overview

With the advent of Agents for Everything, Microsoft has enabled a generative AI experience for Databricks for Azure named Genie. Following a multi-agent architecture low-code Agent creators can extract meaningful data from Databricks with a simple Power Automate Flow and HTTP Connector.

The Racing Agent is an Agent created with Copilot Studio and published to Microsoft Teams. It uses the Conversational Boosting Topic that calls a Agent Flow. This Flow uses an HTTP Connector to call the Genie API. The Genie API will interpret the Utterance from the caller, construct the appropriate query and return the results in a structured JSON string. The string will be parsed in the Copilot Agent leveraging an AI Prompt and then reflected back to the user in Microsoft Teams.

## Prepare for Installation

If you don’t have a working Databricks repository in Azure, create one.

Import the Azure Databricks Formula 1 Racing Data Engineering solution as per this GitHub repo.

<https://github.com/shubham14yadav/Azure-Databricks-Formula-1-Racing-Data-Engineering>

Configure the Genie Conversation API per this article:

[Set up and manage an AI/BI Genie space | Databricks Documentation](https://docs.databricks.com/aws/en/genie/set-up)

Note the following items from the Genie API setup as they’ll be required for the installation of the Microsoft Copilot Studio solution:

1. Genie base URL
2. Genie Space Id
3. Genie Bearer

## Import the solution into a Power Platform Environment

1. Import the unmanaged solution: F1RacingAgentGenieDatabricks_N_N_N_N.zip
2. Ensure all connection references are validated and created.
3. Set the Environment Variables from the Genie API
4. Publish All Customizations.
5. Open the Agent in Copilot Studio
6. Publish the Agent
