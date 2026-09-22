# GitHub Security Alert MVP

This folder contains the MVP setup for forwarding GitHub security alerts to an automation webhook such as Make.com.

## Flow

GitHub security event → Make.com Custom Webhook → Slack/Discord/Email notification

## GitHub events

Enable these webhook events on the repository:
- Dependabot alerts
- Secret scanning alerts
- Code scanning alerts

Use application/json and keep the webhook active.

## Make.com setup

1. Create a Make.com scenario.
2. Add Webhooks → Custom webhook.
3. Name it GitHub Security Alert.
4. Copy the generated webhook URL.
5. Use Redetermine data structure and send a sample GitHub security event.
6. Add Slack, Discord, or Email as the notification step.
7. Map the title, alert type, severity, and URL from the incoming payload.

## Security

Do not commit the Make webhook URL if it contains a secret/token. Store secrets in the automation platform or GitHub Secrets where applicable.

## Test

After activating the webhook, generate or change a security-alert state in GitHub and confirm that Make receives the event and the notification action runs.

## Repository

Target repository: Afo2025/FoltechSolutions.github.io
