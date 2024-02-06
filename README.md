# eks-slack-notifications
A tool that checks your AWS EKS cluster's add-ons for updates and sends a report to Slack if any updates are found.

In Lambda: Configuration > Environment variables

Add the following: 

CLUSTER_NAME: YOUR_CLUSTER_NAME

CLUSTER_VERSION: YOUR_CLUSTER_VERSION

SLACK_CHANNEL: #SLACKCHANNEL

SLACK_USERNAME: YOUR_SLACK_NAME (i.e., Jane Doe)

SLACK_WEBHOOK_URL: YOUR_WEBHOOK_URL




To create a webhook URL in Slack, follow these steps:
1. Click on the upper left corner > Go > Workflow Builder
2. Click 'Create Workflow'
3. Click 'From Webhook'
4. Click 'Set Up Variables'
5. Add the following:
   Key: text
   Data type: Text
6. Click 'Done' and then 'Continue'
7. Click the circle below the "Starts with a webhook" to add a new step.
8. Click Messages > Send an "only visible to you" message
9. Select your Slack Channel and your name
10. Under "Add a message", make sure you insert the 'text' variable we made in a previous step. You can format the message however else you'd like.
    Example:
    EKS Add-on Report:
    | {text}
