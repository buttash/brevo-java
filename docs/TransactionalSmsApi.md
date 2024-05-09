# TransactionalSmsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSmsEvents**](TransactionalSmsApi.md#getSmsEvents) | **GET** /transactionalSMS/statistics/events | Get all your SMS activity (unaggregated events)
[**getTransacAggregatedSmsReport**](TransactionalSmsApi.md#getTransacAggregatedSmsReport) | **GET** /transactionalSMS/statistics/aggregatedReport | Get your SMS activity aggregated over a period of time
[**getTransacSmsReport**](TransactionalSmsApi.md#getTransacSmsReport) | **GET** /transactionalSMS/statistics/reports | Get your SMS activity aggregated per day
[**sendTransacSms**](TransactionalSmsApi.md#sendTransacSms) | **POST** /transactionalSMS/sms | Send SMS message to a mobile number


<a name="getSmsEvents"></a>
# **getSmsEvents**
> GetSmsEventReport getSmsEvents(limit, startDate, endDate, offset, days, phoneNumber, event, tags, sort)

Get all your SMS activity (unaggregated events)

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TransactionalSmsApi;

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

TransactionalSmsApi apiInstance = new TransactionalSmsApi();
Long limit = 50L; // Long | Number of documents per page
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
Long offset = 0L; // Long | Index of the first document of the page
Long days = 789L; // Long | Number of days in the past including today (positive integer). Not compatible with 'startDate' and 'endDate'
String phoneNumber = "phoneNumber_example"; // String | Filter the report for a specific phone number
String event = "event_example"; // String | Filter the report for specific events
String tags = "tags_example"; // String | Filter the report for specific tags passed as a serialized urlencoded array
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetSmsEventReport result = apiInstance.getSmsEvents(limit, startDate, endDate, offset, days, phoneNumber, event, tags, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TransactionalSmsApi#getSmsEvents");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **startDate** | **String**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional]
 **offset** | **Long**| Index of the first document of the page | [optional] [default to 0]
 **days** | **Long**| Number of days in the past including today (positive integer). Not compatible with &#39;startDate&#39; and &#39;endDate&#39; | [optional]
 **phoneNumber** | **String**| Filter the report for a specific phone number | [optional]
 **event** | **String**| Filter the report for specific events | [optional] [enum: bounces, hardBounces, softBounces, delivered, sent, accepted, unsubscription, replies, blocked, rejected]
 **tags** | **String**| Filter the report for specific tags passed as a serialized urlencoded array | [optional]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetSmsEventReport**](GetSmsEventReport.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getTransacAggregatedSmsReport"></a>
# **getTransacAggregatedSmsReport**
> GetTransacAggregatedSmsReport getTransacAggregatedSmsReport(startDate, endDate, days, tag)

Get your SMS activity aggregated over a period of time

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TransactionalSmsApi;

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

TransactionalSmsApi apiInstance = new TransactionalSmsApi();
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
Long days = 789L; // Long | Number of days in the past including today (positive integer). Not compatible with startDate and endDate
String tag = "tag_example"; // String | Filter on a tag
try {
    GetTransacAggregatedSmsReport result = apiInstance.getTransacAggregatedSmsReport(startDate, endDate, days, tag);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TransactionalSmsApi#getTransacAggregatedSmsReport");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional]
 **days** | **Long**| Number of days in the past including today (positive integer). Not compatible with startDate and endDate | [optional]
 **tag** | **String**| Filter on a tag | [optional]

### Return type

[**GetTransacAggregatedSmsReport**](GetTransacAggregatedSmsReport.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getTransacSmsReport"></a>
# **getTransacSmsReport**
> GetTransacSmsReport getTransacSmsReport(startDate, endDate, days, tag, sort)

Get your SMS activity aggregated per day

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TransactionalSmsApi;

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

TransactionalSmsApi apiInstance = new TransactionalSmsApi();
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
Long days = 789L; // Long | Number of days in the past including today (positive integer). Not compatible with 'startDate' and 'endDate'
String tag = "tag_example"; // String | Filter on a tag
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetTransacSmsReport result = apiInstance.getTransacSmsReport(startDate, endDate, days, tag, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TransactionalSmsApi#getTransacSmsReport");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional]
 **days** | **Long**| Number of days in the past including today (positive integer). Not compatible with &#39;startDate&#39; and &#39;endDate&#39; | [optional]
 **tag** | **String**| Filter on a tag | [optional]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetTransacSmsReport**](GetTransacSmsReport.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendTransacSms"></a>
# **sendTransacSms**
> SendSms sendTransacSms(sendTransacSms)

Send SMS message to a mobile number

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TransactionalSmsApi;

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

TransactionalSmsApi apiInstance = new TransactionalSmsApi();
SendTransacSms sendTransacSms = new SendTransacSms(); // SendTransacSms | Values to send a transactional SMS
try {
    SendSms result = apiInstance.sendTransacSms(sendTransacSms);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TransactionalSmsApi#sendTransacSms");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendTransacSms** | [**SendTransacSms**](SendTransacSms.md)| Values to send a transactional SMS |

### Return type

[**SendSms**](SendSms.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

