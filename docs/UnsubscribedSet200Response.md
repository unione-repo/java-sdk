

# UnsubscribedSet200Response


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**status** | **SuccessStatusString** |  |  |  |  true  |
|**address** | **String** | The unsubscribed email. |  |  |  true  |
|**message** | [**MessageEnum**](#MessageEnum) | Unsubscription process details:<br><br>* **unsubscribed** if email has just been unsubscribed,* **was inactive** if it was inactive due some reason,* **was unsubscribed** if it already was unsubscribed before the call,* **added and unsubscribed** if it's a new email without status history and it was added and then unsubscribed immediately. |  |  |  true  |



## Enum: MessageEnum

| Name | Value |
|---- | -----|
| UNSUBSCRIBED | &quot;unsubscribed&quot; |
| WAS_INACTIVE | &quot;was inactive&quot; |
| WAS_UNSUBSCRIBED | &quot;was unsubscribed&quot; |
| ADDED_AND_UNSUBSCRIBED | &quot;added and unsubscribed&quot; |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


