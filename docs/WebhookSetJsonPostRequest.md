

# WebhookSetJsonPostRequest


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**auth** | **String** | MD5-hash of the message body, in which the value **auth** is replaced by api key of the user/project; with this field the recipient of the notification can both authenticate and verify the notification integrity |  |  |  true  |
|**eventsByUser** | [**List&lt;WebhookSetJsonPostRequestEventsByUserInner&gt;**](WebhookSetJsonPostRequestEventsByUserInner.md) | Array with only one element, containing events of a user/project. |  [default to new ArrayList<>()] |  |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


