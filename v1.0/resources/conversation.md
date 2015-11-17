# conversation resource type

A conversation is a collection of [threads](#ConversationThreadResource). All threads and posts in a conversation share the same subject.

### Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[Get conversation](../api/conversation_get.md) | [conversation](conversation.md) |Read properties and relationships of conversation object.|
|[Create thread](../api/conversation_post_threads.md) |[conversationThread](conversationthread.md)| Create a new thread by posting to the threads collection.|
|[List threads](../api/conversation_list_threads.md) |[conversationThread](conversationthread.md) collection| Get a thread object collection.|
|[Update](../api/conversation_update.md) | [conversation](conversation.md)  |Update conversation object. |
|[Delete](../api/conversation_delete.md) | None |Delete conversation object. |


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|hasAttachments|Boolean|Indicates whether any of the posts within this Conversation has at least one attachment.|
|id|String|The group's unique identifier. Read-only.|
|lastDeliveredDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|preview|String|A short summary from the body of the latest post in this converstaion.|
|topic|String|The topic of the conversation. This property can be set when the conversation is created, but it cannot be updated.|
|uniqueSenders|String collection|All the users that sent a message to this Conversation.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|threads|[conversationThread](conversationthread.md) collection|A collection of all the conversation threads in the conversation. A navigation property. Read-only. Nullable.|


### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "threads"
  ],
  "@odata.type": "microsoft.graph.conversation"
}-->

```json
{
  "hasAttachments": true,
  "id": "string (identifier)",
  "lastDeliveredDateTime": {"@odata.type": "microsoft.graph.dateTimeOffset"},
  "preview": "string",
  "topic": "string",
  "uniqueSenders": ["string"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->