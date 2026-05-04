

# WebhookObject

Object with all the webhook properties.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**id** | **Integer** | Webhook unique identifier. |  |  |  true  |
|**url** | **URI** | Webhook URL. |  |  |  true  |
|**status** | **WebhookStatusString** |  |  [default to WebhookStatusString.ACTIVE] |  |  true  |
|**eventFormat** | **WebhookEventFormatString** |  |  [default to WebhookEventFormatString.JSON_POST] |  |  true  |
|**deliveryInfo** | **WebhookDeliveryInfoInteger** |  |  [default to WebhookDeliveryInfoInteger.NUMBER_0] |  |  true  |
|**singleEvent** | **WebhookSingleEventInteger** |  |  [default to WebhookSingleEventInteger.NUMBER_0] |  |  true  |
|**maxParallel** | **Integer** | Maximum quantity of permitted parallel queries to your server. The more your server can handle - the better. |  [default to 10] |  |  true  |
|**updatedAt** | **String** | Webhook properties last update date and time in UTC timezone in **YYYY-MM-DD hh:mm:ss** format. |  |  |  |
|**events** | [**WebhookEventsObject**](WebhookEventsObject.md) |  |  |  |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


