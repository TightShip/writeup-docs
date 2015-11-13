# Webhooks

Webhooks enable you to send messages via Writeup from a third party server, as long as it accepts http. 

### Request
Your Webhook must accept POST requests over HTTP. 

### Request parameters
These parameters are always sent in the request to your Webhook:

| Name | Description |
| -- | -- |
| beacon_id  | Numerical beacon identifier |
| account_id  | Numerical account identifier |

### Response

The Webhook must return valid JSON, like this:

```
{   
    message: {
        text: "Hello {{account.username}}, This is your lucky day!"
    }
}
```
### Responce placeholders
You can add special placeholders in your response message. The system will replace them into their real values.

| Name | Description |
| -- | -- |
| \{\{recipient.username\}\}  | Recipient account username |
| \{\{recipient.displayname\}\}  | Recipient account name |

### Limitations
We check all Webhook messages for uniqueness before they're sent to the recipient. The user will not receive the same message more than once per day.