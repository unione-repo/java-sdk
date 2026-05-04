# ProjectApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**projectCreate**](ProjectApi.md#projectCreate) | **POST** /project/create.json | Creates a new project. |
| [**projectDelete**](ProjectApi.md#projectDelete) | **POST** /project/delete.json | Deletes a project. |
| [**projectList**](ProjectApi.md#projectList) | **POST** /project/list.json | Lists projects. |
| [**projectUpdate**](ProjectApi.md#projectUpdate) | **POST** /project/update.json | Updates a project. |



## projectCreate

> ProjectCreate200Response projectCreate(projectCreateRequest)

Creates a new project.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ProjectApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ProjectApi apiInstance = new ProjectApi(defaultClient);
        ProjectCreateRequest projectCreateRequest = new ProjectCreateRequest();
        ProjectObject mProject = new ProjectObject();
        projectCreateRequest.setProject(mProject);
        try {
            ProjectCreate200Response result = apiInstance.projectCreate(projectCreateRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ProjectApi#projectCreate");
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
| **projectCreateRequest** | [**ProjectCreateRequest**](ProjectCreateRequest.md)|  | |

### Return type

[**ProjectCreate200Response**](ProjectCreate200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Project created successfully. |  -  |
| **0** | Error occured. |  -  |


## projectDelete

> SuccessResponse projectDelete(projectDeleteRequest)

Deletes a project.

The project will be moved to the **trash bin** before being permanently deleted. You can restore the project by contacting support.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ProjectApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ProjectApi apiInstance = new ProjectApi(defaultClient);
        ProjectDeleteRequest projectDeleteRequest = new ProjectDeleteRequest();
        projectDeleteRequest.setProjectId("1234567890");
        projectDeleteRequest.setProjectApiKey("your api_key");
        try {
            SuccessResponse result = apiInstance.projectDelete(projectDeleteRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ProjectApi#projectDelete");
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
| **projectDeleteRequest** | [**ProjectDeleteRequest**](ProjectDeleteRequest.md)|  | |

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
| **200** | Project deleted successfully. |  -  |
| **0** | Error occured. |  -  |


## projectList

> ProjectList200Response projectList(projectListRequest)

Lists projects.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ProjectApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ProjectApi apiInstance = new ProjectApi(defaultClient);
        ProjectListRequest projectListRequest = new ProjectListRequest();
        projectListRequest.setProjectId("1234567890");
        projectListRequest.setProjectApiKey("your api_key");
        try {
            ProjectList200Response result = apiInstance.projectList(projectListRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ProjectApi#projectList");
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
| **projectListRequest** | [**ProjectListRequest**](ProjectListRequest.md)|  | |

### Return type

[**ProjectList200Response**](ProjectList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Projects returned successfully. |  -  |
| **0** | Error occured. |  -  |


## projectUpdate

> ProjectUpdate200Response projectUpdate(projectUpdateRequest)

Updates a project.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.ProjectApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        ProjectApi apiInstance = new ProjectApi(defaultClient);
        ProjectUpdateRequest projectUpdateRequest = new ProjectUpdateRequest();
        projectUpdateRequest.setProjectId("1234567890");
        projectUpdateRequest.setProjectApiKey("your api_key");
        ProjectUpdateObject mProject = new ProjectUpdateObject();
        projectUpdateRequest.setProject(mProject);
        try {
            ProjectUpdate200Response result = apiInstance.projectUpdate(projectUpdateRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ProjectApi#projectUpdate");
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
| **projectUpdateRequest** | [**ProjectUpdateRequest**](ProjectUpdateRequest.md)|  | |

### Return type

[**ProjectUpdate200Response**](ProjectUpdate200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Project updated successfully. |  -  |
| **0** | Error occured. |  -  |

