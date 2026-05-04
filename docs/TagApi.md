# TagApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**tagDelete**](TagApi.md#tagDelete) | **POST** /tag/delete.json | Removes tag. |
| [**tagList**](TagApi.md#tagList) | **POST** /tag/list.json | This method returns the full list of user-defined tags. Does not receive any parameters. |



## tagDelete

> SuccessResponse tagDelete(tagDeleteRequest)

Removes tag.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.TagApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        TagApi apiInstance = new TagApi(defaultClient);
        TagDeleteRequest tagDeleteRequest = new TagDeleteRequest();
        tagDeleteRequest.setTagId(54);
        try {
            SuccessResponse result = apiInstance.tagDelete(tagDeleteRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TagApi#tagDelete");
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
| **tagDeleteRequest** | [**TagDeleteRequest**](TagDeleteRequest.md)|  | |

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
| **200** | Tag deleted successfully. |  -  |
| **0** | Error occured. |  -  |


## tagList

> TagList200Response tagList()

This method returns the full list of user-defined tags. Does not receive any parameters.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.TagApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        TagApi apiInstance = new TagApi(defaultClient);
        try {
            TagList200Response result = apiInstance.tagList();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TagApi#tagList");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**TagList200Response**](TagList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List returned successfully. |  -  |
| **0** | Error occured. |  -  |

