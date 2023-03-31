# Notifications Service

This in a microservice that aims to send notifications to a recipient, as a user, for example. To use this application, create a .env file and add a DATABASE_URL environment, something like:

`DATABASE_URL="postgresql://johndoe:johndoe@localhost:5432/mydb?schema=public"`

## Routes

### Create a new notification (POST Method)

URL: `http://localhost:3000/notifications`
Body:
```json
{
	"recipientId": "f1f8a41b-0576-4ddb-82a8-86fc11de9190",
	"content": "Content",
	"category": "social"
}
```
### Cancel a notification (PATCH Method)
URL: `http://localhost:3000/notifications/:recipientId/cancel`

### Read a notification (PATCH Method)
URL: `http://localhost:3000/notifications/:id/read`

### Unread a notification (PATCH Method)
URL: `http://localhost:3000/notifications/:id/unread`

### Count notifications from recipient (GET Method)
URL: `http://localhost:3000/notifications/count/from/:recipientId`

### Get notifications from recipient (GET Method)
`http://localhost:3000/notifications/from/:recipientId`
