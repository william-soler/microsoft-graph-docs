---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const sendActivityNotification = {
    topic: {
        source: 'entityUrl',
        value: 'https://graph.microsoft.com/beta/teams/{teamId}'
    },
    activityType: 'taskCreated',
    previewText: {
    	content: 'New Task Created'
    },
    recipient: {
        '@odata.type': 'microsoft.graph.aadUserNotificationRecipient',
        userId: '569363e2-4e49-4661-87f2-16f245c5d66a'
    },
    templateParameters: [
        {
            name: 'taskId',
            value: '12322'
        }
    ]
};

await client.api('/teams/{teamId}/sendActivityNotification')
	.version('beta')
	.post(sendActivityNotification);

```