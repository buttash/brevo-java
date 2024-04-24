# EcommerceApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBatchOrder**](EcommerceApi.md#createBatchOrder) | **POST** /orders/status/batch | Create orders in batch
[**createOrder**](EcommerceApi.md#createOrder) | **POST** /orders/status | Managing the status of the order
[**createUpdateBatchCategory**](EcommerceApi.md#createUpdateBatchCategory) | **POST** /categories/batch | Create categories in batch
[**createUpdateBatchProducts**](EcommerceApi.md#createUpdateBatchProducts) | **POST** /products/batch | Create products in batch
[**createUpdateCategory**](EcommerceApi.md#createUpdateCategory) | **POST** /categories | Create/Update a category
[**createUpdateProduct**](EcommerceApi.md#createUpdateProduct) | **POST** /products | Create/Update a product
[**ecommerceActivatePost**](EcommerceApi.md#ecommerceActivatePost) | **POST** /ecommerce/activate | Activate the eCommerce app
[**ecommerceAttributionMetricsConversionSourceConversionSourceIdGet**](EcommerceApi.md#ecommerceAttributionMetricsConversionSourceConversionSourceIdGet) | **GET** /ecommerce/attribution/metrics/{conversionSource}/{conversionSourceId} | Get detailed attribution metrics for a single Brevo campaign
[**ecommerceAttributionMetricsGet**](EcommerceApi.md#ecommerceAttributionMetricsGet) | **GET** /ecommerce/attribution/metrics | Get attribution metrics for one or more Brevo campaigns
[**ecommerceAttributionProductsConversionSourceConversionSourceIdGet**](EcommerceApi.md#ecommerceAttributionProductsConversionSourceConversionSourceIdGet) | **GET** /ecommerce/attribution/products/{conversionSource}/{conversionSourceId} | Get attributed product sales for a single Brevo campaign
[**getCategories**](EcommerceApi.md#getCategories) | **GET** /categories | Return all your categories
[**getCategoryInfo**](EcommerceApi.md#getCategoryInfo) | **GET** /categories/{id} | Get a category details
[**getOrders**](EcommerceApi.md#getOrders) | **GET** /orders | Get order details
[**getProductInfo**](EcommerceApi.md#getProductInfo) | **GET** /products/{id} | Get a product&#39;s details
[**getProducts**](EcommerceApi.md#getProducts) | **GET** /products | Return all your products


<a name="createBatchOrder"></a>
# **createBatchOrder**
> createBatchOrder(orderBatch)

Create orders in batch

Create multiple orders at one time instead of one order at a time

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
OrderBatch orderBatch = new OrderBatch(); // OrderBatch | 
try {
    apiInstance.createBatchOrder(orderBatch);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#createBatchOrder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderBatch** | [**OrderBatch**](OrderBatch.md)|  |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createOrder"></a>
# **createOrder**
> createOrder(order)

Managing the status of the order

Manages the transactional status of the order

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Order order = new Order(); // Order | 
try {
    apiInstance.createOrder(order);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#createOrder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order** | [**Order**](Order.md)|  |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createUpdateBatchCategory"></a>
# **createUpdateBatchCategory**
> CreateUpdateBatchCategoryModel createUpdateBatchCategory(createUpdateBatchCategory)

Create categories in batch

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
CreateUpdateBatchCategory createUpdateBatchCategory = new CreateUpdateBatchCategory(); // CreateUpdateBatchCategory | Values to create a batch of categories
try {
    CreateUpdateBatchCategoryModel result = apiInstance.createUpdateBatchCategory(createUpdateBatchCategory);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#createUpdateBatchCategory");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUpdateBatchCategory** | [**CreateUpdateBatchCategory**](CreateUpdateBatchCategory.md)| Values to create a batch of categories |

### Return type

[**CreateUpdateBatchCategoryModel**](CreateUpdateBatchCategoryModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createUpdateBatchProducts"></a>
# **createUpdateBatchProducts**
> CreateUpdateBatchProductsModel createUpdateBatchProducts(createUpdateBatchProducts)

Create products in batch

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
CreateUpdateBatchProducts createUpdateBatchProducts = new CreateUpdateBatchProducts(); // CreateUpdateBatchProducts | Values to create a batch of products
try {
    CreateUpdateBatchProductsModel result = apiInstance.createUpdateBatchProducts(createUpdateBatchProducts);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#createUpdateBatchProducts");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUpdateBatchProducts** | [**CreateUpdateBatchProducts**](CreateUpdateBatchProducts.md)| Values to create a batch of products |

### Return type

[**CreateUpdateBatchProductsModel**](CreateUpdateBatchProductsModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createUpdateCategory"></a>
# **createUpdateCategory**
> CreateCategoryModel createUpdateCategory(createUpdateCategory)

Create/Update a category

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
CreateUpdateCategory createUpdateCategory = new CreateUpdateCategory(); // CreateUpdateCategory | Values to create/update a category
try {
    CreateCategoryModel result = apiInstance.createUpdateCategory(createUpdateCategory);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#createUpdateCategory");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUpdateCategory** | [**CreateUpdateCategory**](CreateUpdateCategory.md)| Values to create/update a category |

### Return type

[**CreateCategoryModel**](CreateCategoryModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createUpdateProduct"></a>
# **createUpdateProduct**
> CreateProductModel createUpdateProduct(createUpdateProduct)

Create/Update a product

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
CreateUpdateProduct createUpdateProduct = new CreateUpdateProduct(); // CreateUpdateProduct | Values to create/update a product
try {
    CreateProductModel result = apiInstance.createUpdateProduct(createUpdateProduct);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#createUpdateProduct");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createUpdateProduct** | [**CreateUpdateProduct**](CreateUpdateProduct.md)| Values to create/update a product |

### Return type

[**CreateProductModel**](CreateProductModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="ecommerceActivatePost"></a>
# **ecommerceActivatePost**
> ecommerceActivatePost()

Activate the eCommerce app

Getting access to Brevo eCommerce.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
try {
    apiInstance.ecommerceActivatePost();
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#ecommerceActivatePost");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="ecommerceAttributionMetricsConversionSourceConversionSourceIdGet"></a>
# **ecommerceAttributionMetricsConversionSourceConversionSourceIdGet**
> ecommerceAttributionMetricsConversionSourceConversionSourceIdGet(conversionSource, conversionSourceId)

Get detailed attribution metrics for a single Brevo campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Object conversionSource = null; // Object | The Brevo campaign type for which data will be retrieved
Object conversionSourceId = null; // Object | The Brevo campaign id for which data will be retrieved
try {
    apiInstance.ecommerceAttributionMetricsConversionSourceConversionSourceIdGet(conversionSource, conversionSourceId);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#ecommerceAttributionMetricsConversionSourceConversionSourceIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversionSource** | [**Object**](.md)| The Brevo campaign type for which data will be retrieved |
 **conversionSourceId** | [**Object**](.md)| The Brevo campaign id for which data will be retrieved |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="ecommerceAttributionMetricsGet"></a>
# **ecommerceAttributionMetricsGet**
> ecommerceAttributionMetricsGet(periodFrom, periodTo, emailCampaignId)

Get attribution metrics for one or more Brevo campaigns

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Object periodFrom = null; // Object | When getting metrics for a specific period, define the starting datetime in RFC3339 format
Object periodTo = null; // Object | When getting metrics for a specific period, define the end datetime in RFC3339 format
Object emailCampaignId = null; // Object | The email campaign id(s) to get metrics for
try {
    apiInstance.ecommerceAttributionMetricsGet(periodFrom, periodTo, emailCampaignId);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#ecommerceAttributionMetricsGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **periodFrom** | [**Object**](.md)| When getting metrics for a specific period, define the starting datetime in RFC3339 format | [optional]
 **periodTo** | [**Object**](.md)| When getting metrics for a specific period, define the end datetime in RFC3339 format | [optional]
 **emailCampaignId** | [**Object**](.md)| The email campaign id(s) to get metrics for | [optional]

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="ecommerceAttributionProductsConversionSourceConversionSourceIdGet"></a>
# **ecommerceAttributionProductsConversionSourceConversionSourceIdGet**
> ecommerceAttributionProductsConversionSourceConversionSourceIdGet(conversionSource, conversionSourceId)

Get attributed product sales for a single Brevo campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Object conversionSource = null; // Object | The Brevo campaign type for which data will be retrieved
Object conversionSourceId = null; // Object | The Brevo campaign id for which data will be retrieved
try {
    apiInstance.ecommerceAttributionProductsConversionSourceConversionSourceIdGet(conversionSource, conversionSourceId);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#ecommerceAttributionProductsConversionSourceConversionSourceIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **conversionSource** | [**Object**](.md)| The Brevo campaign type for which data will be retrieved |
 **conversionSourceId** | [**Object**](.md)| The Brevo campaign id for which data will be retrieved |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCategories"></a>
# **getCategories**
> GetCategories getCategories(limit, offset, sort, ids, name, modifiedSince, createdSince)

Return all your categories

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
List<String> ids = Arrays.asList("ids_example"); // List<String> | Filter by category ids
String name = "name_example"; // String | Filter by category name
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the categories modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**         
String createdSince = "createdSince_example"; // String | Filter (urlencoded) the categories created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**         
try {
    GetCategories result = apiInstance.getCategories(limit, offset, sort, ids, name, modifiedSince, createdSince);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#getCategories");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]
 **ids** | [**List&lt;String&gt;**](String.md)| Filter by category ids | [optional]
 **name** | **String**| Filter by category name | [optional]
 **modifiedSince** | **String**| Filter (urlencoded) the categories modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**          | [optional]
 **createdSince** | **String**| Filter (urlencoded) the categories created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**          | [optional]

### Return type

[**GetCategories**](GetCategories.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCategoryInfo"></a>
# **getCategoryInfo**
> GetCategoryDetails getCategoryInfo(id)

Get a category details

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
String id = "id_example"; // String | Category ID
try {
    GetCategoryDetails result = apiInstance.getCategoryInfo(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#getCategoryInfo");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Category ID |

### Return type

[**GetCategoryDetails**](GetCategoryDetails.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getOrders"></a>
# **getOrders**
> GetOrders getOrders(limit, offset, sort, modifiedSince, createdSince)

Get order details

Get all the orders

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the orders modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.** 
String createdSince = "createdSince_example"; // String | Filter (urlencoded) the orders created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.** 
try {
    GetOrders result = apiInstance.getOrders(limit, offset, sort, modifiedSince, createdSince);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#getOrders");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]
 **modifiedSince** | **String**| Filter (urlencoded) the orders modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**  | [optional]
 **createdSince** | **String**| Filter (urlencoded) the orders created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**  | [optional]

### Return type

[**GetOrders**](GetOrders.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getProductInfo"></a>
# **getProductInfo**
> GetProductDetails getProductInfo(id)

Get a product&#39;s details

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
String id = "id_example"; // String | Product ID
try {
    GetProductDetails result = apiInstance.getProductInfo(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#getProductInfo");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Product ID |

### Return type

[**GetProductDetails**](GetProductDetails.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getProducts"></a>
# **getProducts**
> GetProducts getProducts(limit, offset, sort, ids, name, priceLte, priceGte, priceLt, priceGt, priceEq, priceNe, categories, modifiedSince, createdSince)

Return all your products

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EcommerceApi;

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

EcommerceApi apiInstance = new EcommerceApi();
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
List<String> ids = Arrays.asList("ids_example"); // List<String> | Filter by product ids
String name = "name_example"; // String | Filter by product name, minimum 3 characters should be present for search
BigDecimal priceLte = new BigDecimal(); // BigDecimal | Price filter for products less than and equals to particular amount
BigDecimal priceGte = new BigDecimal(); // BigDecimal | Price filter for products greater than and equals to particular amount
BigDecimal priceLt = new BigDecimal(); // BigDecimal | Price filter for products less than particular amount
BigDecimal priceGt = new BigDecimal(); // BigDecimal | Price filter for products greater than particular amount
BigDecimal priceEq = new BigDecimal(); // BigDecimal | Price filter for products equals to particular amount
BigDecimal priceNe = new BigDecimal(); // BigDecimal | Price filter for products not equals to particular amount
List<String> categories = Arrays.asList("categories_example"); // List<String> | Filter by category ids
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the orders modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.** 
String createdSince = "createdSince_example"; // String | Filter (urlencoded) the orders created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.** 
try {
    GetProducts result = apiInstance.getProducts(limit, offset, sort, ids, name, priceLte, priceGte, priceLt, priceGt, priceEq, priceNe, categories, modifiedSince, createdSince);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EcommerceApi#getProducts");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]
 **ids** | [**List&lt;String&gt;**](String.md)| Filter by product ids | [optional]
 **name** | **String**| Filter by product name, minimum 3 characters should be present for search | [optional]
 **priceLte** | **BigDecimal**| Price filter for products less than and equals to particular amount | [optional]
 **priceGte** | **BigDecimal**| Price filter for products greater than and equals to particular amount | [optional]
 **priceLt** | **BigDecimal**| Price filter for products less than particular amount | [optional]
 **priceGt** | **BigDecimal**| Price filter for products greater than particular amount | [optional]
 **priceEq** | **BigDecimal**| Price filter for products equals to particular amount | [optional]
 **priceNe** | **BigDecimal**| Price filter for products not equals to particular amount | [optional]
 **categories** | [**List&lt;String&gt;**](String.md)| Filter by category ids | [optional]
 **modifiedSince** | **String**| Filter (urlencoded) the orders modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**  | [optional]
 **createdSince** | **String**| Filter (urlencoded) the orders created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). **Prefer to pass your timezone in date-time format for accurate result.**  | [optional]

### Return type

[**GetProducts**](GetProducts.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

