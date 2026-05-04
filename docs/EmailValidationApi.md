# EmailValidationApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**emailValidationSingle**](EmailValidationApi.md#emailValidationSingle) | **POST** /email-validation/single.json | A maximum of two concurrent requests are allowed; if you send more requests, an error will be returned. Since the verification process should be completed promptly, we've set a time limit on email check. If we encounter a slow email server that does not respond in 5 seconds, you may get an “unknown” status. |



## emailValidationSingle

> EmailValidationSingle200Response emailValidationSingle(emailValidationSingleRequest)

A maximum of two concurrent requests are allowed; if you send more requests, an error will be returned. Since the verification process should be completed promptly, we've set a time limit on email check. If we encounter a slow email server that does not respond in 5 seconds, you may get an “unknown” status.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.EmailValidationApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        EmailValidationApi apiInstance = new EmailValidationApi(defaultClient);
        EmailValidationSingleRequest emailValidationSingleRequest = new EmailValidationSingleRequest();
        emailValidationSingleRequest.setEmail("email@example.com");
        try {
            EmailValidationSingle200Response result = apiInstance.emailValidationSingle(emailValidationSingleRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling EmailValidationApi#emailValidationSingle");
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
| **emailValidationSingleRequest** | [**EmailValidationSingleRequest**](EmailValidationSingleRequest.md)|  | |

### Return type

[**EmailValidationSingle200Response**](EmailValidationSingle200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email check completed successfully. |  -  |
| **0** | Error occured. |  -  |

