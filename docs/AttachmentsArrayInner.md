

# AttachmentsArrayInner


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**type** | **String** | Attachment type, see [MIME](https://en.wikipedia.org/wiki/MIME). If unsure, use **application/octet-stream**. |  | text/plain |  true  |
|**name** | **String** | Attachment name in the format: **name.extension**. When multiple attachments are passed, their names must be unique. The symbol ‘/’ is not allowed in attachment names. |  | readme.txt |  true  |
|**content** | **byte[]** | File contents in [base64](https://en.wikipedia.org/wiki/Base64). Maximum file size 7MB (9786710 bytes in base64). |  | [B@16a3cc88 |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


