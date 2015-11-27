# Webhooks

Webhooks enable you to send messages via Writeup from a third party server, as long as it accepts http. 

### Request
Your Webhook must accept POST requests over HTTP. 

### Request parameters
These parameters are always sent in the request to your Webhook:

| Name | Description |
| -- | -- |
| beacon_id  | Numerical beacon identifier |
| account_id  | Id of recipient |

### Response

The Webhook must return valid JSON. Max response time is 5000ms.

```
{   
    message: {
        text: "Hello {{recipient.name}}, This is beacon {{beacon.name}}"
    }
}
```
### Responce placeholders
You can add special placeholders in your response message. The system will replace them into their real values.

| Name | Description |
| -- | -- |
| \{\{recipient.username\}\}  | Recipient account username |
| \{\{recipient.name\}\}  | Recipient account name |
| \{\{beacon.name\}\}  | Beacon name |

### Limitations
We check all Webhook messages for uniqueness before they're sent to the recipient. The user will not receive the same message more than once per day.