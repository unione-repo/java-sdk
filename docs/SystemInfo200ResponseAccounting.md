

# SystemInfo200ResponseAccounting

Object with accounting period properties. Present only if the API key used for request is the user API key.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**periodStart** | **String** | Date and time of accounting period start in UTC in **YYYY-MM-DD hh:mm:ss** format. |  | 2016-08-29 09:12:33 |  true  |
|**periodEnd** | **String** | Date and time of accounting period end in UTC in **YYYY-MM-DD hh:mm:ss** format. |  | 2016-09-29 09:12:33 |  true  |
|**emailsIncluded** | **Long** | Number of emails included into accounting period. |  |  |  true  |
|**emailsSent** | **Long** | Number of emails sent during accounting period. Can be bigger than emails_included in case of overage. |  |  |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


