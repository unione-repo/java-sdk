

# WebhookSetRequest


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**url** | **URI** | URL that will receive the notification when an event occurs. The URL should be unique for a user or a project. Only ASCII characters are supported for now in URL, please convert to [Punycode](https://en.wikipedia.org/wiki/Punycode) if you need to use non-ASCII characters. |  | https://yourhost.example.com/unione-webhook |  true  |
|**status** | **WebhookStatusString** |  |  [default to WebhookStatusString.ACTIVE] |  |  |
|**eventFormat** | **WebhookEventFormatString** |  |  [default to WebhookEventFormatString.JSON_POST] |  |  |
|**deliveryInfo** | **WebhookDeliveryInfoInteger** |  |  [default to WebhookDeliveryInfoInteger.NUMBER_0] |  |  |
|**singleEvent** | **WebhookSingleEventInteger** |  |  [default to WebhookSingleEventInteger.NUMBER_0] |  |  |
|**maxParallel** | **Integer** | Maximum quantity of permitted parallel queries to your server. The more your server can handle - the better. |  [default to 10] |  |  |
|**events** | [**WebhookEventsObject**](WebhookEventsObject.md) |  |  |  |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


