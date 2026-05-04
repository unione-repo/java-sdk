# TemplateApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**templateDelete**](TemplateApi.md#templateDelete) | **POST** /template/delete.json | Deletes a template by id. |
| [**templateGet**](TemplateApi.md#templateGet) | **POST** /template/get.json | Gets template properties by it's id. |
| [**templateList**](TemplateApi.md#templateList) | **POST** /template/list.json | Returns the list of all or some templates of the account. |
| [**templateSet**](TemplateApi.md#templateSet) | **POST** /template/set.json | Creates or updates an email template. |



## templateDelete

> SuccessResponse templateDelete(templateGetRequest)

Deletes a template by id.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.TemplateApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        TemplateApi apiInstance = new TemplateApi(defaultClient);
        TemplateGetRequest templateGetRequest = new TemplateGetRequest();
        templateGetRequest.setId("00000000-0000-0000-0000-000000000000");
        try {
            SuccessResponse result = apiInstance.templateDelete(templateGetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TemplateApi#templateDelete");
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
| **templateGetRequest** | [**TemplateGetRequest**](TemplateGetRequest.md)|  | |

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
| **200** | Template deleted successfully. |  -  |
| **0** | Error occured. |  -  |


## templateGet

> TemplateSet200Response templateGet(templateGetRequest)

Gets template properties by it's id.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.TemplateApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        TemplateApi apiInstance = new TemplateApi(defaultClient);
        TemplateGetRequest templateGetRequest = new TemplateGetRequest();
        templateGetRequest.setId("00000000-0000-0000-0000-000000000000");
        try {
            TemplateSet200Response result = apiInstance.templateGet(templateGetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TemplateApi#templateGet");
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
| **templateGetRequest** | [**TemplateGetRequest**](TemplateGetRequest.md)|  | |

### Return type

[**TemplateSet200Response**](TemplateSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template returned successfully. |  -  |
| **0** | Error occured. |  -  |


## templateList

> TemplateList200Response templateList(templateListRequest)

Returns the list of all or some templates of the account.

You can iterate thru large list using **offset** and **limit** parameters. When less than **limit** templates are returned then the end of list is reached.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.TemplateApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        TemplateApi apiInstance = new TemplateApi(defaultClient);
        TemplateListRequest templateListRequest = new TemplateListRequest();
        templateListRequest.setLimit(null);
        templateListRequest.setOffset(null);
        try {
            TemplateList200Response result = apiInstance.templateList(templateListRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TemplateApi#templateList");
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
| **templateListRequest** | [**TemplateListRequest**](TemplateListRequest.md)|  | |

### Return type

[**TemplateList200Response**](TemplateList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template list returned successfully. |  -  |
| **0** | Error occured. |  -  |


## templateSet

> TemplateSet200Response templateSet(templateSetRequest)

Creates or updates an email template.

Restrictions:<br>* The maximum request size is 10 MB.<br>* The number of templates is limited to 10000.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.TemplateApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        TemplateApi apiInstance = new TemplateApi(defaultClient);
        TemplateSetRequest templateSetRequest = new TemplateSetRequest();
        TemplateObject mTemplate = new TemplateObject();
        templateSetRequest.setTemplate(mTemplate);
        try {
            TemplateSet200Response result = apiInstance.templateSet(templateSetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TemplateApi#templateSet");
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
| **templateSetRequest** | [**TemplateSetRequest**](TemplateSetRequest.md)|  | |

### Return type

[**TemplateSet200Response**](TemplateSet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Template set successfully. |  -  |
| **0** | Error occured. |  -  |

