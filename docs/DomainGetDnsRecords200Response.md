

# DomainGetDnsRecords200Response


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**status** | **SuccessStatusString** |  |  |  |  true  |
|**domain** | **String** | Domain to get DNS records for. |  | example.com |  true  |
|**verificationRecord** | **String** | Record to be added **as is** to verify ownership of this domain. |  | unione-validate-hash=483bb362ebdbeedd755cfb1d4d661 |  true  |
|**dkim** | **String** | DKIM signature for the domain. This property contains only the key part, you should prepend it with **k=rsa, p=** part for the record to be valid (see example). |  | MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDo7 |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


