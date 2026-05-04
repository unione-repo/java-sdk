

# WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventData

Object with different event properties depending on **event_name**. Below you can see all the properties, **transactional_email_status**-related first and then **transactional_spam_block**-related.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**jobId** | **String** | Job identifier returned earlier by [email/send](https://docs.unione.io/en/web-api-ref#email-send) method. Property exists only if event_name=**transactional_email_status**. |  | 1ZymBc-00041N-9X |  |
|**metadata** | **Map&lt;String, String&gt;** | Metadata passed in [email/send](https://docs.unione.io/en/web-api-ref#email-send) method in recipients.metadata or global_metadata properties. This property exists only if event_name=**transactional_email_status**. |  [default to new HashMap<>()] | {\"campaign_id\":\"c77f4f4e-3561-49f7-9f07-c35be01b4f43\",\"customer_hash\":\"b253ac7\"} |  |
|**email** | **String** | Recipient's email. This property exists only if event_name=**transactional_email_status**. |  |  |  |
|**status** | [**StatusEnum**](#StatusEnum) | Email delivery status. This property exists only if event_name=**transactional_email_status**. Possible values are:<br>__accepted__ — the message has been accepted, but not sent yet.<br>__sent__ — the message has been sent, but not delivered yet.<br>__delivered__ — the message has been delivered. It can be changed to “opened”, “clicked”, “unsubscribed”, “subscribed” or “spam”.<br>__opened__ — the message has been delivered and read. It can be changed to “clicked”, “unsubscribed”, “subscribed” or “spam”.<br>__clicked__ — the message has been delivered, read, and at least one of the links in email has been clicked. It can be changed to “unsubscribed”, “subscribed” or “spam”.<br>__unsubscribed__ — the message has been delivered to the recipient and read, but then the recipient unsubscribed. It can be changed to “subscribed”.<br>__subscribed__ — the message has been delivered to the recipient and read, but then the recipient unsubscribed and subscribed again. It can be changed to “unsubscribed”.<br>__soft_bounced__ — temporary delivery failure. UniOne will try to deliver the message during 48 hours. In case of success the status changes to “delivered”, in case of failure to deliver during 48 hours message status changes to “hard_bounced”.<br>__hard_bounced__ — failed to deliver the message, there will be no delivery attempts. It's a final status. There are a lot of possible reasons, you can use SMTP response from delivery_info.destination_response field or UniOne internal reason classification from delivery_info.delivery_status field to analyze the reason.<br>__spam__ — the message has been delivered, but it was reported as spam by the recipient. UniOne can receive and process the spam complaint from several domains, including msn.com, outlook.com, hotmail.com, live.com, ukr.net, yahoo.com, aol.com using [FBL](https://en.wikipedia.org/wiki/Feedback_loop_(email)). |  |  |  |
|**eventTime** | **String** | Event date & time in UTC time zone in **YYYY-MM-DD hh:mm:ss** format. This property exists only if event_name=**transactional_email_status**. |  | 2020-12-24 16:05:58 |  |
|**url** | **URI** | URL for **opened** and **clicked** statuses. This property exists only if event_name=**transactional_email_status**. |  |  |  |
|**deliveryInfo** | [**WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventDataDeliveryInfo**](WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventDataDeliveryInfo.md) |  |  |  |  |
|**blockTime** | **String** | Spam block date & time in UTC time zone in **YYYY-MM-DD hh:mm:ss** format. This property exists only if event_name=**transactional_spam_block**. |  | 2020-12-24 16:05:58 |  |
|**blockType** | [**BlockTypeEnum**](#BlockTypeEnum) | Spam block type, either single or multiple sending SMTP. For single sending SMTP block in common pool UniOne retries several other SMTPs. This property exists only if event_name=**transactional_spam_block**. |  |  |  |
|**domain** | **String** | Domain that blocked sending. This property exists only if event_name=**transactional_spam_block**. |  | example.com |  |
|**smTPBlocksCount** | **Integer** | Number of sending SMTPs blocked. This property exists only if event_name=**transactional_spam_block**. |  |  |  |
|**domainStatus** | [**DomainStatusEnum**](#DomainStatusEnum) | Whether it's a block or unblock event. This property exists only if event_name=**transactional_spam_block**. |  |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| SENT | &quot;sent&quot; |
| DELIVERED | &quot;delivered&quot; |
| OPENED | &quot;opened&quot; |
| CLICKED | &quot;clicked&quot; |
| UNSUBSCRIBED | &quot;unsubscribed&quot; |
| SUBSCRIBED | &quot;subscribed&quot; |
| SOFT_BOUNCED | &quot;soft_bounced&quot; |
| HARD_BOUNCED | &quot;hard_bounced&quot; |
| SPAM | &quot;spam&quot; |



## Enum: BlockTypeEnum

| Name | Value |
|---- | -----|
| ONE_SMTP | &quot;one_smtp&quot; |
| ALL_SMTP | &quot;all_smtp&quot; |



## Enum: DomainStatusEnum

| Name | Value |
|---- | -----|
| BLOCKED | &quot;blocked&quot; |
| UNBLOCKED | &quot;unblocked&quot; |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


