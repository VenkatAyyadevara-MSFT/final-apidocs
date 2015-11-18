# externalReferenceCollection resource type

The ExternalReferenceCollection* resource represents the collection of references on a task. It is part of the [task details](taskdetails.md) object. The value in the property-value pair is the [externalReference](externalreference.md) object.

*Note that this is an Open Type.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.externalreferencecollection"
}-->

```json
{
}

```

```json
{
}

```
### Properties
Properties of an Open Type can be defined by the client. In this case, the client must provide **valid URLs** based on the **HTTP/HTTPS** protocols as properties and their values must be the [externalReference](externalreference.md) objects. Based on OData, property names in Open Types cannot contain the following characters: `.`, `:`, `%`  so they need to be encoded. Example is shown above. To remove a reference, set the value of the property to `null`

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "externalReferenceCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->