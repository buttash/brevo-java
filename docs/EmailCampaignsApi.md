# EmailCampaignsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createEmailCampaign**](EmailCampaignsApi.md#createEmailCampaign) | **POST** /emailCampaigns | Create an email campaign
[**deleteEmailCampaign**](EmailCampaignsApi.md#deleteEmailCampaign) | **DELETE** /emailCampaigns/{campaignId} | Delete an email campaign
[**emailExportRecipients**](EmailCampaignsApi.md#emailExportRecipients) | **POST** /emailCampaigns/{campaignId}/exportRecipients | Export the recipients of an email campaign
[**getAbTestCampaignResult**](EmailCampaignsApi.md#getAbTestCampaignResult) | **GET** /emailCampaigns/{campaignId}/abTestCampaignResult | Get an A/B test email campaign results
[**getEmailCampaign**](EmailCampaignsApi.md#getEmailCampaign) | **GET** /emailCampaigns/{campaignId} | Get an email campaign report
[**getEmailCampaigns**](EmailCampaignsApi.md#getEmailCampaigns) | **GET** /emailCampaigns | Return all your created email campaigns
[**getSharedTemplateUrl**](EmailCampaignsApi.md#getSharedTemplateUrl) | **GET** /emailCampaigns/{campaignId}/sharedUrl | Get a shared template url
[**sendEmailCampaignNow**](EmailCampaignsApi.md#sendEmailCampaignNow) | **POST** /emailCampaigns/{campaignId}/sendNow | Send an email campaign immediately, based on campaignId
[**sendReport**](EmailCampaignsApi.md#sendReport) | **POST** /emailCampaigns/{campaignId}/sendReport | Send the report of a campaign
[**sendTestEmail**](EmailCampaignsApi.md#sendTestEmail) | **POST** /emailCampaigns/{campaignId}/sendTest | Send an email campaign to your test list
[**updateCampaignStatus**](EmailCampaignsApi.md#updateCampaignStatus) | **PUT** /emailCampaigns/{campaignId}/status | Update an email campaign status
[**updateEmailCampaign**](EmailCampaignsApi.md#updateEmailCampaign) | **PUT** /emailCampaigns/{campaignId} | Update an email campaign
[**uploadImageToGallery**](EmailCampaignsApi.md#uploadImageToGallery) | **POST** /emailCampaigns/images | Upload an image to your account&#39;s image gallery


<a name="createEmailCampaign"></a>
# **createEmailCampaign**
> CreateModel createEmailCampaign(emailCampaigns)

Create an email campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
CreateEmailCampaign emailCampaigns = new CreateEmailCampaign(); // CreateEmailCampaign | Values to create a campaign
try {
    CreateModel result = apiInstance.createEmailCampaign(emailCampaigns);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#createEmailCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emailCampaigns** | [**CreateEmailCampaign**](CreateEmailCampaign.md)| Values to create a campaign |

### Return type

[**CreateModel**](CreateModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteEmailCampaign"></a>
# **deleteEmailCampaign**
> deleteEmailCampaign(campaignId)

Delete an email campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | id of the campaign
try {
    apiInstance.deleteEmailCampaign(campaignId);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#deleteEmailCampaign");
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

<a name="emailExportRecipients"></a>
# **emailExportRecipients**
> CreatedProcessId emailExportRecipients(campaignId, recipientExport)

Export the recipients of an email campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
EmailExportRecipients recipientExport = new EmailExportRecipients(); // EmailExportRecipients | Values to send for a recipient export request
try {
    CreatedProcessId result = apiInstance.emailExportRecipients(campaignId, recipientExport);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#emailExportRecipients");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **recipientExport** | [**EmailExportRecipients**](EmailExportRecipients.md)| Values to send for a recipient export request | [optional]

### Return type

[**CreatedProcessId**](CreatedProcessId.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getAbTestCampaignResult"></a>
# **getAbTestCampaignResult**
> AbTestCampaignResult getAbTestCampaignResult(campaignId)

Get an A/B test email campaign results

Obtain winning version of an A/B test email campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the A/B test campaign
try {
    AbTestCampaignResult result = apiInstance.getAbTestCampaignResult(campaignId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#getAbTestCampaignResult");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the A/B test campaign |

### Return type

[**AbTestCampaignResult**](AbTestCampaignResult.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getEmailCampaign"></a>
# **getEmailCampaign**
> GetEmailCampaign getEmailCampaign(campaignId, statistics)

Get an email campaign report

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
String statistics = "statistics_example"; // String | Filter on the type of statistics required. Example **globalStats** value will only fetch globalStats info of the campaign in returned response.
try {
    GetEmailCampaign result = apiInstance.getEmailCampaign(campaignId, statistics);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#getEmailCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **statistics** | **String**| Filter on the type of statistics required. Example **globalStats** value will only fetch globalStats info of the campaign in returned response. | [optional] [enum: globalStats, linksStats, statsByDomain, statsByDevice, statsByBrowser]

### Return type

[**GetEmailCampaign**](GetEmailCampaign.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getEmailCampaigns"></a>
# **getEmailCampaigns**
> GetEmailCampaigns getEmailCampaigns(type, status, statistics, startDate, endDate, limit, offset, sort, excludeHtmlContent)

Return all your created email campaigns

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
String type = "type_example"; // String | Filter on the type of the campaigns
String status = "status_example"; // String | Filter on the status of the campaign
String statistics = "statistics_example"; // String | Filter on the type of statistics required. Example **globalStats** value will only fetch globalStats info of the campaign in returned response.
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Starting (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the sent email campaigns. Prefer to pass your timezone in date-time format for accurate result ( only available if either 'status' not passed and if passed is set to 'sent' )
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the sent email campaigns. Prefer to pass your timezone in date-time format for accurate result ( only available if either 'status' not passed and if passed is set to 'sent' )
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
Boolean excludeHtmlContent = true; // Boolean | Use this flag to exclude htmlContent from the response body. If set to **true**, htmlContent field will be returned as empty string in the response body
try {
    GetEmailCampaigns result = apiInstance.getEmailCampaigns(type, status, statistics, startDate, endDate, limit, offset, sort, excludeHtmlContent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#getEmailCampaigns");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **String**| Filter on the type of the campaigns | [optional] [enum: classic, trigger]
 **status** | **String**| Filter on the status of the campaign | [optional] [enum: suspended, archive, sent, queued, draft, inProcess]
 **statistics** | **String**| Filter on the type of statistics required. Example **globalStats** value will only fetch globalStats info of the campaign in returned response. | [optional] [enum: globalStats, linksStats, statsByDomain]
 **startDate** | **String**| Mandatory if endDate is used. Starting (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the sent email campaigns. Prefer to pass your timezone in date-time format for accurate result ( only available if either &#39;status&#39; not passed and if passed is set to &#39;sent&#39; ) | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to filter the sent email campaigns. Prefer to pass your timezone in date-time format for accurate result ( only available if either &#39;status&#39; not passed and if passed is set to &#39;sent&#39; ) | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document in the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]
 **excludeHtmlContent** | **Boolean**| Use this flag to exclude htmlContent from the response body. If set to **true**, htmlContent field will be returned as empty string in the response body | [optional]

### Return type

[**GetEmailCampaigns**](GetEmailCampaigns.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getSharedTemplateUrl"></a>
# **getSharedTemplateUrl**
> GetSharedTemplateUrl getSharedTemplateUrl(campaignId)

Get a shared template url

Get a unique URL to share &amp; import an email template from one Brevo account to another.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign or template
try {
    GetSharedTemplateUrl result = apiInstance.getSharedTemplateUrl(campaignId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#getSharedTemplateUrl");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign or template |

### Return type

[**GetSharedTemplateUrl**](GetSharedTemplateUrl.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendEmailCampaignNow"></a>
# **sendEmailCampaignNow**
> sendEmailCampaignNow(campaignId)

Send an email campaign immediately, based on campaignId

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
try {
    apiInstance.sendEmailCampaignNow(campaignId);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#sendEmailCampaignNow");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendReport"></a>
# **sendReport**
> sendReport(campaignId, sendReport)

Send the report of a campaign

A PDF will be sent to the specified email addresses

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
SendReport sendReport = new SendReport(); // SendReport | Values for send a report
try {
    apiInstance.sendReport(campaignId, sendReport);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#sendReport");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **sendReport** | [**SendReport**](SendReport.md)| Values for send a report |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendTestEmail"></a>
# **sendTestEmail**
> sendTestEmail(campaignId, emailTo)

Send an email campaign to your test list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
SendTestEmail emailTo = new SendTestEmail(); // SendTestEmail | 
try {
    apiInstance.sendTestEmail(campaignId, emailTo);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#sendTestEmail");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **emailTo** | [**SendTestEmail**](SendTestEmail.md)|  |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateCampaignStatus"></a>
# **updateCampaignStatus**
> updateCampaignStatus(campaignId, status)

Update an email campaign status

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
UpdateCampaignStatus status = new UpdateCampaignStatus(); // UpdateCampaignStatus | Status of the campaign
try {
    apiInstance.updateCampaignStatus(campaignId, status);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#updateCampaignStatus");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **status** | [**UpdateCampaignStatus**](UpdateCampaignStatus.md)| Status of the campaign |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateEmailCampaign"></a>
# **updateEmailCampaign**
> updateEmailCampaign(campaignId, emailCampaign)

Update an email campaign

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
Long campaignId = 789L; // Long | Id of the campaign
UpdateEmailCampaign emailCampaign = new UpdateEmailCampaign(); // UpdateEmailCampaign | Values to update a campaign
try {
    apiInstance.updateEmailCampaign(campaignId, emailCampaign);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#updateEmailCampaign");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignId** | **Long**| Id of the campaign |
 **emailCampaign** | [**UpdateEmailCampaign**](UpdateEmailCampaign.md)| Values to update a campaign |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="uploadImageToGallery"></a>
# **uploadImageToGallery**
> UploadImageModel uploadImageToGallery(uploadImage)

Upload an image to your account&#39;s image gallery

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.EmailCampaignsApi;

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

EmailCampaignsApi apiInstance = new EmailCampaignsApi();
UploadImageToGallery uploadImage = new UploadImageToGallery(); // UploadImageToGallery | Parameters to upload an image
try {
    UploadImageModel result = apiInstance.uploadImageToGallery(uploadImage);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling EmailCampaignsApi#uploadImageToGallery");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uploadImage** | [**UploadImageToGallery**](UploadImageToGallery.md)| Parameters to upload an image |

### Return type

[**UploadImageModel**](UploadImageModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

