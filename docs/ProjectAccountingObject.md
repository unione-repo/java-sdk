

# ProjectAccountingObject

Object with email counter properties. Present only if the API key used for request is the user API key.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**emailCounter** | **Integer** | Project's email counter value. It increases on every email sent. |  |  |  true  |
|**emailCounterLimit** | **Integer** | Allows you to limit the number of emails sent by the project. The sending stops when the limit is reached. Any non-negative 64-bit integer is acceptable. 0 means no limit. |  |  |  true  |
|**emailCounterMode** | [**EmailCounterModeEnum**](#EmailCounterModeEnum) | 'default' - the counter resets to zero automatically at the beginning of each accounting period. 'permanent' - the counter never resets automatically. |  [default to EmailCounterModeEnum.DEFAULT] |  |  true  |



## Enum: EmailCounterModeEnum

| Name | Value |
|---- | -----|
| DEFAULT | &quot;default&quot; |
| PERMANENT | &quot;permanent&quot; |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


