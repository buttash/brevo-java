# CouponsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createCouponCollection**](CouponsApi.md#createCouponCollection) | **POST** /couponCollections | Create а coupon collection
[**createCoupons**](CouponsApi.md#createCoupons) | **POST** /coupons | Create coupons for a coupon collection
[**getCouponCollection**](CouponsApi.md#getCouponCollection) | **GET** /couponCollections/{id} | Get a coupon collection by id
[**getCouponCollections**](CouponsApi.md#getCouponCollections) | **GET** /couponCollections | Get all your coupon collections
[**updateCouponCollection**](CouponsApi.md#updateCouponCollection) | **PATCH** /couponCollections/{id} | Update a coupon collection by id


<a name="createCouponCollection"></a>
# **createCouponCollection**
> InlineResponse2013 createCouponCollection(createCouponCollection)

Create а coupon collection

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CouponsApi;

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

CouponsApi apiInstance = new CouponsApi();
CreateCouponCollection createCouponCollection = new CreateCouponCollection(); // CreateCouponCollection | Values to create a coupon collection
try {
    InlineResponse2013 result = apiInstance.createCouponCollection(createCouponCollection);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CouponsApi#createCouponCollection");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createCouponCollection** | [**CreateCouponCollection**](CreateCouponCollection.md)| Values to create a coupon collection |

### Return type

[**InlineResponse2013**](InlineResponse2013.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createCoupons"></a>
# **createCoupons**
> createCoupons(createCoupons)

Create coupons for a coupon collection

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CouponsApi;

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

CouponsApi apiInstance = new CouponsApi();
CreateCoupons createCoupons = new CreateCoupons(); // CreateCoupons | Values to create coupons
try {
    apiInstance.createCoupons(createCoupons);
} catch (ApiException e) {
    System.err.println("Exception when calling CouponsApi#createCoupons");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createCoupons** | [**CreateCoupons**](CreateCoupons.md)| Values to create coupons |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCouponCollection"></a>
# **getCouponCollection**
> GetCouponCollection getCouponCollection(id)

Get a coupon collection by id

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CouponsApi;

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

CouponsApi apiInstance = new CouponsApi();
String id = "id_example"; // String | Id of the collection to return
try {
    GetCouponCollection result = apiInstance.getCouponCollection(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CouponsApi#getCouponCollection");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Id of the collection to return |

### Return type

[**GetCouponCollection**](GetCouponCollection.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCouponCollections"></a>
# **getCouponCollections**
> GetCouponCollection getCouponCollections(limit, offset, sort, sortBy)

Get all your coupon collections

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CouponsApi;

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

CouponsApi apiInstance = new CouponsApi();
Long limit = 50L; // Long | Number of documents returned per page
Long offset = 0L; // Long | Index of the first document on the page
String sort = "desc"; // String | Sort the results by creation time in ascending/descending order
Object sortBy = null; // Object | The field used to sort coupon collections
try {
    GetCouponCollection result = apiInstance.getCouponCollections(limit, offset, sort, sortBy);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CouponsApi#getCouponCollections");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents returned per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document on the page | [optional] [default to 0]
 **sort** | **String**| Sort the results by creation time in ascending/descending order | [optional] [default to desc] [enum: asc, desc]
 **sortBy** | [**Object**](.md)| The field used to sort coupon collections | [optional]

### Return type

[**GetCouponCollection**](GetCouponCollection.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateCouponCollection"></a>
# **updateCouponCollection**
> InlineResponse2003 updateCouponCollection(id, updateCouponCollection)

Update a coupon collection by id

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.CouponsApi;

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

CouponsApi apiInstance = new CouponsApi();
String id = "id_example"; // String | Id of the collection to update
UpdateCouponCollection updateCouponCollection = new UpdateCouponCollection(); // UpdateCouponCollection | Values to update the coupon collection
try {
    InlineResponse2003 result = apiInstance.updateCouponCollection(id, updateCouponCollection);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling CouponsApi#updateCouponCollection");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Id of the collection to update |
 **updateCouponCollection** | [**UpdateCouponCollection**](UpdateCouponCollection.md)| Values to update the coupon collection | [optional]

### Return type

[**InlineResponse2003**](InlineResponse2003.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

