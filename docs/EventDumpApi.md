# EventDumpApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**eventDumpCreate**](EventDumpApi.md#eventDumpCreate) | **POST** /event-dump/create.json | This asynchronous method initiates the preparation of data dump in CSV format. The number of dump files created or stored is limited to 10; to order more files, you have to delete one of the previous ones or wait until they will be deleted automatically. A newly created dump file is kept for 8 hours. If the request period is more than a day or there are too many events then several files will be generated and each file will contain no more than 100,000 events. File contains columns with the following information - 'event_time', 'job_id', 'from_email', 'email', 'status', 'delivery_status', 'metadata', 'destination_response', 'user_agent', 'url', 'ip', 'tags' and 'project_id' (for accounts with projects enabled). You can change the fields and include 'subject' field using 'dump_fileds' parameter. |
| [**eventDumpDelete**](EventDumpApi.md#eventDumpDelete) | **POST** /event-dump/delete.json | Removes dump from queue or storage. |
| [**eventDumpGet**](EventDumpApi.md#eventDumpGet) | **POST** /event-dump/get.json | Returns dump properties for a given identifier |
| [**eventDumpList**](EventDumpApi.md#eventDumpList) | **POST** /event-dump/list.json | This method does not require any parameters; returns the full list of existing dumps. |



## eventDumpCreate

> EventDumpCreate200Response eventDumpCreate(eventDumpCreateRequest)

This asynchronous method initiates the preparation of data dump in CSV format. The number of dump files created or stored is limited to 10; to order more files, you have to delete one of the previous ones or wait until they will be deleted automatically. A newly created dump file is kept for 8 hours. If the request period is more than a day or there are too many events then several files will be generated and each file will contain no more than 100,000 events. File contains columns with the following information - 'event_time', 'job_id', 'from_email', 'email', 'status', 'delivery_status', 'metadata', 'destination_response', 'user_agent', 'url', 'ip', 'tags' and 'project_id' (for accounts with projects enabled). You can change the fields and include 'subject' field using 'dump_fileds' parameter.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EventDumpApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EventDumpApi apiInstance = new EventDumpApi(defaultClient);
        EventDumpCreateRequest eventDumpCreateRequest = new EventDumpCreateRequest();
        eventDumpCreateRequest.setStartTime("2022-07-20 00:00:00");
        eventDumpCreateRequest.setEndTime("2022-07-21 00:00:00");
        eventDumpCreateRequest.setLimit(50);
        eventDumpCreateRequest.setAllProjects(true);
        FilterObject mFilter = new FilterObject();
        eventDumpCreateRequest.setFilter(mFilter);
        eventDumpCreateRequest.setDumpFields(new java.util.ArrayList<>());
        eventDumpCreateRequest.setAggregate("day_status");
        eventDumpCreateRequest.setDelimiter(";");
        eventDumpCreateRequest.setFormat("csv");
        try {
            EventDumpCreate200Response result = apiInstance.eventDumpCreate(eventDumpCreateRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EventDumpApi#eventDumpCreate");
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
| **eventDumpCreateRequest** | [**EventDumpCreateRequest**](EventDumpCreateRequest.md)|  | |

### Return type

[**EventDumpCreate200Response**](EventDumpCreate200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Method call has succeeded. |  -  |
| **0** | Error occured. |  -  |


## eventDumpDelete

> SuccessResponse eventDumpDelete(eventDumpDeleteRequest)

Removes dump from queue or storage.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EventDumpApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EventDumpApi apiInstance = new EventDumpApi(defaultClient);
        EventDumpDeleteRequest eventDumpDeleteRequest = new EventDumpDeleteRequest();
        eventDumpDeleteRequest.setDumpId("Gqfasjh34tlasd");
        try {
            SuccessResponse result = apiInstance.eventDumpDelete(eventDumpDeleteRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EventDumpApi#eventDumpDelete");
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
| **eventDumpDeleteRequest** | [**EventDumpDeleteRequest**](EventDumpDeleteRequest.md)|  | |

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
| **200** | Dump deleted successfully. |  -  |
| **0** | Error occured. |  -  |


## eventDumpGet

> EventDumpGet200Response eventDumpGet(eventDumpGetRequest)

Returns dump properties for a given identifier

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EventDumpApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EventDumpApi apiInstance = new EventDumpApi(defaultClient);
        EventDumpGetRequest eventDumpGetRequest = new EventDumpGetRequest();
        eventDumpGetRequest.setDumpId("Gqfasjh34tlasd");
        try {
            EventDumpGet200Response result = apiInstance.eventDumpGet(eventDumpGetRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EventDumpApi#eventDumpGet");
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
| **eventDumpGetRequest** | [**EventDumpGetRequest**](EventDumpGetRequest.md)|  | |

### Return type

[**EventDumpGet200Response**](EventDumpGet200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Dump information returned successfully. |  -  |
| **0** | Error occured. |  -  |


## eventDumpList

> EventDumpList200Response eventDumpList()

This method does not require any parameters; returns the full list of existing dumps.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EventDumpApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EventDumpApi apiInstance = new EventDumpApi(defaultClient);
        try {
            EventDumpList200Response result = apiInstance.eventDumpList();
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EventDumpApi#eventDumpList");
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

[**EventDumpList200Response**](EventDumpList200Response.md)

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

