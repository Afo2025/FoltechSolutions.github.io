# GitHub Security Alert MVP

This MVP forwards GitHub security-alert webhook events to a Make.com Custom Webhook and then to a notification channel such as Slack, Discord, or email.

## Architecture

```
GitHub security alert
        |
        | HTTPS webhook
        v
Make.com Custom Webhook
        |
        v
Notification module
(Slack / Discord / Email)
```

GitHub supports dedicated webhook events for:
- `dependabot_alert`
- `secret_scanning_alert`
- `code_scanning_alert`

These events can fire when security alerts are created or their state changes. GitHub documents these as security-alert webhook events.

## Make.com

Use the existing Make Custom Webhook URL supplied for this project, but **do not commit the URL to this repository** because webhook URLs can act as an endpoint credential.

In Make:

1. Open the scenario containing the Custom Webhook named **GitHub Security Alert**.
2. Confirm the Custom Webhook is present.
3. Use **Re-determine data structure** if Make needs a sample payload.
4. Add the notification module after the webhook.
5. Turn the scenario **ON** and use immediate webhook processing.
6. Map the GitHub event fields to the notification message.

### Recommended notification template

**Title**
`🚨 GitHub Security Alert — {{repository.full_name}}`

**Body**
```
Event: {{github_event}}
Action: {{action}}
Repository: {{repository.full_name}}
Alert URL: {{alert.html_url}}
Severity: {{alert.severity}}
```

Because GitHub uses different payload structures for Dependabot, secret-scanning, and code-scanning events, do not assume that every event contains the same `alert` fields. Map fields from each actual sample received by Make.

## GitHub webhook

On the repository:

**Settings → Webhooks → Add webhook**

Set:

- Payload URL: the Make Custom Webhook URL
- Content type: `application/json`
- SSL verification: enabled
- Active: enabled
- Events: select only the security events required by this MVP:
  - Dependabot alerts
  - Secret scanning alerts
  - Code scanning alerts

GitHub recommends subscribing only to the events required by the integration and using a webhook secret where supported.

## Testing

1. Turn the Make scenario on.
2. In GitHub, open the repository's Security and quality area.
3. Use an existing alert whose state can safely be changed, or generate a test event in a test repository.
4. Confirm GitHub records a successful webhook delivery.
5. Confirm Make receives the event.
6. Confirm the notification module sends the formatted alert.

## Important limitation

The GitHub connector available to this workspace can modify repository contents, but it does not expose repository webhook administration. Therefore the actual **Settings → Webhooks** registration and the Make scenario's ON/OFF state must be completed in the respective service account.

Target repository: **Afo2025/FoltechSolutions.github.io**
