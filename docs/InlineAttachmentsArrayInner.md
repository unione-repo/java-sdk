

# InlineAttachmentsArrayInner


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**type** | **String** | Attachment type, see [MIME](https://en.wikipedia.org/wiki/MIME). If unsure, use **application/octet-stream**. |  | image/gif |  true  |
|**name** | **String** | Attachment content id. For example, **name**=**IMAGECID1** should be referenced in HTML like <img src=**cid:IMAGECID1**>. |  | IMAGECID1 |  true  |
|**content** | **byte[]** | File contents in [base64](https://en.wikipedia.org/wiki/Base64). Maximum file size 7MB (9786710 bytes in base64). |  | [B@696b52bc |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


