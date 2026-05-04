

# SuppressionList200Response


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**status** | **SuccessStatusString** |  |  |  |  true  |
|**suppressions** | [**List&lt;SuppressionListObject&gt;**](SuppressionListObject.md) | Array of suppression objects. |  [default to new ArrayList<>()] |  |  true  |
|**cursor** | **String** | The parameter indicates from which position the selection is to be started. Must be empty or omitted for the first data chunk. In order to get subsequent chunks, you must set the **cursor** parameter in your request, using the value received in response to the previous request. |  | Ajfb6Hvdkn3hdhhvG57xbdufhG5 |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


