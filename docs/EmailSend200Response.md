

# EmailSend200Response


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**status** | **SuccessStatusString** |  |  |  |  true  |
|**jobId** | **String** | Job identifier, might be useful for investigating errors. |  | 1ZymBc-00041N-9X |  true  |
|**emails** | **List&lt;String&gt;** | Array of recipients emails successfully accepted for sending. |  [default to new ArrayList<>()] |  |  |
|**failedEmails** | **List&lt;Map&lt;String, String&gt;&gt;** | Object with emails rejected for sending as property names and their statuses as property values, e.g.: {**email1@gmail.com**: **temporary_unavailable**}. Possible statuses:<br><br>* __unsubscribed__ - specified email is unsubscribed;* __invalid__ - the email does not exist or has been entered incorrectly;* __duplicate__ - the email already exists in the request, email duplicating is prevented;* __temporary_unavailable__ - the email address is unavailable. This means that over the next three days sending to this address will return an error. Email may be temporarily unavailable due to several reasons, e.g.:<br>        1. a previous email has been rejected by the recipient's server for spam;* the recipient's mailbox is full or is not used;* recipient's domain does not accept mail;* sending server was rejected due to blacklisting;* __permanent_unavailable__ - the email address is permanently unavailable or unsubscribed globally.* __complained__ - the recipient reported spam in the previous emails;* __blocked__ - sending to the email is prohibited by administration of UniOne.<br><br>We may added new statuses in the future. |  [default to new ArrayList<>()] | {\"email1@gmail.com\":\"temporary_unavailable\",\"bad@address\":\"invalid\",\"email@example.com\":\"duplicate\",\"root@example.org\":\"permanent_unavailable\",\"olduser@example.net\":\"unsubscribed\"} |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


