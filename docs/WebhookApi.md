# WebhookApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**webhookDelete**](WebhookApi.md#webhookDelete) | **POST** /webhook/delete.json | Deletes an event notification handler |
| [**webhookGet**](WebhookApi.md#webhookGet) | **POST** /webhook/get.json | Gets properties of a [webhook](https://docs.unione.io/en/web-api-ref#webhook). |
| [**webhookList**](WebhookApi.md#webhookList) | **POST** /webhook/list.json | List all or some [webhooks](https://docs.unione.io/en/web-api-ref#webhook) (event notification handlers) of a user or a project. |
| [**webhookSet**](WebhookApi.md#webhookSet) | **POST** /webhook/set.json | Sets or edits a [webhook](https://docs.unione.io/en/web-api-ref#webhook), i.e. an event notification handler. |



## webhookDelete

> SuccessResponse webhookDelete(webhookGetRequest)

Deletes an event notification handler

You can also temporarily deactivate webhook without deleting it by setting it's status to **disabled** in [webhook/set](https://docs.unione.io/en/web-api-ref#webhook-set) method.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.WebhookApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        WebhookApi apiInstance = new WebhookApi(defaultClient);
        WebhookGetRequest webhookGetRequest = new WebhookGetRequest();
        webhookGetRequest.setUrl("https://example.com/webhook");
        try {
            SuccessResponse result = apiInstance.webhookDelete(webhookGetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhookApi#webhookDelete");
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
| **webhookGetRequest** | [**WebhookGetRequest**](WebhookGetRequest.md)|  | |

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
| **200** | Webhook deleted successfully. |  -  |
| **0** | Error occured. |  -  |


## webhookGet

> WebhookSet200Response webhookGet(webhookGetRequest)

Gets properties of a [webhook](https://docs.unione.io/en/web-api-ref#webhook).

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.WebhookApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        WebhookApi apiInstance = new WebhookApi(defaultClient);
        WebhookGetRequest webhookGetRequest = new WebhookGetRequest();
        webhookGetRequest.setUrl("https://example.com/webhook");
        try {
            WebhookSet200Response result = apiInstance.webhookGet(webhookGetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhookApi#webhookGet");
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
| **webhookGetRequest** | [**WebhookGetRequest**](WebhookGetRequest.md)|  | |

### Return type

[**WebhookSet200Response**](WebhookSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook returned successfully. |  -  |
| **0** | Error occured. |  -  |


## webhookList

> WebhookList200Response webhookList(webhookListRequest)

List all or some [webhooks](https://docs.unione.io/en/web-api-ref#webhook) (event notification handlers) of a user or a project.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.WebhookApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        WebhookApi apiInstance = new WebhookApi(defaultClient);
        WebhookListRequest webhookListRequest = new WebhookListRequest();
        webhookListRequest.setLimit(null);
        webhookListRequest.setOffset(null);
        try {
            WebhookList200Response result = apiInstance.webhookList(webhookListRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhookApi#webhookList");
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
| **webhookListRequest** | [**WebhookListRequest**](WebhookListRequest.md)|  | |

### Return type

[**WebhookList200Response**](WebhookList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook list returned successfully. |  -  |
| **0** | Error occured. |  -  |


## webhookSet

> WebhookSet200Response webhookSet(webhookSetRequest)

Sets or edits a [webhook](https://docs.unione.io/en/web-api-ref#webhook), i.e. an event notification handler.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.WebhookApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        WebhookApi apiInstance = new WebhookApi(defaultClient);
        WebhookSetRequest webhookSetRequest = new WebhookSetRequest();
        webhookSetRequest.setUrl("https://yourhost.example.com/unione-webhook");
        webhookSetRequest.setStatus(null);
        webhookSetRequest.setEventFormat(null);
        webhookSetRequest.setDeliveryInfo(null);
        webhookSetRequest.setSingleEvent(null);
        webhookSetRequest.setMaxParallel(null);
        WebhookEventsObject mEvents = new WebhookEventsObject();
        webhookSetRequest.setEvents(mEvents);
        try {
            WebhookSet200Response result = apiInstance.webhookSet(webhookSetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhookApi#webhookSet");
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
| **webhookSetRequest** | [**WebhookSetRequest**](WebhookSetRequest.md)|  | |

### Return type

[**WebhookSet200Response**](WebhookSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webhook set successfully. |  -  |
| **0** | Error occured. |  -  |

