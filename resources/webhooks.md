---
icon: key
order: 100
title: "Webhooks"
---
# Webhooks
Get notified as soon as someone votes for your listing on Discollab! We'll send a `POST` request to your provided endpoint.
## Get Started
Your first step is to visit our [dashboard](https://discollab.org/dashboard) and select the server or bot you want a vote webhook for. Once selected, scroll all the way down and look for a button named <b>Show More Options</b>, click it. At the bottom of this extended section, you'll see 2 inputs where you can provide us with your endpoint URL and its token.
## Security
To verify that a webhook came from Discollab, be sure to check the `Authorization` header. It should contain the token you provided in the dashboard.

If you're using a firewall, be sure to whitelist the IP `51.222.204.155`.

## Structure
For servers:

| Field                          | Description                                                                                                |
|--------------------------------|-----------------------------------------------------------------------------------------------------------|
| `guild_id`                   | The ID of the server that was voted for.                                                                                |
| `user_id`                   | The ID of the user that voted for the server.                                                                                |
| `username` | The username of the user that voted for the server. |
| `voted_on` | The time the user voted for the server. |
| `times_voted` | How many times the user has voted for the server. |

For bots:

| Field                          | Description                                                                                                |
|--------------------------------|-----------------------------------------------------------------------------------------------------------|
| `client_id`                   | The ID of the bot that was voted for.                                                                                |
| `user_id`                   | The ID of the user that voted for the bot.                                                                                |
| `username` | The username of the user that voted for the bot. |
| `voted_on` | The time the user voted for the bot. |
| `times_voted` | How many times the user has voted for the bot. |