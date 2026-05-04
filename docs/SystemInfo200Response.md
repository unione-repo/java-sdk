

# SystemInfo200Response


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**status** | **SuccessStatusString** |  |  |  |  true  |
|**userId** | **Integer** | Unique user identifier. |  | 11344 |  true  |
|**email** | **String** | Email of the user. |  |  |  true  |
|**projectId** | **String** | Unqiue project identifier, ASCII string up to 36 characters long. Present only if the API key used for request is the project API key. |  | 6123462132634 |  |
|**projectName** | **String** | Project name, unique for user account. Present only if the API key used for request is the project API key. |  | Project 1A |  |
|**projectAccounting** | [**ProjectAccountingObject**](ProjectAccountingObject.md) |  |  |  |  |
|**accounting** | [**SystemInfo200ResponseAccounting**](SystemInfo200ResponseAccounting.md) |  |  |  |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


