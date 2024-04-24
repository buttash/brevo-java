# ExternalFeedsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createExternalFeed**](ExternalFeedsApi.md#createExternalFeed) | **POST** /feeds | Create an external feed
[**deleteExternalFeed**](ExternalFeedsApi.md#deleteExternalFeed) | **DELETE** /feeds/{uuid} | Delete an external feed
[**getAllExternalFeeds**](ExternalFeedsApi.md#getAllExternalFeeds) | **GET** /feeds | Fetch all external feeds
[**getExternalFeedByUUID**](ExternalFeedsApi.md#getExternalFeedByUUID) | **GET** /feeds/{uuid} | Get an external feed by UUID
[**updateExternalFeed**](ExternalFeedsApi.md#updateExternalFeed) | **PUT** /feeds/{uuid} | Update an external feed


<a name="createExternalFeed"></a>
# **createExternalFeed**
> InlineResponse2015 createExternalFeed(createExternalFeed)

Create an external feed

This endpoint will create an external feed.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ExternalFeedsApi;

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

ExternalFeedsApi apiInstance = new ExternalFeedsApi();
CreateExternalFeed createExternalFeed = new CreateExternalFeed(); // CreateExternalFeed | Values to create a feed
try {
    InlineResponse2015 result = apiInstance.createExternalFeed(createExternalFeed);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ExternalFeedsApi#createExternalFeed");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createExternalFeed** | [**CreateExternalFeed**](CreateExternalFeed.md)| Values to create a feed |

### Return type

[**InlineResponse2015**](InlineResponse2015.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteExternalFeed"></a>
# **deleteExternalFeed**
> deleteExternalFeed(uuid)

Delete an external feed

This endpoint will delete an external feed.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ExternalFeedsApi;

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

ExternalFeedsApi apiInstance = new ExternalFeedsApi();
String uuid = "uuid_example"; // String | UUID of the feed to delete
try {
    apiInstance.deleteExternalFeed(uuid);
} catch (ApiException e) {
    System.err.println("Exception when calling ExternalFeedsApi#deleteExternalFeed");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **String**| UUID of the feed to delete |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getAllExternalFeeds"></a>
# **getAllExternalFeeds**
> GetAllExternalFeeds getAllExternalFeeds(search, startDate, endDate, sort, authType, limit, offset)

Fetch all external feeds

This endpoint can fetch all created external feeds.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ExternalFeedsApi;

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

ExternalFeedsApi apiInstance = new ExternalFeedsApi();
String search = "search_example"; // String | Can be used to filter records by search keyword on feed name
LocalDate startDate = LocalDate.now(); // LocalDate | Mandatory if `endDate` is used. Starting date (YYYY-MM-DD) from which you want to fetch the list. Can be maximum 30 days older than current date.
LocalDate endDate = LocalDate.now(); // LocalDate | Mandatory if `startDate` is used. Ending date (YYYY-MM-DD) till which you want to fetch the list. Maximum time period that can be selected is one month.
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed.
String authType = "authType_example"; // String | Filter the records by `authType` of the feed.
Long limit = 50L; // Long | Number of documents returned per page.
Long offset = 0L; // Long | Index of the first document on the page.
try {
    GetAllExternalFeeds result = apiInstance.getAllExternalFeeds(search, startDate, endDate, sort, authType, limit, offset);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ExternalFeedsApi#getAllExternalFeeds");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **search** | **String**| Can be used to filter records by search keyword on feed name | [optional]
 **startDate** | **LocalDate**| Mandatory if &#x60;endDate&#x60; is used. Starting date (YYYY-MM-DD) from which you want to fetch the list. Can be maximum 30 days older than current date. | [optional]
 **endDate** | **LocalDate**| Mandatory if &#x60;startDate&#x60; is used. Ending date (YYYY-MM-DD) till which you want to fetch the list. Maximum time period that can be selected is one month. | [optional]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed. | [optional] [default to desc] [enum: asc, desc]
 **authType** | **String**| Filter the records by &#x60;authType&#x60; of the feed. | [optional] [enum: basic, token, noAuth]
 **limit** | **Long**| Number of documents returned per page. | [optional] [default to 50]
 **offset** | **Long**| Index of the first document on the page. | [optional] [default to 0]

### Return type

[**GetAllExternalFeeds**](GetAllExternalFeeds.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getExternalFeedByUUID"></a>
# **getExternalFeedByUUID**
> GetExternalFeedByUUID getExternalFeedByUUID(uuid)

Get an external feed by UUID

This endpoint will update an external feed.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ExternalFeedsApi;

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

ExternalFeedsApi apiInstance = new ExternalFeedsApi();
String uuid = "uuid_example"; // String | UUID of the feed to fetch
try {
    GetExternalFeedByUUID result = apiInstance.getExternalFeedByUUID(uuid);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ExternalFeedsApi#getExternalFeedByUUID");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **String**| UUID of the feed to fetch |

### Return type

[**GetExternalFeedByUUID**](GetExternalFeedByUUID.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateExternalFeed"></a>
# **updateExternalFeed**
> updateExternalFeed(uuid, updateExternalFeed)

Update an external feed

This endpoint will update an external feed.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ExternalFeedsApi;

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

ExternalFeedsApi apiInstance = new ExternalFeedsApi();
String uuid = "uuid_example"; // String | UUID of the feed to update
UpdateExternalFeed updateExternalFeed = new UpdateExternalFeed(); // UpdateExternalFeed | Values to update a feed
try {
    apiInstance.updateExternalFeed(uuid, updateExternalFeed);
} catch (ApiException e) {
    System.err.println("Exception when calling ExternalFeedsApi#updateExternalFeed");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **String**| UUID of the feed to update |
 **updateExternalFeed** | [**UpdateExternalFeed**](UpdateExternalFeed.md)| Values to update a feed |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

