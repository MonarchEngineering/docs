---
title: "Connect Airtop with Make"
sidebarTitle: "Make.com"
icon: "/images/connections/make-logo.svg"
description: "Connect Airtop Agents with Make to create code-free automations and integrate with hundreds of apps and services."
keywords: ["Make", "connections", "integrations"]
---

## Overview

[Make](https://www.make.com) is a visual platform that allows you to design, build, and automate workflows without writing code. After you **deploy** your Agent, you can trigger it directly from Make and process the results within your scenarios.

## Run your deployed Agent from Make

<Steps>
  <Step title="Open connection settings">
    Navigate to your Agent's build page and click **Connect**.
    <Frame>
      <img src="/images/connections/make-open-connect-settings.gif" alt="Open connection settings for Make" />
    </Frame>
  </Step>

  <Step title="Add the Airtop module">
    In your Make scenario, add the Airtop **Run Agent** module.
    <Frame>
      <img src="/images/connections/make-add-agent-module.png" alt="Add Run Agent module in Make" />
    </Frame>
  </Step>

  <Step title="Configure the Webhook URL">
    Enter the Webhook URL from the connection modal into the **Webhook URL** field.
    ```bash
    # Example of a Webhook URL
    https://api.airtop.ai/api/hooks/agents/{agent-id}/webhooks/{webhook-id}
    ```
  </Step>

  <Step title="Set Agent parameters">
    Copy the Agent's parameters from the connection modal and paste them into the **Parameters** field in the Make module. Adjust the values as needed.
    ```json
    // Example of Agent parameters
    {
      "configVars": {
        // Your Agent's configuration variables
      }
    }
    ```
    When configured correctly, the module settings should look like this:
    <Frame>
      <img src="/images/connections/make-module-config.png" alt="Make module configuration" />
    </Frame>
  </Step>

  <Step title="Run the scenario">
    Save your changes and run the scenario to test the integration.
  </Step>
</Steps>
