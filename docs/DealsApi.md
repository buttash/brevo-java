# DealsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**crmAttributesDealsGet**](DealsApi.md#crmAttributesDealsGet) | **GET** /crm/attributes/deals | Get deal attributes
[**crmDealsGet**](DealsApi.md#crmDealsGet) | **GET** /crm/deals | Get all deals
[**crmDealsIdDelete**](DealsApi.md#crmDealsIdDelete) | **DELETE** /crm/deals/{id} | Delete a deal
[**crmDealsIdGet**](DealsApi.md#crmDealsIdGet) | **GET** /crm/deals/{id} | Get a deal
[**crmDealsIdPatch**](DealsApi.md#crmDealsIdPatch) | **PATCH** /crm/deals/{id} | Update a deal
[**crmDealsLinkUnlinkIdPatch**](DealsApi.md#crmDealsLinkUnlinkIdPatch) | **PATCH** /crm/deals/link-unlink/{id} | Link and Unlink a deal with contacts and companies
[**crmDealsPost**](DealsApi.md#crmDealsPost) | **POST** /crm/deals | Create a deal
[**crmPipelineDetailsAllGet**](DealsApi.md#crmPipelineDetailsAllGet) | **GET** /crm/pipeline/details/all | Get all pipelines
[**crmPipelineDetailsGet**](DealsApi.md#crmPipelineDetailsGet) | **GET** /crm/pipeline/details | Get pipeline stages
[**crmPipelineDetailsPipelineIDGet**](DealsApi.md#crmPipelineDetailsPipelineIDGet) | **GET** /crm/pipeline/details/{pipelineID} | Get a pipeline


<a name="crmAttributesDealsGet"></a>
# **crmAttributesDealsGet**
> DealAttributes crmAttributesDealsGet()

Get deal attributes

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
try {
    DealAttributes result = apiInstance.crmAttributesDealsGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmAttributesDealsGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DealAttributes**](DealAttributes.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsGet"></a>
# **crmDealsGet**
> DealsList crmDealsGet(filtersAttributesDealName, filtersLinkedCompaniesIds, filtersLinkedContactsIds, offset, limit, sort, sortBy)

Get all deals

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String filtersAttributesDealName = "filtersAttributesDealName_example"; // String | Filter by attributes. If you have a filter for the owner on your end, please send it as filters[attributes.deal_owner] and utilize the account email for the filtering.
String filtersLinkedCompaniesIds = "filtersLinkedCompaniesIds_example"; // String | Filter by linked companies ids
String filtersLinkedContactsIds = "filtersLinkedContactsIds_example"; // String | Filter by linked companies ids
Long offset = 789L; // Long | Index of the first document of the page
Long limit = 50L; // Long | Number of documents per page
String sort = "sort_example"; // String | Sort the results in the ascending/descending order. Default order is **descending** by creation if `sort` is not passed
String sortBy = "sortBy_example"; // String | The field used to sort field names.
try {
    DealsList result = apiInstance.crmDealsGet(filtersAttributesDealName, filtersLinkedCompaniesIds, filtersLinkedContactsIds, offset, limit, sort, sortBy);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filtersAttributesDealName** | **String**| Filter by attributes. If you have a filter for the owner on your end, please send it as filters[attributes.deal_owner] and utilize the account email for the filtering. | [optional]
 **filtersLinkedCompaniesIds** | **String**| Filter by linked companies ids | [optional]
 **filtersLinkedContactsIds** | **String**| Filter by linked companies ids | [optional]
 **offset** | **Long**| Index of the first document of the page | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **sort** | **String**| Sort the results in the ascending/descending order. Default order is **descending** by creation if &#x60;sort&#x60; is not passed | [optional] [enum: asc, desc]
 **sortBy** | **String**| The field used to sort field names. | [optional]

### Return type

[**DealsList**](DealsList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsIdDelete"></a>
# **crmDealsIdDelete**
> crmDealsIdDelete(id)

Delete a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
try {
    apiInstance.crmDealsIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsIdGet"></a>
# **crmDealsIdGet**
> Deal crmDealsIdGet(id)

Get a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
try {
    Deal result = apiInstance.crmDealsIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |

### Return type

[**Deal**](Deal.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsIdPatch"></a>
# **crmDealsIdPatch**
> crmDealsIdPatch(id, body)

Update a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
Body7 body = new Body7(); // Body7 | Updated deal details.
try {
    apiInstance.crmDealsIdPatch(id, body);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsIdPatch");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **body** | [**Body7**](Body7.md)| Updated deal details. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsLinkUnlinkIdPatch"></a>
# **crmDealsLinkUnlinkIdPatch**
> crmDealsLinkUnlinkIdPatch(id, body)

Link and Unlink a deal with contacts and companies

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String id = "id_example"; // String | 
Body8 body = new Body8(); // Body8 | Linked / Unlinked contacts and companies ids.
try {
    apiInstance.crmDealsLinkUnlinkIdPatch(id, body);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsLinkUnlinkIdPatch");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**|  |
 **body** | [**Body8**](Body8.md)| Linked / Unlinked contacts and companies ids. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmDealsPost"></a>
# **crmDealsPost**
> InlineResponse2011 crmDealsPost(body)

Create a deal

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
Body6 body = new Body6(); // Body6 | Deal create data.
try {
    InlineResponse2011 result = apiInstance.crmDealsPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmDealsPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body6**](Body6.md)| Deal create data. |

### Return type

[**InlineResponse2011**](InlineResponse2011.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmPipelineDetailsAllGet"></a>
# **crmPipelineDetailsAllGet**
> Pipelines crmPipelineDetailsAllGet()

Get all pipelines

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
try {
    Pipelines result = apiInstance.crmPipelineDetailsAllGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmPipelineDetailsAllGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Pipelines**](Pipelines.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmPipelineDetailsGet"></a>
# **crmPipelineDetailsGet**
> Pipeline crmPipelineDetailsGet()

Get pipeline stages

This endpoint is deprecated. Prefer /crm/pipeline/details/{pipelineID} instead.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
try {
    Pipeline result = apiInstance.crmPipelineDetailsGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmPipelineDetailsGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Pipeline**](Pipeline.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="crmPipelineDetailsPipelineIDGet"></a>
# **crmPipelineDetailsPipelineIDGet**
> Pipelines crmPipelineDetailsPipelineIDGet(pipelineID)

Get a pipeline

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.DealsApi;

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

DealsApi apiInstance = new DealsApi();
String pipelineID = "pipelineID_example"; // String | 
try {
    Pipelines result = apiInstance.crmPipelineDetailsPipelineIDGet(pipelineID);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling DealsApi#crmPipelineDetailsPipelineIDGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pipelineID** | **String**|  |

### Return type

[**Pipelines**](Pipelines.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

