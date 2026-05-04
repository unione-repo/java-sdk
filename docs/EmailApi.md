# EmailApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**emailSend**](EmailApi.md#emailSend) | **POST** /email/send.json | Sends an email or a bunch of emails |
| [**emailSubscribe**](EmailApi.md#emailSubscribe) | **POST** /email/subscribe.json | Sends an email with (re)subscribe link. |



## emailSend

> EmailSend200Response emailSend(emailSendRequest)

Sends an email or a bunch of emails

While sending you can provide substitutions (merge tags), use a template, turn on read or click tracking, etc.<br>Restrictions:<br>* maximum request size is 10 MB<br>* maximum number of recipients is 500<br>* The symbol '/' is not allowed in attachment names<br>If the list of recipients contains invalid, non-existent, duplicate, or unsubscribed emails, those emails will be returned in the output parameter failed_emails, and the email will be sent to all other valid emails addresses. If all the emails addresses fall into failed_emails, sending will not be carried out and API error 204 will be returned.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EmailApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EmailApi apiInstance = new EmailApi(defaultClient);
        EmailSendRequest emailSendRequest = new EmailSendRequest();
        MessageObject mMessage = new MessageObject();
        emailSendRequest.setMessage(mMessage);
        try {
            EmailSend200Response result = apiInstance.emailSend(emailSendRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EmailApi#emailSend");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailSendRequest** | [**EmailSendRequest**](EmailSendRequest.md)|  | |

### Return type

[**EmailSend200Response**](EmailSend200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email successfully accepted for sending. |  -  |
| **0** | Error occured. |  -  |


## emailSubscribe

> SuccessResponse emailSubscribe(emailSubscribeRequest)

Sends an email with (re)subscribe link.

This method allows subscription renewal by a former subscriber who has previously unsubscribed, or who is blocked because of complaints. This method sends an email with a new subscription link to a former subscriber. Once the recipient clicks the link, their subscription status is restored.<br>There is a default restriction that limits this method to being used once a day. If you need to resubscribe more often, please ask support about it.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EmailApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EmailApi apiInstance = new EmailApi(defaultClient);
        EmailSubscribeRequest emailSubscribeRequest = new EmailSubscribeRequest();
        emailSubscribeRequest.setFromEmail("email@example.com");
        emailSubscribeRequest.setFromName("Example");
        emailSubscribeRequest.setToEmail("email@example.com");
        try {
            SuccessResponse result = apiInstance.emailSubscribe(emailSubscribeRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EmailApi#emailSubscribe");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **emailSubscribeRequest** | [**EmailSubscribeRequest**](EmailSubscribeRequest.md)|  | |

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email successfully accepted for sending. |  -  |
| **0** | Error occured. |  -  |

