# SuppressionApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**suppressionDelete**](SuppressionApi.md#suppressionDelete) | **POST** /suppression/delete.json | Deletes an email from suppression list (only records with is_deletable=true). If there are no entries of this email in the suppression list, API error 3003 is returned. If such entries exist but no one can be deleted, API error 3004 is returned. If daily limit of deletes exceeded, API error 906 is returned. |
| [**suppressionGet**](SuppressionApi.md#suppressionGet) | **POST** /suppression/get.json | Gets a reason and date of email suppression. |
| [**suppressionList**](SuppressionApi.md#suppressionList) | **POST** /suppression/list.json | Returns a suppression list since provided date. |
| [**suppressionSet**](SuppressionApi.md#suppressionSet) | **POST** /suppression/set.json | Adds an email address to the suppression list. You can always remove this address from the suppression list later using the [suppression/delete](https://docs.unione.io/en/web-api-ref#suppression-delete) method. |



## suppressionDelete

> SuccessResponse suppressionDelete(suppressionDeleteRequest)

Deletes an email from suppression list (only records with is_deletable=true). If there are no entries of this email in the suppression list, API error 3003 is returned. If such entries exist but no one can be deleted, API error 3004 is returned. If daily limit of deletes exceeded, API error 906 is returned.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.SuppressionApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        SuppressionApi apiInstance = new SuppressionApi(defaultClient);
        SuppressionDeleteRequest suppressionDeleteRequest = new SuppressionDeleteRequest();
        suppressionDeleteRequest.setEmail("email@example.com");
        try {
            SuccessResponse result = apiInstance.suppressionDelete(suppressionDeleteRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SuppressionApi#suppressionDelete");
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
| **suppressionDeleteRequest** | [**SuppressionDeleteRequest**](SuppressionDeleteRequest.md)|  | |

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
| **200** | Email has been deleted from the suppression list. |  -  |
| **0** | Error occured. |  -  |


## suppressionGet

> SuppressionGet200Response suppressionGet(suppressionGetRequest)

Gets a reason and date of email suppression.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.SuppressionApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        SuppressionApi apiInstance = new SuppressionApi(defaultClient);
        SuppressionGetRequest suppressionGetRequest = new SuppressionGetRequest();
        suppressionGetRequest.setEmail("email@example.com");
        suppressionGetRequest.setAllProjects(true);
        try {
            SuppressionGet200Response result = apiInstance.suppressionGet(suppressionGetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SuppressionApi#suppressionGet");
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
| **suppressionGetRequest** | [**SuppressionGetRequest**](SuppressionGetRequest.md)|  | |

### Return type

[**SuppressionGet200Response**](SuppressionGet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Method call has succeeded (but suppressions array can be empty if sending to email is not suppressed). |  -  |
| **0** | Error occured. |  -  |


## suppressionList

> SuppressionList200Response suppressionList(suppressionListRequest)

Returns a suppression list since provided date.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.SuppressionApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        SuppressionApi apiInstance = new SuppressionApi(defaultClient);
        SuppressionListRequest suppressionListRequest = new SuppressionListRequest();
        suppressionListRequest.setCause("unsubscribed");
        suppressionListRequest.setSource("user");
        suppressionListRequest.setStartTime("2020-10-14 17:00:00");
        suppressionListRequest.setCursor("Ajfb6Hvdkn3hdhhvG57xbdufhG5");
        suppressionListRequest.setLimit(50);
        try {
            SuppressionList200Response result = apiInstance.suppressionList(suppressionListRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SuppressionApi#suppressionList");
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
| **suppressionListRequest** | [**SuppressionListRequest**](SuppressionListRequest.md)|  | |

### Return type

[**SuppressionList200Response**](SuppressionList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Returns a suppression list since provided date. |  -  |
| **0** | Error occured. |  -  |


## suppressionSet

> SuccessResponse suppressionSet(suppressionSetRequest)

Adds an email address to the suppression list. You can always remove this address from the suppression list later using the [suppression/delete](https://docs.unione.io/en/web-api-ref#suppression-delete) method.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.SuppressionApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        SuppressionApi apiInstance = new SuppressionApi(defaultClient);
        SuppressionSetRequest suppressionSetRequest = new SuppressionSetRequest();
        suppressionSetRequest.setEmail("email@example.com");
        suppressionSetRequest.setCause("unsubscribed");
        suppressionSetRequest.setCreated("2021-12-19 10:15:49");
        try {
            SuccessResponse result = apiInstance.suppressionSet(suppressionSetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling SuppressionApi#suppressionSet");
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
| **suppressionSetRequest** | [**SuppressionSetRequest**](SuppressionSetRequest.md)|  | |

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
| **200** | Email has been added to the suppression list. |  -  |
| **0** | Error occured. |  -  |

