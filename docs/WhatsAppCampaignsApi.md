# WhatsAppCampaignsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createWhatsAppCampaign**](WhatsAppCampaignsApi.md#createWhatsAppCampaign) | **POST** /whatsappCampaigns | Create and Send a WhatsApp campaign
[**createWhatsAppTemplate**](WhatsAppCampaignsApi.md#createWhatsAppTemplate) | **POST** /whatsppCampaigns/template | Create a WhatsApp template
[**deleteWhatsAppCampaign**](WhatsAppCampaignsApi.md#deleteWhatsAppCampaign) | **DELETE** /whatsappCampaigns/{campaignId} | Delete a WhatsApp campaign
[**getWhatsAppCampaign**](WhatsAppCampaignsApi.md#getWhatsAppCampaign) | **GET** /whatsappCampaigns/{campaignId} | Get a WhatsApp campaign
[**getWhatsAppCampaigns**](WhatsAppCampaignsApi.md#getWhatsAppCampaigns) | **GET** /whatsappCampaigns | Return all your created WhatsApp campaigns
[**getWhatsAppConfig**](WhatsAppCampaignsApi.md#getWhatsAppConfig) | **GET** /whatsappCampaigns/config | Get your WhatsApp API account information
[**getWhatsAppTemplates**](WhatsAppCampaignsApi.md#getWhatsAppTemplates) | **GET** /whatsappCampaigns/template-list | Return all your created WhatsApp templates
[**sendWhatsAppTemplateApproval**](WhatsAppCampaignsApi.md#sendWhatsAppTemplateApproval) | **POST** /whatsappCampaigns/template/approval/{templateId} | Send your WhatsApp template for approval
[**updateWhatsAppCampaign**](WhatsAppCampaignsApi.md#updateWhatsAppCampaign) | **PUT** /whatsappCampaigns/{campaignId} | Update a WhatsApp campaign


<a name="createWhatsAppCampaign"></a>
# **createWhatsAppCampaign**
> CreateModel createWhatsAppCampaign(whatsAppCampaigns)

Create and Send a WhatsApp campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
CreateWhatsAppCampaign whatsAppCampaigns = new CreateWhatsAppCampaign(); // CreateWhatsAppCampaign | Values to create a campaign
try {
    CreateModel result = apiInstance.createWhatsAppCampaign(whatsAppCampaigns);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#createWhatsAppCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **whatsAppCampaigns** | [**CreateWhatsAppCampaign**](CreateWhatsAppCampaign.md)| Values to create a campaign |

### Return type

[**CreateModel**](CreateModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createWhatsAppTemplate"></a>
# **createWhatsAppTemplate**
> CreateModel createWhatsAppTemplate(whatsAppTemplates)

Create a WhatsApp template

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
CreateWhatsAppTemplate whatsAppTemplates = new CreateWhatsAppTemplate(); // CreateWhatsAppTemplate | Values to create a template
try {
    CreateModel result = apiInstance.createWhatsAppTemplate(whatsAppTemplates);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#createWhatsAppTemplate");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **whatsAppTemplates** | [**CreateWhatsAppTemplate**](CreateWhatsAppTemplate.md)| Values to create a template |

### Return type

[**CreateModel**](CreateModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteWhatsAppCampaign"></a>
# **deleteWhatsAppCampaign**
> deleteWhatsAppCampaign(campaignId)

Delete a WhatsApp campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
Long campaignId = 789L; // Long | id of the campaign
try {
    apiInstance.deleteWhatsAppCampaign(campaignId);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#deleteWhatsAppCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| id of the campaign |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getWhatsAppCampaign"></a>
# **getWhatsAppCampaign**
> GetWhatsappCampaignOverview getWhatsAppCampaign(campaignId)

Get a WhatsApp campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
try {
    GetWhatsappCampaignOverview result = apiInstance.getWhatsAppCampaign(campaignId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#getWhatsAppCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |

### Return type

[**GetWhatsappCampaignOverview**](GetWhatsappCampaignOverview.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getWhatsAppCampaigns"></a>
# **getWhatsAppCampaigns**
> GetWhatsappCampaigns getWhatsAppCampaigns(startDate, endDate, limit, offset, sort)

Return all your created WhatsApp campaigns

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
String startDate = "startDate_example"; // String | **Mandatory if endDate is used**. Starting (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the campaigns created. **Prefer to pass your timezone in date-time format for accurate result** 
String endDate = "endDate_example"; // String | **Mandatory if startDate is used**. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the campaigns created. **Prefer to pass your timezone in date-time format for accurate result** 
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record modification. Default order is **descending** if `sort` is not passed
try {
    GetWhatsappCampaigns result = apiInstance.getWhatsAppCampaigns(startDate, endDate, limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#getWhatsAppCampaigns");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| **Mandatory if endDate is used**. Starting (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the campaigns created. **Prefer to pass your timezone in date-time format for accurate result**  | [optional]
 **endDate** | **String**| **Mandatory if startDate is used**. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the campaigns created. **Prefer to pass your timezone in date-time format for accurate result**  | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record modification. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetWhatsappCampaigns**](GetWhatsappCampaigns.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getWhatsAppConfig"></a>
# **getWhatsAppConfig**
> GetWhatsAppConfig getWhatsAppConfig()

Get your WhatsApp API account information

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
try {
    GetWhatsAppConfig result = apiInstance.getWhatsAppConfig();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#getWhatsAppConfig");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetWhatsAppConfig**](GetWhatsAppConfig.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getWhatsAppTemplates"></a>
# **getWhatsAppTemplates**
> GetWATemplates getWhatsAppTemplates(startDate, endDate, limit, offset, sort, source)

Return all your created WhatsApp templates

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
String startDate = "startDate_example"; // String | **Mandatory if endDate is used**. Starting (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the templates created. **Prefer to pass your timezone in date-time format for accurate result** 
String endDate = "endDate_example"; // String | **Mandatory if startDate is used**. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the templates created. **Prefer to pass your timezone in date-time format for accurate result** 
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record modification. Default order is **descending** if `sort` is not passed
String source = "source_example"; // String | source of the template
try {
    GetWATemplates result = apiInstance.getWhatsAppTemplates(startDate, endDate, limit, offset, sort, source);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#getWhatsAppTemplates");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| **Mandatory if endDate is used**. Starting (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the templates created. **Prefer to pass your timezone in date-time format for accurate result**  | [optional]
 **endDate** | **String**| **Mandatory if startDate is used**. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the templates created. **Prefer to pass your timezone in date-time format for accurate result**  | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record modification. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]
 **source** | **String**| source of the template | [optional] [enum: Automation, Conversations]

### Return type

[**GetWATemplates**](GetWATemplates.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendWhatsAppTemplateApproval"></a>
# **sendWhatsAppTemplateApproval**
> sendWhatsAppTemplateApproval(templateId)

Send your WhatsApp template for approval

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
Long templateId = 789L; // Long | id of the campaign
try {
    apiInstance.sendWhatsAppTemplateApproval(templateId);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#sendWhatsAppTemplateApproval");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **templateId** | **Long**| id of the campaign |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateWhatsAppCampaign"></a>
# **updateWhatsAppCampaign**
> updateWhatsAppCampaign(campaignId, whatsAppCampaign)

Update a WhatsApp campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.WhatsAppCampaignsApi;

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

WhatsAppCampaignsApi apiInstance = new WhatsAppCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
UpdateWhatsAppCampaign whatsAppCampaign = new UpdateWhatsAppCampaign(); // UpdateWhatsAppCampaign | values to update WhatsApp Campaign
try {
    apiInstance.updateWhatsAppCampaign(campaignId, whatsAppCampaign);
} catch (ApiException e) {
    System.err.println("Exception when calling WhatsAppCampaignsApi#updateWhatsAppCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **whatsAppCampaign** | [**UpdateWhatsAppCampaign**](UpdateWhatsAppCampaign.md)| values to update WhatsApp Campaign | [optional]

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

