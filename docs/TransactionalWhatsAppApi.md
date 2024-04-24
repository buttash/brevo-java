# TransactionalWhatsAppApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getWhatsappEventReport**](TransactionalWhatsAppApi.md#getWhatsappEventReport) | **GET** /whatsapp/statistics/events | Get all your WhatsApp activity (unaggregated events)
[**sendWhatsappMessage**](TransactionalWhatsAppApi.md#sendWhatsappMessage) | **POST** /whatsapp/sendMessage | Send a WhatsApp message


<a name="getWhatsappEventReport"></a>
# **getWhatsappEventReport**
> GetWhatsappEventReport getWhatsappEventReport(limit, offset, startDate, endDate, days, contactNumber, event, sort)

Get all your WhatsApp activity (unaggregated events)

This endpoint will show the unaggregated statistics for WhatsApp activity (30 days by default if &#x60;startDate&#x60; and &#x60;endDate&#x60; or &#x60;days&#x60; is not passed. The date range can not exceed 90 days)

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TransactionalWhatsAppApi;

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

TransactionalWhatsAppApi apiInstance = new TransactionalWhatsAppApi();
Long limit = 2500L; // Long | Number limitation for the result returned
Long offset = 0L; // Long | Beginning point in the list to retrieve from
String startDate = "startDate_example"; // String | **Mandatory if endDate is used.** Starting date of the report (YYYY-MM-DD). Must be lower than equal to endDate 
String endDate = "endDate_example"; // String | **Mandatory if startDate is used.** Ending date of the report (YYYY-MM-DD). Must be greater than equal to startDate 
Long days = 789L; // Long | Number of days in the past including today (positive integer). _Not compatible with 'startDate' and 'endDate'_ 
String contactNumber = "contactNumber_example"; // String | Filter results for specific contact (WhatsApp Number with country code. Example, 85264318721)
String event = "event_example"; // String | Filter the report for a specific event type
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetWhatsappEventReport result = apiInstance.getWhatsappEventReport(limit, offset, startDate, endDate, days, contactNumber, event, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TransactionalWhatsAppApi#getWhatsappEventReport");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number limitation for the result returned | [optional] [default to 2500]
 **offset** | **Long**| Beginning point in the list to retrieve from | [optional] [default to 0]
 **startDate** | **String**| **Mandatory if endDate is used.** Starting date of the report (YYYY-MM-DD). Must be lower than equal to endDate  | [optional]
 **endDate** | **String**| **Mandatory if startDate is used.** Ending date of the report (YYYY-MM-DD). Must be greater than equal to startDate  | [optional]
 **days** | **Long**| Number of days in the past including today (positive integer). _Not compatible with &#39;startDate&#39; and &#39;endDate&#39;_  | [optional]
 **contactNumber** | **String**| Filter results for specific contact (WhatsApp Number with country code. Example, 85264318721) | [optional]
 **event** | **String**| Filter the report for a specific event type | [optional] [enum: sent, delivered, read, error, unsubscribe, reply, soft-bounce]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetWhatsappEventReport**](GetWhatsappEventReport.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendWhatsappMessage"></a>
# **sendWhatsappMessage**
> InlineResponse2014 sendWhatsappMessage(sendWhatsappMessage)

Send a WhatsApp message

This endpoint is used to send a WhatsApp message. &lt;br/&gt;(**The first message you send using the API must contain a Template ID. You must create a template on WhatsApp on the Brevo platform to fetch the Template ID.**)

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.TransactionalWhatsAppApi;

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

TransactionalWhatsAppApi apiInstance = new TransactionalWhatsAppApi();
SendWhatsappMessage sendWhatsappMessage = new SendWhatsappMessage(); // SendWhatsappMessage | Values to send WhatsApp message
try {
    InlineResponse2014 result = apiInstance.sendWhatsappMessage(sendWhatsappMessage);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling TransactionalWhatsAppApi#sendWhatsappMessage");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendWhatsappMessage** | [**SendWhatsappMessage**](SendWhatsappMessage.md)| Values to send WhatsApp message |

### Return type

[**InlineResponse2014**](InlineResponse2014.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

