

# TemplateObject

Object with all the template properties.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**id** | **UUID** | Template unique identifier. If you omit the **id** field then new template will be created. If you specify the **id** field, the system will try to find a template with the specified id and edit it. |  |  |  |
|**name** | **String** | Template name. |  |  |  true  |
|**editorType** | **EditorTypeString** |  |  |  |  |
|**templateEngine** | **TemplateEngineString** |  |  |  |  |
|**globalSubstitutions** | **Map&lt;String, String&gt;** | Object for passing the substitutions(merge tags) common for all recipients - e.g., company name. If the substitution names are duplicated in object **substitutions**, the values of the variables will be taken from the object **substitutions**. The substitutions can be used in the following parameters:<br><br>* body.html* body.plaintext* body.amp* subject* from_name* options.unsubscribe_url<br><br>A substitution name can consist from latin characeters, numbers and **_** symbol, and should start with the letter. |  [default to new HashMap<>()] |  |  |
|**globalMetadata** | **Map&lt;String, String&gt;** | Object for passing the metadata common for all the recipients, such as **key**: **value**. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](https://docs.unione.io/en/web-api-ref#webhook). To group single emails into a campaign, you can use the system key 'campaign_id' with a value in the form of a non-negative decimal integer up to 128 bits or a UUID in the format 'c7703772-453e-4c77-a9ae-9a1b94051b5a'. Incorrect values will be treated as '0'. |  [default to new HashMap<>()] |  |  |
|**body** | [**BodyObject**](BodyObject.md) |  |  |  |  |
|**subject** | **String** | Email subject. |  | UniOne test email |  |
|**fromEmail** | **String** | Sender's email. |  |  |  true  |
|**fromName** | **String** | Sender's name. |  | John Smith |  |
|**replyTo** | **String** | Optional Reply-To email (in case it's different to sender's email) |  | email@example.com |  |
|**replyToName** | **String** | Optional Reply-To name (if reply_to email is specified and you want to display not only this email but also the name) |  | John Smith |  |
|**trackLinks** | **TrackLinksInteger** |  |  |  |  |
|**trackRead** | **TrackReadInteger** |  |  |  |  |
|**headers** | **HeadersObject** |  |  |  |  |
|**attachments** | [**List&lt;AttachmentsArrayInner&gt;**](AttachmentsArrayInner.md) | Optional array of attachments |  [default to new ArrayList<>()] |  |  |
|**inlineAttachments** | [**List&lt;InlineAttachmentsArrayInner&gt;**](InlineAttachmentsArrayInner.md) | Optional array of inline attachments, e.g. for including images in email instead of loading them from external URL. |  [default to new ArrayList<>()] |  |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


