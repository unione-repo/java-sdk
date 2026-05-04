

# WebhookEventsObject

Object containing events to notify of.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**spamBlock** | **List&lt;String&gt;** | If present then spam block events will be reported. Should contain single array element with ***** string. |  [default to new ArrayList<>()] | [\"*\"] |  |
|**emailStatus** | [**List&lt;EmailStatusEnum&gt;**](#List&lt;EmailStatusEnum&gt;) | If present then email status change events will be reported. Contains names of statuses to notify of. |  [default to new ArrayList<>()] | [\"delivered\",\"opened\",\"clicked\",\"unsubscribed\",\"subscribed\",\"soft_bounced\",\"hard_bounced\",\"spam\"] |  |



## Enum: List&lt;EmailStatusEnum&gt;

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


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


