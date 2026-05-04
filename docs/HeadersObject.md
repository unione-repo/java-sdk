

# HeadersObject

Contains email headers, maximum 50. Only headers with “X-” name prefix are accepted, all other are ignored, for example X-UNIONE-Global-Language, X-UNIONE-Template-Engine. Standard headers **To,** **CC,** and **BCC** are passed without the **X-.** Yet, they are processed in a particular way and, as a result, have a number of restrictions. You can find more details about it [here](/cc-and-bcc). If our support have approved omitting standard unsubscription block for you, you can also pass List-Unsubscribe, List-Subscribe, List-Help, List-Owner, List-Archive, In-Reply-To and References headers.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**xUNIONEGlobalLanguage** | **String** | The language of the unsubscribe footer and unsubscribe page. Languages supported are: **be**, **de**, **en**, **es**, **fr**, **it**, **pl**, **pt**, **ru**, **ua**, **kz**. |  |  |  |
|**xUNIONETemplateEngine** | **String** | The template engine for handling the substitutions(merge tags), “simple”, “velocity”, “liquid” or “none”. Default value is “simple”. Has a priority over the value allowed in the “template_engine” parameter. |  |  |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


