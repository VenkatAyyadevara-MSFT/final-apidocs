# Update message

Update the properties of message object.
### Prerequisites
One of the following **scopes** is required to execute this API: _Mail.ReadWrite_ 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/<id | userPrincipalName>/messages/<id>
PATCH /drive/root/createdByUser/messages/<id>
PATCH /drive/root/lastModifiedByUser/messages/<id>
```
### Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer <token>. Required. |
| Content-Type | string  | Nature of the data in the body of an entity. Required. |
### Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are 

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|bccRecipients|Recipient|Updatable only if IsDraft = true|
|categories|String||
|ccRecipients|Recipient|Updatable only if IsDraft = true|
|from|Recipient|Updatable only if IsDraft = true|
|importance|String| Possible values are: `Low`, `Normal`, `High`.|
|isRead|Boolean||
|replyTo|Recipient|Updatable only if IsDraft = true|
|sender|Recipient|Updatable only if IsDraft = true|
|toRecipients|Recipient|Updatable only if IsDraft = true|
|body|ItemBody|Updatable only if IsDraft = true|
|isDeliveryReceiptRequested|Boolean||
|isReadReceiptRequested|Boolean||
|subject|String|Updatable only if IsDraft = true|

### Response
If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_message"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/<id>
Content-type: application/json
Content-length: 248

{
  "subject": "subject-value",
  "body": {
    "contentType": {
    },
    "content": "content-value"
  }
}
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": {
    },
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->