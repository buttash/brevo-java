# DomainsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authenticateDomain**](DomainsApi.md#authenticateDomain) | **PUT** /senders/domains/{domainName}/authenticate | Authenticate a domain
[**createDomain**](DomainsApi.md#createDomain) | **POST** /senders/domains | Create a new domain
[**deleteDomain**](DomainsApi.md#deleteDomain) | **DELETE** /senders/domains/{domainName} | Delete a domain
[**getDomainConfiguration**](DomainsApi.md#getDomainConfiguration) | **GET** /senders/domains/{domainName} | Validate domain configuration
[**getDomains**](DomainsApi.md#getDomains) | **GET** /senders/domains | Get the list of all your domains


<a name="authenticateDomain"></a>
# **authenticateDomain**
> AuthenticateDomainModel authenticateDomain(domainName)

Authenticate a domain

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DomainsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

DomainsApi apiInstance = new DomainsApi();
String domainName = "domainName_example"; // String | Domain name
try {
    AuthenticateDomainModel result = apiInstance.authenticateDomain(domainName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DomainsApi#authenticateDomain");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainName** | **String**| Domain name |

### Return type

[**AuthenticateDomainModel**](AuthenticateDomainModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createDomain"></a>
# **createDomain**
> CreateDomainModel createDomain(domainName)

Create a new domain

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DomainsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

DomainsApi apiInstance = new DomainsApi();
CreateDomain domainName = new CreateDomain(); // CreateDomain | domain's name
try {
    CreateDomainModel result = apiInstance.createDomain(domainName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DomainsApi#createDomain");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainName** | [**CreateDomain**](CreateDomain.md)| domain&#39;s name | [optional]

### Return type

[**CreateDomainModel**](CreateDomainModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteDomain"></a>
# **deleteDomain**
> deleteDomain(domainName)

Delete a domain

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DomainsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

DomainsApi apiInstance = new DomainsApi();
String domainName = "domainName_example"; // String | Domain name
try {
    apiInstance.deleteDomain(domainName);
} catch (ApiException e) {
    System.err.println("Exception when calling DomainsApi#deleteDomain");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainName** | **String**| Domain name |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getDomainConfiguration"></a>
# **getDomainConfiguration**
> GetDomainConfigurationModel getDomainConfiguration(domainName)

Validate domain configuration

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DomainsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

DomainsApi apiInstance = new DomainsApi();
String domainName = "domainName_example"; // String | Domain name
try {
    GetDomainConfigurationModel result = apiInstance.getDomainConfiguration(domainName);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DomainsApi#getDomainConfiguration");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainName** | **String**| Domain name |

### Return type

[**GetDomainConfigurationModel**](GetDomainConfigurationModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getDomains"></a>
# **getDomains**
> GetDomainsList getDomains()

Get the list of all your domains

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DomainsApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api-key
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("api-key");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

// Configure API key authorization: partner-key
ApiKeyAuth partnerKey = (ApiKeyAuth) defaultClient.getAuthentication("partner-key");
partnerKey.setApiKey("YOUR PARTNER KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//partnerKey.setApiKeyPrefix("Token");

DomainsApi apiInstance = new DomainsApi();
try {
    GetDomainsList result = apiInstance.getDomains();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DomainsApi#getDomains");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetDomainsList**](GetDomainsList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

