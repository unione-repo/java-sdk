# DomainApi

All URIs are relative to *https://api.unione.io/en/transactional/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**domainDelete**](DomainApi.md#domainDelete) | **POST** /domain/delete.json | Deletes a domain. Attention: you should use project's API key to delete a project's domain. |
| [**domainGetDnsRecords**](DomainApi.md#domainGetDnsRecords) | **POST** /domain/get-dns-records.json | Returns info on domain DNS setup for using with UniOne. |
| [**domainList**](DomainApi.md#domainList) | **POST** /domain/list.json | Returns a list of all registered domains for user or project, together with statuses of last validations. |
| [**domainValidateDkim**](DomainApi.md#domainValidateDkim) | **POST** /domain/validate-dkim.json | Validates DKIM record for domain. |
| [**domainValidateVerificationRecord**](DomainApi.md#domainValidateVerificationRecord) | **POST** /domain/validate-verification-record.json | Triggers verification record validation for domain. |



## domainDelete

> DomainDelete200Response domainDelete(domainDeleteRequest)

Deletes a domain. Attention: you should use project's API key to delete a project's domain.

Deletes a domain.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.DomainApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        DomainApi apiInstance = new DomainApi(defaultClient);
        DomainDeleteRequest domainDeleteRequest = new DomainDeleteRequest();
        domainDeleteRequest.setDomain("example.com");
        try {
            DomainDelete200Response result = apiInstance.domainDelete(domainDeleteRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DomainApi#domainDelete");
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
| **domainDeleteRequest** | [**DomainDeleteRequest**](DomainDeleteRequest.md)|  | |

### Return type

[**DomainDelete200Response**](DomainDelete200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Domain has been successfully deleted. |  -  |
| **0** | Error occured. |  -  |


## domainGetDnsRecords

> DomainGetDnsRecords200Response domainGetDnsRecords(domainGetDnsRecordsRequest)

Returns info on domain DNS setup for using with UniOne.

In order to send emails you have to confirm that you own the domain that you are going to send emails from and setup DKIM signature for the domain. This method allows you to register your domain in UniOne and generate verification record and DKIM key, or return previously generated ones if domain is already registered.<br>You should add then DNS records like this to all of the domains you want to confirm:<br>`@ IN TXT **unione-validate-hash=483bb362ebdbeedd755cfb1d4d661**`<br>`us._domainkey IN TXT **k=rsa; p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDo7**`<br>`@ IN TXT **v=spf1 include:spf.unione.io ~all**`<br>- First record value should contain **verification-record** field returned by get-dns-records method **as is**.<br>- Second record value should contain **dkim** field value after **p=**. Mind the name of this record! **us._domainkey.** prefix is important for DKIM selector of UniOne to work properly.<br>- Third record contains optional, but very recommended SPF entry. Probably you already have one, then just add append include:spf.unione.io right after v=spf1.<br>Syntax requirements of different DNS providers may differ:<br>- sometimes it's necesarry to put full domain name instead of @ sign.<br>- some providers require add TTL value (like 3600)<br>- some providers don't require quotes for enclosing values<br>Please check requirements of your provider and advice your users to do it.

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.DomainApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        DomainApi apiInstance = new DomainApi(defaultClient);
        DomainGetDnsRecordsRequest domainGetDnsRecordsRequest = new DomainGetDnsRecordsRequest();
        domainGetDnsRecordsRequest.setDomain("example.com");
        try {
            DomainGetDnsRecords200Response result = apiInstance.domainGetDnsRecords(domainGetDnsRecordsRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DomainApi#domainGetDnsRecords");
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
| **domainGetDnsRecordsRequest** | [**DomainGetDnsRecordsRequest**](DomainGetDnsRecordsRequest.md)|  | |

### Return type

[**DomainGetDnsRecords200Response**](DomainGetDnsRecords200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Domain DNS info returned successfully. |  -  |
| **0** | Error occured. |  -  |


## domainList

> DomainList200Response domainList(domainListRequest)

Returns a list of all registered domains for user or project, together with statuses of last validations.

Returns last status of ownership validation and DKIM validation for each domain. Read more [here](https://docs.unione.io/en/web-api-ref#domain).

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.DomainApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        DomainApi apiInstance = new DomainApi(defaultClient);
        DomainListRequest domainListRequest = new DomainListRequest();
        domainListRequest.setDomain("example.com");
        domainListRequest.setLimit(null);
        domainListRequest.setOffset(null);
        try {
            DomainList200Response result = apiInstance.domainList(domainListRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DomainApi#domainList");
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
| **domainListRequest** | [**DomainListRequest**](DomainListRequest.md)|  | |

### Return type

[**DomainList200Response**](DomainList200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of the registered domains returned successfully. |  -  |
| **0** | Error occured. |  -  |


## domainValidateDkim

> DomainValidateVerificationRecord200Response domainValidateDkim(domainValidateDkimRequest)

Validates DKIM record for domain.

If you get 200 OK then it means the validation process started succesfully, but it doesn't mean the DKIM record is valid. You should check later dkim.status field returned by [domain/list](https://docs.unione.io/en/web-api-ref#domain-list) method to get the result. Please read more [here](https://docs.unione.io/en/web-api-ref#domain).

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.DomainApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        DomainApi apiInstance = new DomainApi(defaultClient);
        DomainValidateDkimRequest domainValidateDkimRequest = new DomainValidateDkimRequest();
        domainValidateDkimRequest.setDomain("example.com");
        try {
            DomainValidateVerificationRecord200Response result = apiInstance.domainValidateDkim(domainValidateDkimRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DomainApi#domainValidateDkim");
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
| **domainValidateDkimRequest** | [**DomainValidateDkimRequest**](DomainValidateDkimRequest.md)|  | |

### Return type

[**DomainValidateVerificationRecord200Response**](DomainValidateVerificationRecord200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | DKIM record validation has started successfully. |  -  |
| **0** | Error occured or record is invalid. |  -  |


## domainValidateVerificationRecord

> DomainValidateVerificationRecord200Response domainValidateVerificationRecord(domainValidateVerificationRecordRequest)

Triggers verification record validation for domain.

If you get 200 OK then it means the validation process started succesfully, but it doesn't mean the verification record is valid. You should check later verification-record.status field returned by [domain/list](https://docs.unione.io/en/web-api-ref#domain-list) method to get the result. Please read more [here](https://docs.unione.io/en/web-api-ref#domain).

### Example

```java
// Import classes:
import com.unione.api.invoker.ApiClient;
import com.unione.api.invoker.ApiException;
import com.unione.api.invoker.Configuration;
import com.unione.api.invoker.auth.*;
import com.unione.api.invoker.models.*;
import com.unione.api.DomainApi;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.unione.io/en/transactional/api/v1");
        
        // Configure API key authorization: apiKeyAuth
        ApiKeyAuth apiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("apiKeyAuth");
        apiKeyAuth.setApiKey("YOUR API KEY");


        DomainApi apiInstance = new DomainApi(defaultClient);
        DomainValidateVerificationRecordRequest domainValidateVerificationRecordRequest = new DomainValidateVerificationRecordRequest();
        domainValidateVerificationRecordRequest.setDomain("example.com");
        try {
            DomainValidateVerificationRecord200Response result = apiInstance.domainValidateVerificationRecord(domainValidateVerificationRecordRequest);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DomainApi#domainValidateVerificationRecord");
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
| **domainValidateVerificationRecordRequest** | [**DomainValidateVerificationRecordRequest**](DomainValidateVerificationRecordRequest.md)|  | |

### Return type

[**DomainValidateVerificationRecord200Response**](DomainValidateVerificationRecord200Response.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification record is valid. |  -  |
| **0** | Error occured or record is invalid. |  -  |

