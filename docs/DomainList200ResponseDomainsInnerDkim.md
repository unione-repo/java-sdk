

# DomainList200ResponseDomainsInnerDkim

Object describing DKIM record value and status.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**key** | **String** | DKIM signature for the domain. This property contains only the key part, you should prepend it with **k=rsa, p=** part for the record to be valid (see [domain/get-dns-records](https://docs.unione.io/en/web-api-ref#domain-get-dns-records)). |  | MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDo7 |  |
|**status** | [**StatusEnum**](#StatusEnum) | Only domains with **active** DKIM record are allowed as sender domains. |  |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;active&quot; |
| INACTIVE | &quot;inactive&quot; |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


