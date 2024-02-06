# EKS Slack Notifications

EKS Slack Notifications is a tool that checks your AWS EKS cluster's add-ons for updates and sends a report to Slack if any updates are found.

## Lambda Configuration

In Lambda > ThisFunction > Configuration > Environment variables, add the correct values for the following environment variables:

- `CLUSTER_VERSION`: Replace with your cluster's version.
- `CLUSTER_NAME`: Replace with your EKS cluster name.
- `SLACK_CHANNEL`: Replace with your desired Slack channel name.
- `SLACK_USERNAME`: Replace with your desired Slack username.
- `SLACK_WEBHOOK_URL`: Replace with your Slack webhook URL.

You can also complete this step by putting the values directly into the CloudFormation template.

## Setting Up Slack Webhook

To create a webhook URL in Slack, follow these steps:

1. Click on the upper left corner > Go > Workflow Builder.
2. Click "Create Workflow"
3. Click "From Webhook"
4. Click "Set Up Variables"
5. Add the following:
   - **Key:** `text`
   - **Data type:** Text
6. Click "Done" and then "Continue"
7. Click the circle below the "Starts with a webhook" to add a new step.
8. Click "Messages" > "Send an 'only visible to you' message"
9. Select your Slack Channel and your name.
10. Under "Add a message," make sure you insert the `{text}` variable we made in a previous step. You can format the message however else you'd like.

### Example

```
EKS Add-on Report:
| {text}
```
