

# MessageObjectRecipientsInner


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**email** | **String** | Recipient email |  |  |  true  |
|**substitutions** | **Map&lt;String, String&gt;** | Object to pass the substitutions(merge tags) for the recipient (e.g. recipient name, discount code, password change link, etc. See [Template engines](https://docs.unione.io/en/template-engines)). The substitutions can be used in the following parameters:<br><br>* body.html* body.plaintext* body.amp* subject* from_name* headers[**List-Unsubscribe**]* options.unsubscribe_url<br><br>A substitution name can consist from latin characters, numbers and **_** symbol, and should start with the letter. There's a special substitution **to_name** which is used to put recipent's name like **Name Surname** to include it to SMTP header **To** in the form **Name Surname <email@example.com>**. The **to_name** length is limited to 78 symbols. |  [default to new HashMap<>()] | {\"CustomerId\":\"12452\",\"to_name\":\"John Smith\"} |  |
|**metadata** | **Map&lt;String, String&gt;** | Object for passing the metadata, such as **key**: **value**. Max key quantity: 10. Max key length: 64 symbols. Max value length: 1024 symbols. The metadata is returned by [webhook](https://docs.unione.io/en/web-api-ref#webhook) and [event-dump](https://docs.unione.io/en/web-api-ref#event-dump) methods. If you pass strign up to 128 bit with **campaign_id** field name (name is configurable thru support), it will be considered as campaign identifier in statistics. |  [default to new HashMap<>()] | {\"campaign_id\":\"c77f4f4e-3561-49f7-9f07-c35be01b4f43\",\"customer_hash\":\"b253ac7\"} |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


