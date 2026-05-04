

# WebhookSetJsonPostRequestEventsByUserInner


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**userId** | **Integer** | Unique user identifier. |  | 11344 |  true  |
|**projectId** | **String** | Project identifier, present only if webhook was registered for the project using project API key. |  |  |  |
|**projectName** | **String** | Project name, present only if webhook was registered for the project using project API key. |  |  |  |
|**events** | [**List&lt;WebhookSetJsonPostRequestEventsByUserInnerEventsInner&gt;**](WebhookSetJsonPostRequestEventsByUserInnerEventsInner.md) | Array of events reported by webhook. |  [default to new ArrayList<>()] |  |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


