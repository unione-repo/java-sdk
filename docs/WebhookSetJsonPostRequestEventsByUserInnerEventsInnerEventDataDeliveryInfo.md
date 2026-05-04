

# WebhookSetJsonPostRequestEventsByUserInnerEventsInnerEventDataDeliveryInfo

Object with detailed delivery info.Event date & time in UTC time zone in **YYYY-MM-DD hh:mm:ss** format. This property exists only if webhook has delivery_info proeprty set to 1 and event_name=**transactional_email_status**.

## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**deliveryStatus** | **String** | UniOne internal detailed delivery status. Some possible values are:<br>__err_user_unknown__ -- email address doesn't exist;<br>__err_user_inactive__ -- email address isn't used anymore;<br>__err_will_retry__ -- email was temporary rejected, delivery will be retried later;<br>__err_mailbox_discarded__ -- email address was active earlier, but now it's deleted;<br>__err_mailbox_full__ -- mailbox is full;<br>__err_spam_rejected__ -- email was rejected as a spam;<br>__err_blacklisted__ -- email was rejected because sender IP or sender domain is found in a black list;<br>__err_too_large__ -- email size is over limit, according to recipient's server;<br>__err_unsubscribed__ -- email was unsubscribed;<br>__err_unreachable__ -- numerous delivery failures lead to mark this email address as permanently unavailable;<br>__err_skip_letter__ -- sending has been canceled because the email address is temporarily unavailable;<br>__err_domain_inactive__ -- the domain does not accept mail or does not exist;<br>__err_destination_misconfigured__ -- the domain does not accept mail due to incorrect settings on the recipient’s side, and the server’s response contains information about a cause that can be fixed (for example, an inoperative blacklist is used, etc.);<br>__err_delivery_failed__ -- delivery failed due to other reasons;<br>__err_spam_skipped__ -- sending has been canceled because the campaign has been blocked as a spam;<br>__err_lost__ -- the message was not sent due to inconsistency of its parts or it has been lost because of the failure on our side. The sender needs to re-send the letter on his own, since the original has not been saved;<br>We reserve the right to change or add internal delivery statuses as we need, so the following list is provided as an example only, without any description: ok_sent, ok_delivered, ok_read, ok_link_visited, ok_unsubscribed, ok_resubscribed, ok_spam_folder, ok_fbl, not_sent, skip_dup_unreachable, skip_dup_temp_unreachable, skip_dup_mailbox_full, err_spam_removed, err_resend, err_unknown, err_retry_letter, err_src_invalid, err_dest_invalid, err_not_available, err_internal, err_no_dns, err_no_smtp, err_giveup. |  |  |  |
|**destinationResponse** | **String** | SMTP response. |  |  |  |
|**userAgent** | **String** | User agent of recipient. Present only if detected for **clicked** and **opened** statuses. |  | Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/57.0.2987.133 Safari/537.36 |  |
|**ip** | **String** | Recipient's IP address. Present only if detected for **clicked** and **opened** statuses. |  | 111.222.33.44 |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


