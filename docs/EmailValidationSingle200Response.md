

# EmailValidationSingle200Response


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**status** | **SuccessStatusString** |  |  |  |  true  |
|**email** | **String** | Email address to be checked. |  |  |  true  |
|**result** | **String** | Possible statuses:<br><br>* **valid** - the address is valid,* **invalid** - the address is invalid,* **suspicious** - the address looks suspicious,* **unknown** - could not perform validation, the domain’s mail server has not responded within the time limit. |  | suspicious |  true  |
|**cause** | **String** | Possible statuses:<br><br>* **no_mx_record** - no MX record found for the target domain,* **syntax_error** - the address syntax is invalid,* **possible_typo** - the address is likely to have a typo,* **mailbox_not_found** - the address does not exist,* **global_suppression** - the address has been marked as unreachable due to multiple previous delivery errors,* **disposable** - this is a disposable one-time email address which is usually valid for a few minutes only,* **role** - the address is not likely to belong to an actual person, but rather to a certain business staff role,* **abuse** - the address is known to be a source of a large number of complaints, sometimes issued automatically,* **spamtrap** - this email is a spam trap, it is published openly but never used for actual emails. Sending messages to such addresses has a huge negative impact on reputation score,* **smtp_connection_failed** - the domain’s SMTP server does not respond; the address may contain a typo. |  | disposable |  true  |
|**validity** | **Integer** | Validity score, from 0 to 100 (0 – invalid, 100 – valid). |  | 10 |  true  |
|**localPart** | **String** | Local part (everything preceding the @ sign). |  | user |  true  |
|**domain** | **String** | Domain name part. |  | example.com |  true  |
|**mxFound** | **Boolean** | True if the address’ domain does have an MX record, false if does not. |  | true |  true  |
|**mxRecord** | **String** | Preferred MX record for the domain. |  | 10 |  true  |
|**didYouMean** | **String** | For addresses which are likely to have typing errors (cause=possible_typo), a suggested variant with a fixed typo. |  | user@example.com |  true  |
|**processedAt** | **String** | Email check date and time, YYYY-MM-DD hh:mm:ss UTC. |  | 2023-01-01 22:14:59 |  true  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


