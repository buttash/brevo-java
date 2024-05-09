# ContactsApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addContactToList**](ContactsApi.md#addContactToList) | **POST** /contacts/lists/{listId}/contacts/add | Add existing contacts to a list
[**createAttribute**](ContactsApi.md#createAttribute) | **POST** /contacts/attributes/{attributeCategory}/{attributeName} | Create contact attribute
[**createContact**](ContactsApi.md#createContact) | **POST** /contacts | Create a contact
[**createDoiContact**](ContactsApi.md#createDoiContact) | **POST** /contacts/doubleOptinConfirmation | Create Contact via DOI (Double-Opt-In) Flow
[**createFolder**](ContactsApi.md#createFolder) | **POST** /contacts/folders | Create a folder
[**createList**](ContactsApi.md#createList) | **POST** /contacts/lists | Create a list
[**deleteAttribute**](ContactsApi.md#deleteAttribute) | **DELETE** /contacts/attributes/{attributeCategory}/{attributeName} | Delete an attribute
[**deleteContact**](ContactsApi.md#deleteContact) | **DELETE** /contacts/{identifier} | Delete a contact
[**deleteFolder**](ContactsApi.md#deleteFolder) | **DELETE** /contacts/folders/{folderId} | Delete a folder (and all its lists)
[**deleteList**](ContactsApi.md#deleteList) | **DELETE** /contacts/lists/{listId} | Delete a list
[**getAttributes**](ContactsApi.md#getAttributes) | **GET** /contacts/attributes | List all attributes
[**getContactInfo**](ContactsApi.md#getContactInfo) | **GET** /contacts/{identifier} | Get a contact&#39;s details
[**getContactStats**](ContactsApi.md#getContactStats) | **GET** /contacts/{identifier}/campaignStats | Get email campaigns&#39; statistics for a contact
[**getContacts**](ContactsApi.md#getContacts) | **GET** /contacts | Get all the contacts
[**getContactsFromList**](ContactsApi.md#getContactsFromList) | **GET** /contacts/lists/{listId}/contacts | Get contacts in a list
[**getFolder**](ContactsApi.md#getFolder) | **GET** /contacts/folders/{folderId} | Returns a folder&#39;s details
[**getFolderLists**](ContactsApi.md#getFolderLists) | **GET** /contacts/folders/{folderId}/lists | Get lists in a folder
[**getFolders**](ContactsApi.md#getFolders) | **GET** /contacts/folders | Get all folders
[**getList**](ContactsApi.md#getList) | **GET** /contacts/lists/{listId} | Get a list&#39;s details
[**getLists**](ContactsApi.md#getLists) | **GET** /contacts/lists | Get all the lists
[**getSegments**](ContactsApi.md#getSegments) | **GET** /contacts/segments | Get all the Segments
[**importContacts**](ContactsApi.md#importContacts) | **POST** /contacts/import | Import contacts
[**removeContactFromList**](ContactsApi.md#removeContactFromList) | **POST** /contacts/lists/{listId}/contacts/remove | Delete a contact from a list
[**requestContactExport**](ContactsApi.md#requestContactExport) | **POST** /contacts/export | Export contacts
[**updateAttribute**](ContactsApi.md#updateAttribute) | **PUT** /contacts/attributes/{attributeCategory}/{attributeName} | Update contact attribute
[**updateBatchContacts**](ContactsApi.md#updateBatchContacts) | **POST** /contacts/batch | Update multiple contacts
[**updateContact**](ContactsApi.md#updateContact) | **PUT** /contacts/{identifier} | Update a contact
[**updateFolder**](ContactsApi.md#updateFolder) | **PUT** /contacts/folders/{folderId} | Update a folder
[**updateList**](ContactsApi.md#updateList) | **PUT** /contacts/lists/{listId} | Update a list


<a name="addContactToList"></a>
# **addContactToList**
> PostContactInfo addContactToList(listId, contactEmails)

Add existing contacts to a list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long listId = 789L; // Long | Id of the list
AddContactToList contactEmails = new AddContactToList(); // AddContactToList | Emails addresses OR IDs of the contacts
try {
    PostContactInfo result = apiInstance.addContactToList(listId, contactEmails);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#addContactToList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **Long**| Id of the list |
 **contactEmails** | [**AddContactToList**](AddContactToList.md)| Emails addresses OR IDs of the contacts |

### Return type

[**PostContactInfo**](PostContactInfo.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createAttribute"></a>
# **createAttribute**
> createAttribute(attributeCategory, attributeName, createAttribute)

Create contact attribute

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String attributeCategory = "attributeCategory_example"; // String | Category of the attribute
String attributeName = "attributeName_example"; // String | Name of the attribute
CreateAttribute createAttribute = new CreateAttribute(); // CreateAttribute | Values to create an attribute
try {
    apiInstance.createAttribute(attributeCategory, attributeName, createAttribute);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#createAttribute");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attributeCategory** | **String**| Category of the attribute | [enum: normal, transactional, category, calculated, global]
 **attributeName** | **String**| Name of the attribute |
 **createAttribute** | [**CreateAttribute**](CreateAttribute.md)| Values to create an attribute |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createContact"></a>
# **createContact**
> CreateUpdateContactModel createContact(createContact)

Create a contact

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
CreateContact createContact = new CreateContact(); // CreateContact | Values to create a contact
try {
    CreateUpdateContactModel result = apiInstance.createContact(createContact);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#createContact");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createContact** | [**CreateContact**](CreateContact.md)| Values to create a contact |

### Return type

[**CreateUpdateContactModel**](CreateUpdateContactModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createDoiContact"></a>
# **createDoiContact**
> createDoiContact(createDoiContact)

Create Contact via DOI (Double-Opt-In) Flow

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
CreateDoiContact createDoiContact = new CreateDoiContact(); // CreateDoiContact | Values to create the Double opt-in (DOI) contact
try {
    apiInstance.createDoiContact(createDoiContact);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#createDoiContact");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createDoiContact** | [**CreateDoiContact**](CreateDoiContact.md)| Values to create the Double opt-in (DOI) contact |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createFolder"></a>
# **createFolder**
> CreateModel createFolder(createFolder)

Create a folder

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
CreateUpdateFolder createFolder = new CreateUpdateFolder(); // CreateUpdateFolder | Name of the folder
try {
    CreateModel result = apiInstance.createFolder(createFolder);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#createFolder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createFolder** | [**CreateUpdateFolder**](CreateUpdateFolder.md)| Name of the folder |

### Return type

[**CreateModel**](CreateModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="createList"></a>
# **createList**
> CreateModel createList(createList)

Create a list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
CreateList createList = new CreateList(); // CreateList | Values to create a list
try {
    CreateModel result = apiInstance.createList(createList);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#createList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createList** | [**CreateList**](CreateList.md)| Values to create a list |

### Return type

[**CreateModel**](CreateModel.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteAttribute"></a>
# **deleteAttribute**
> deleteAttribute(attributeCategory, attributeName)

Delete an attribute

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String attributeCategory = "attributeCategory_example"; // String | Category of the attribute
String attributeName = "attributeName_example"; // String | Name of the existing attribute
try {
    apiInstance.deleteAttribute(attributeCategory, attributeName);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#deleteAttribute");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attributeCategory** | **String**| Category of the attribute | [enum: normal, transactional, category, calculated, global]
 **attributeName** | **String**| Name of the existing attribute |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteContact"></a>
# **deleteContact**
> deleteContact(identifier)

Delete a contact

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String identifier = "identifier_example"; // String | Email (urlencoded) OR ID of the contact
try {
    apiInstance.deleteContact(identifier);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#deleteContact");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identifier** | **String**| Email (urlencoded) OR ID of the contact |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteFolder"></a>
# **deleteFolder**
> deleteFolder(folderId)

Delete a folder (and all its lists)

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long folderId = 789L; // Long | Id of the folder
try {
    apiInstance.deleteFolder(folderId);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#deleteFolder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **Long**| Id of the folder |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteList"></a>
# **deleteList**
> deleteList(listId)

Delete a list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long listId = 789L; // Long | Id of the list
try {
    apiInstance.deleteList(listId);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#deleteList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **Long**| Id of the list |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getAttributes"></a>
# **getAttributes**
> GetAttributes getAttributes()

List all attributes

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
try {
    GetAttributes result = apiInstance.getAttributes();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getAttributes");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetAttributes**](GetAttributes.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getContactInfo"></a>
# **getContactInfo**
> GetExtendedContactDetails getContactInfo(identifier, startDate, endDate)

Get a contact&#39;s details

Along with the contact details, this endpoint will show the statistics of contact for the recent 90 days by default. To fetch the earlier statistics, please use Get contact campaign stats (https://developers.brevo.com/reference/contacts-7#getcontactstats) endpoint with the appropriate date ranges.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String identifier = "identifier_example"; // String | Email (urlencoded) OR ID of the contact OR its SMS attribute value
String startDate = "startDate_example"; // String | **Mandatory if endDate is used.** Starting date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be lower than equal to endDate 
String endDate = "endDate_example"; // String | **Mandatory if startDate is used.** Ending date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be greater than equal to startDate. 
try {
    GetExtendedContactDetails result = apiInstance.getContactInfo(identifier, startDate, endDate);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getContactInfo");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identifier** | **String**| Email (urlencoded) OR ID of the contact OR its SMS attribute value |
 **startDate** | **String**| **Mandatory if endDate is used.** Starting date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be lower than equal to endDate  | [optional]
 **endDate** | **String**| **Mandatory if startDate is used.** Ending date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be greater than equal to startDate.  | [optional]

### Return type

[**GetExtendedContactDetails**](GetExtendedContactDetails.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getContactStats"></a>
# **getContactStats**
> GetContactCampaignStats getContactStats(identifier, startDate, endDate)

Get email campaigns&#39; statistics for a contact

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String identifier = "identifier_example"; // String | Email (urlencoded) OR ID of the contact
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be lower than equal to endDate
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be greater than equal to startDate. Maximum difference between startDate and endDate should not be greater than 90 days
try {
    GetContactCampaignStats result = apiInstance.getContactStats(identifier, startDate, endDate);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getContactStats");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identifier** | **String**| Email (urlencoded) OR ID of the contact |
 **startDate** | **String**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be lower than equal to endDate | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the statistic events specific to campaigns. Must be greater than equal to startDate. Maximum difference between startDate and endDate should not be greater than 90 days | [optional]

### Return type

[**GetContactCampaignStats**](GetContactCampaignStats.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getContacts"></a>
# **getContacts**
> GetContacts getContacts(limit, offset, modifiedSince, createdSince, sort, segmentId, listIds)

Get all the contacts

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document of the page
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
String createdSince = "createdSince_example"; // String | Filter (urlencoded) the contacts created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
Long segmentId = 789L; // Long | Id of the segment. **Either listIds or segmentId can be passed.**
List<Long> listIds = Arrays.asList(56L); // List<Long> | Ids of the list. **Either listIds or segmentId can be passed.**
try {
    GetContacts result = apiInstance.getContacts(limit, offset, modifiedSince, createdSince, sort, segmentId, listIds);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getContacts");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document of the page | [optional] [default to 0]
 **modifiedSince** | **String**| Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **createdSince** | **String**| Filter (urlencoded) the contacts created after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]
 **segmentId** | **Long**| Id of the segment. **Either listIds or segmentId can be passed.** | [optional]
 **listIds** | [**List&lt;Long&gt;**](Long.md)| Ids of the list. **Either listIds or segmentId can be passed.** | [optional]

### Return type

[**GetContacts**](GetContacts.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getContactsFromList"></a>
# **getContactsFromList**
> GetContacts getContactsFromList(listId, modifiedSince, limit, offset, sort)

Get contacts in a list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long listId = 789L; // Long | Id of the list
String modifiedSince = "modifiedSince_example"; // String | Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result.
Long limit = 50L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document of the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetContacts result = apiInstance.getContactsFromList(listId, modifiedSince, limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getContactsFromList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **Long**| Id of the list |
 **modifiedSince** | **String**| Filter (urlencoded) the contacts modified after a given UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ). Prefer to pass your timezone in date-time format for accurate result. | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 50]
 **offset** | **Long**| Index of the first document of the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetContacts**](GetContacts.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getFolder"></a>
# **getFolder**
> GetFolder getFolder(folderId)

Returns a folder&#39;s details

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long folderId = 789L; // Long | id of the folder
try {
    GetFolder result = apiInstance.getFolder(folderId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getFolder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **Long**| id of the folder |

### Return type

[**GetFolder**](GetFolder.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getFolderLists"></a>
# **getFolderLists**
> GetFolderLists getFolderLists(folderId, limit, offset, sort)

Get lists in a folder

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long folderId = 789L; // Long | Id of the folder
Long limit = 10L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document of the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetFolderLists result = apiInstance.getFolderLists(folderId, limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getFolderLists");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **Long**| Id of the folder |
 **limit** | **Long**| Number of documents per page | [optional] [default to 10]
 **offset** | **Long**| Index of the first document of the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetFolderLists**](GetFolderLists.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getFolders"></a>
# **getFolders**
> GetFolders getFolders(limit, offset, sort)

Get all folders

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long limit = 10L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document of the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetFolders result = apiInstance.getFolders(limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getFolders");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [default to 10]
 **offset** | **Long**| Index of the first document of the page | [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetFolders**](GetFolders.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getList"></a>
# **getList**
> GetExtendedList getList(listId, startDate, endDate)

Get a list&#39;s details

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long listId = 789L; // Long | Id of the list
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to aggregate the sent email campaigns for a specific list id.Prefer to pass your timezone in date-time format for accurate result
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to aggregate the sent email campaigns for a specific list id.Prefer to pass your timezone in date-time format for accurate result
try {
    GetExtendedList result = apiInstance.getList(listId, startDate, endDate);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **Long**| Id of the list |
 **startDate** | **String**| Mandatory if endDate is used. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to aggregate the sent email campaigns for a specific list id.Prefer to pass your timezone in date-time format for accurate result | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Ending (urlencoded) UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) to aggregate the sent email campaigns for a specific list id.Prefer to pass your timezone in date-time format for accurate result | [optional]

### Return type

[**GetExtendedList**](GetExtendedList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getLists"></a>
# **getLists**
> GetLists getLists(limit, offset, sort)

Get all the lists

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long limit = 10L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document of the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetLists result = apiInstance.getLists(limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getLists");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [optional] [default to 10]
 **offset** | **Long**| Index of the first document of the page | [optional] [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetLists**](GetLists.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getSegments"></a>
# **getSegments**
> GetSegments getSegments(limit, offset, sort)

Get all the Segments

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long limit = 10L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document of the page
String sort = "desc"; // String | Sort the results in the ascending/descending order of record creation. Default order is **descending** if `sort` is not passed
try {
    GetSegments result = apiInstance.getSegments(limit, offset, sort);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#getSegments");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Long**| Number of documents per page | [default to 10]
 **offset** | **Long**| Index of the first document of the page | [default to 0]
 **sort** | **String**| Sort the results in the ascending/descending order of record creation. Default order is **descending** if &#x60;sort&#x60; is not passed | [optional] [default to desc] [enum: asc, desc]

### Return type

[**GetSegments**](GetSegments.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="importContacts"></a>
# **importContacts**
> CreatedProcessId importContacts(requestContactImport)

Import contacts

It returns the background process ID which on completion calls the notify URL that you have set in the input.  **Note**: - Any contact attribute that doesn&#39;t exist in your account will be ignored at import end. 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
RequestContactImport requestContactImport = new RequestContactImport(); // RequestContactImport | Values to import contacts in Brevo. To know more about the expected format, please have a look at ``https://help.brevo.com/hc/en-us/articles/209499265-Build-contacts-lists-for-your-email-marketing-campaigns``
try {
    CreatedProcessId result = apiInstance.importContacts(requestContactImport);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#importContacts");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestContactImport** | [**RequestContactImport**](RequestContactImport.md)| Values to import contacts in Brevo. To know more about the expected format, please have a look at &#x60;&#x60;https://help.brevo.com/hc/en-us/articles/209499265-Build-contacts-lists-for-your-email-marketing-campaigns&#x60;&#x60; |

### Return type

[**CreatedProcessId**](CreatedProcessId.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="removeContactFromList"></a>
# **removeContactFromList**
> PostContactInfo removeContactFromList(listId, contactEmails)

Delete a contact from a list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long listId = 789L; // Long | Id of the list
RemoveContactFromList contactEmails = new RemoveContactFromList(); // RemoveContactFromList | Emails addresses OR IDs of the contacts
try {
    PostContactInfo result = apiInstance.removeContactFromList(listId, contactEmails);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#removeContactFromList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **Long**| Id of the list |
 **contactEmails** | [**RemoveContactFromList**](RemoveContactFromList.md)| Emails addresses OR IDs of the contacts |

### Return type

[**PostContactInfo**](PostContactInfo.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="requestContactExport"></a>
# **requestContactExport**
> CreatedProcessId requestContactExport(requestContactExport)

Export contacts

It returns the background process ID which on completion calls the notify URL that you have set in the input. File will be available in csv.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
RequestContactExport requestContactExport = new RequestContactExport(); // RequestContactExport | Values to request a contact export
try {
    CreatedProcessId result = apiInstance.requestContactExport(requestContactExport);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#requestContactExport");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestContactExport** | [**RequestContactExport**](RequestContactExport.md)| Values to request a contact export |

### Return type

[**CreatedProcessId**](CreatedProcessId.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateAttribute"></a>
# **updateAttribute**
> updateAttribute(attributeCategory, attributeName, updateAttribute)

Update contact attribute

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String attributeCategory = "attributeCategory_example"; // String | Category of the attribute
String attributeName = "attributeName_example"; // String | Name of the existing attribute
UpdateAttribute updateAttribute = new UpdateAttribute(); // UpdateAttribute | Values to update an attribute
try {
    apiInstance.updateAttribute(attributeCategory, attributeName, updateAttribute);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#updateAttribute");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attributeCategory** | **String**| Category of the attribute | [enum: category, calculated, global]
 **attributeName** | **String**| Name of the existing attribute |
 **updateAttribute** | [**UpdateAttribute**](UpdateAttribute.md)| Values to update an attribute |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateBatchContacts"></a>
# **updateBatchContacts**
> updateBatchContacts(updateBatchContacts)

Update multiple contacts

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
UpdateBatchContacts updateBatchContacts = new UpdateBatchContacts(); // UpdateBatchContacts | Values to update multiple contacts
try {
    apiInstance.updateBatchContacts(updateBatchContacts);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#updateBatchContacts");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **updateBatchContacts** | [**UpdateBatchContacts**](UpdateBatchContacts.md)| Values to update multiple contacts |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateContact"></a>
# **updateContact**
> updateContact(identifier, updateContact)

Update a contact

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
String identifier = "identifier_example"; // String | Email (urlencoded) OR ID of the contact
UpdateContact updateContact = new UpdateContact(); // UpdateContact | Values to update a contact
try {
    apiInstance.updateContact(identifier, updateContact);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#updateContact");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identifier** | **String**| Email (urlencoded) OR ID of the contact |
 **updateContact** | [**UpdateContact**](UpdateContact.md)| Values to update a contact |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateFolder"></a>
# **updateFolder**
> updateFolder(folderId, updateFolder)

Update a folder

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long folderId = 789L; // Long | Id of the folder
CreateUpdateFolder updateFolder = new CreateUpdateFolder(); // CreateUpdateFolder | Name of the folder
try {
    apiInstance.updateFolder(folderId, updateFolder);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#updateFolder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **Long**| Id of the folder |
 **updateFolder** | [**CreateUpdateFolder**](CreateUpdateFolder.md)| Name of the folder |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="updateList"></a>
# **updateList**
> updateList(listId, updateList)

Update a list

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.ContactsApi;

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

ContactsApi apiInstance = new ContactsApi();
Long listId = 789L; // Long | Id of the list
UpdateList updateList = new UpdateList(); // UpdateList | Values to update a list
try {
    apiInstance.updateList(listId, updateList);
} catch (ApiException e) {
    System.err.println("Exception when calling ContactsApi#updateList");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **Long**| Id of the list |
 **updateList** | [**UpdateList**](UpdateList.md)| Values to update a list |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

