

# DomainList200ResponseDomainsInnerVerificationRecord

Object describing verification record value and status.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**value** | **String** | Record to be added **as is** to verify ownership of this domain. |  | unione-validate-hash=483bb362ebdbeedd755cfb1d4d661 |  |
|**status** | [**StatusEnum**](#StatusEnum) | Only domains with **confirmed** verification record are allowed as sender domains. |  |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| CONFIRMED | &quot;confirmed&quot; |
| UNCONFIRMED | &quot;unconfirmed&quot; |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


