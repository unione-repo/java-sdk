# ObsoleteApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**unsubscribedCheck**](ObsoleteApi.md#unsubscribedCheck) | **POST** /unsubscribed/check.json | Checks if an email is unsubscribed. |
| [**unsubscribedList**](ObsoleteApi.md#unsubscribedList) | **POST** /unsubscribed/list.json | Returns a list of all unsubscribed emails since provided date. |
| [**unsubscribedSet**](ObsoleteApi.md#unsubscribedSet) | **POST** /unsubscribed/set.json | Registers a new unsubscribed email. |



## unsubscribedCheck

> UnsubscribedCheck200Response unsubscribedCheck(unsubscribedCheckRequest)

Checks if an email is unsubscribed.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ObsoleteApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ObsoleteApi apiInstance = new ObsoleteApi(defaultClient);
        UnsubscribedCheckRequest unsubscribedCheckRequest = new UnsubscribedCheckRequest();
        unsubscribedCheckRequest.setAddress("email@example.com");
        try {
            UnsubscribedCheck200Response result = apiInstance.unsubscribedCheck(unsubscribedCheckRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ObsoleteApi#unsubscribedCheck");
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
| **unsubscribedCheckRequest** | [**UnsubscribedCheckRequest**](UnsubscribedCheckRequest.md)|  | |

### Return type

[**UnsubscribedCheck200Response**](UnsubscribedCheck200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email unsubscription status successfully returned. |  -  |
| **0** | Error occured. |  -  |


## unsubscribedList

> UnsubscribedList200Response unsubscribedList(unsubscribedListRequest)

Returns a list of all unsubscribed emails since provided date.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ObsoleteApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ObsoleteApi apiInstance = new ObsoleteApi(defaultClient);
        UnsubscribedListRequest unsubscribedListRequest = new UnsubscribedListRequest();
        unsubscribedListRequest.setDateFrom("2020-10-14");
        try {
            UnsubscribedList200Response result = apiInstance.unsubscribedList(unsubscribedListRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ObsoleteApi#unsubscribedList");
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
| **unsubscribedListRequest** | [**UnsubscribedListRequest**](UnsubscribedListRequest.md)|  | |

### Return type

[**UnsubscribedList200Response**](UnsubscribedList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of unsubscribed emails returned successfully. |  -  |
| **0** | Error occured. |  -  |


## unsubscribedSet

> UnsubscribedSet200Response unsubscribedSet(unsubscribedSetRequest)

Registers a new unsubscribed email.

After registering an email as unsubscribed all future attempts to send a message to this email will be rejected. Please note that there's no way to remove an email from unsubscribed thru the API. But you can send an email with a link to resubscribe using [email/subscribe](https://docs.unione.io/en/web-api-ref#email-subscribe) method or remove **unsubscribed** status manually on [Email Search page](https://cp.unione.io/en/user/email) in control panel (but only a limited number of unsubscribed email per day can be removed).

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ObsoleteApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ObsoleteApi apiInstance = new ObsoleteApi(defaultClient);
        UnsubscribedSetRequest unsubscribedSetRequest = new UnsubscribedSetRequest();
        unsubscribedSetRequest.setAddress("email@example.com");
        try {
            UnsubscribedSet200Response result = apiInstance.unsubscribedSet(unsubscribedSetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ObsoleteApi#unsubscribedSet");
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
| **unsubscribedSetRequest** | [**UnsubscribedSetRequest**](UnsubscribedSetRequest.md)|  | |

### Return type

[**UnsubscribedSet200Response**](UnsubscribedSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email has been unsubscribed successfully. |  -  |
| **0** | Error occured. |  -  |

