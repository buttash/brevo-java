# MasterAccountApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**corporateGroupIdDelete**](MasterAccountApi.md#corporateGroupIdDelete) | **DELETE** /corporate/group/{id} | Delete a group
[**corporateGroupIdGet**](MasterAccountApi.md#corporateGroupIdGet) | **GET** /corporate/group/{id} | GET a group details
[**corporateGroupIdPut**](MasterAccountApi.md#corporateGroupIdPut) | **PUT** /corporate/group/{id} | Update a group of sub-accounts
[**corporateGroupPost**](MasterAccountApi.md#corporateGroupPost) | **POST** /corporate/group | Create a new group of sub-accounts
[**corporateGroupUnlinkGroupIdSubAccountsPut**](MasterAccountApi.md#corporateGroupUnlinkGroupIdSubAccountsPut) | **PUT** /corporate/group/unlink/{groupId}/subAccounts | Delete sub-account from group
[**corporateMasterAccountGet**](MasterAccountApi.md#corporateMasterAccountGet) | **GET** /corporate/masterAccount | Get the details of requested master account
[**corporateSsoTokenPost**](MasterAccountApi.md#corporateSsoTokenPost) | **POST** /corporate/ssoToken | Generate SSO token to access admin account
[**corporateSubAccountGet**](MasterAccountApi.md#corporateSubAccountGet) | **GET** /corporate/subAccount | Get the list of all the sub-accounts of the master account.
[**corporateSubAccountIdApplicationsTogglePut**](MasterAccountApi.md#corporateSubAccountIdApplicationsTogglePut) | **PUT** /corporate/subAccount/{id}/applications/toggle | Enable/disable sub-account application(s)
[**corporateSubAccountIdDelete**](MasterAccountApi.md#corporateSubAccountIdDelete) | **DELETE** /corporate/subAccount/{id} | Delete a sub-account
[**corporateSubAccountIdGet**](MasterAccountApi.md#corporateSubAccountIdGet) | **GET** /corporate/subAccount/{id} | Get sub-account details
[**corporateSubAccountIdPlanPut**](MasterAccountApi.md#corporateSubAccountIdPlanPut) | **PUT** /corporate/subAccount/{id}/plan | Update sub-account plan
[**corporateSubAccountKeyPost**](MasterAccountApi.md#corporateSubAccountKeyPost) | **POST** /corporate/subAccount/key | Create an API key for a sub-account
[**corporateSubAccountPost**](MasterAccountApi.md#corporateSubAccountPost) | **POST** /corporate/subAccount | Create a new sub-account under a master account.
[**corporateSubAccountSsoTokenPost**](MasterAccountApi.md#corporateSubAccountSsoTokenPost) | **POST** /corporate/subAccount/ssoToken | Generate SSO token to access sub-account
[**corporateUserInvitationActionEmailPut**](MasterAccountApi.md#corporateUserInvitationActionEmailPut) | **PUT** /corporate/user/invitation/{action}/{email} | Resend / cancel admin user invitation
[**corporateUserRevokeEmailDelete**](MasterAccountApi.md#corporateUserRevokeEmailDelete) | **DELETE** /corporate/user/revoke/{email} | Revoke an admin user
[**getAccountActivity**](MasterAccountApi.md#getAccountActivity) | **GET** /organization/activities | Get user activity logs
[**getCorporateInvitedUsersList**](MasterAccountApi.md#getCorporateInvitedUsersList) | **GET** /corporate/invited/users | Get the list of all admin users
[**getCorporateUserPermission**](MasterAccountApi.md#getCorporateUserPermission) | **GET** /corporate/user/{email}/permissions | Check admin user permissions
[**getSubAccountGroups**](MasterAccountApi.md#getSubAccountGroups) | **GET** /corporate/groups | Get the list of groups
[**inviteAdminUser**](MasterAccountApi.md#inviteAdminUser) | **POST** /corporate/user/invitation/send | Send invitation to an admin user


<a name="corporateGroupIdDelete"></a>
# **corporateGroupIdDelete**
> corporateGroupIdDelete(id)

Delete a group

This endpoint allows you to delete a group of sub-organizations. When a group is deleted, the sub-organizations are no longer part of this group. The users associated with the group are no longer associated with the group once deleted.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String id = "id_example"; // String | Id of the group
try {
    apiInstance.corporateGroupIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateGroupIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Id of the group |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateGroupIdGet"></a>
# **corporateGroupIdGet**
> CorporateGroupDetailsResponse corporateGroupIdGet(id)

GET a group details

This endpoint allows you to retrieve a specific group’s information such as the list of sub-organizations and the user associated with the group.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String id = "id_example"; // String | Id of the group of sub-organization
try {
    CorporateGroupDetailsResponse result = apiInstance.corporateGroupIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateGroupIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Id of the group of sub-organization |

### Return type

[**CorporateGroupDetailsResponse**](CorporateGroupDetailsResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateGroupIdPut"></a>
# **corporateGroupIdPut**
> corporateGroupIdPut(id, body)

Update a group of sub-accounts

This endpoint allows you to update a group of sub-accounts

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String id = "id_example"; // String | Id of the group
Body1 body = new Body1(); // Body1 | Group details to be updated.
try {
    apiInstance.corporateGroupIdPut(id, body);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateGroupIdPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| Id of the group |
 **body** | [**Body1**](Body1.md)| Group details to be updated. |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateGroupPost"></a>
# **corporateGroupPost**
> InlineResponse201 corporateGroupPost(body)

Create a new group of sub-accounts

This endpoint allows to create a group of sub-accounts

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
Body body = new Body(); // Body | Group details to be created.
try {
    InlineResponse201 result = apiInstance.corporateGroupPost(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateGroupPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Body**](Body.md)| Group details to be created. |

### Return type

[**InlineResponse201**](InlineResponse201.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateGroupUnlinkGroupIdSubAccountsPut"></a>
# **corporateGroupUnlinkGroupIdSubAccountsPut**
> corporateGroupUnlinkGroupIdSubAccountsPut(groupId, body)

Delete sub-account from group

This endpoint allows you to remove a sub-organization from a group.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String groupId = "groupId_example"; // String | Id of the group
Body2 body = new Body2(); // Body2 | List of sub-account ids
try {
    apiInstance.corporateGroupUnlinkGroupIdSubAccountsPut(groupId, body);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateGroupUnlinkGroupIdSubAccountsPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupId** | **String**| Id of the group |
 **body** | [**Body2**](Body2.md)| List of sub-account ids |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateMasterAccountGet"></a>
# **corporateMasterAccountGet**
> MasterDetailsResponse corporateMasterAccountGet()

Get the details of requested master account

This endpoint will provide the details of the master account.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
try {
    MasterDetailsResponse result = apiInstance.corporateMasterAccountGet();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateMasterAccountGet");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MasterDetailsResponse**](MasterDetailsResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSsoTokenPost"></a>
# **corporateSsoTokenPost**
> GetSsoToken corporateSsoTokenPost(ssoTokenRequestCorporate)

Generate SSO token to access admin account

This endpoint generates an SSO token to authenticate and access the admin account using the endpoint https://account-app.brevo.com/account/login/corporate/sso/[token], where [token] will be replaced by the actual token.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
SsoTokenRequestCorporate ssoTokenRequestCorporate = new SsoTokenRequestCorporate(); // SsoTokenRequestCorporate | User email of admin account
try {
    GetSsoToken result = apiInstance.corporateSsoTokenPost(ssoTokenRequestCorporate);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSsoTokenPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ssoTokenRequestCorporate** | [**SsoTokenRequestCorporate**](SsoTokenRequestCorporate.md)| User email of admin account |

### Return type

[**GetSsoToken**](GetSsoToken.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountGet"></a>
# **corporateSubAccountGet**
> SubAccountsResponse corporateSubAccountGet(offset, limit)

Get the list of all the sub-accounts of the master account.

This endpoint will provide the list all the sub-accounts of the master account.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
Integer offset = 56; // Integer | Index of the first sub-account in the page
Integer limit = 56; // Integer | Number of sub-accounts to be displayed on each page
try {
    SubAccountsResponse result = apiInstance.corporateSubAccountGet(offset, limit);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **Integer**| Index of the first sub-account in the page |
 **limit** | **Integer**| Number of sub-accounts to be displayed on each page |

### Return type

[**SubAccountsResponse**](SubAccountsResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountIdApplicationsTogglePut"></a>
# **corporateSubAccountIdApplicationsTogglePut**
> corporateSubAccountIdApplicationsTogglePut(id, toggleApplications)

Enable/disable sub-account application(s)

API endpoint for the Corporate owner to enable/disable applications on the sub-account

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
Long id = 789L; // Long | Id of the sub-account organization (mandatory)
SubAccountAppsToggleRequest toggleApplications = new SubAccountAppsToggleRequest(); // SubAccountAppsToggleRequest | List of applications to activate or deactivate on a sub-account
try {
    apiInstance.corporateSubAccountIdApplicationsTogglePut(id, toggleApplications);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountIdApplicationsTogglePut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Long**| Id of the sub-account organization (mandatory) |
 **toggleApplications** | [**SubAccountAppsToggleRequest**](SubAccountAppsToggleRequest.md)| List of applications to activate or deactivate on a sub-account |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountIdDelete"></a>
# **corporateSubAccountIdDelete**
> corporateSubAccountIdDelete(id)

Delete a sub-account

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
Long id = 789L; // Long | Id of the sub-account organization to be deleted
try {
    apiInstance.corporateSubAccountIdDelete(id);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountIdDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Long**| Id of the sub-account organization to be deleted |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountIdGet"></a>
# **corporateSubAccountIdGet**
> SubAccountDetailsResponse corporateSubAccountIdGet(id)

Get sub-account details

This endpoint will provide the details for the specified sub-account company

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
Long id = 789L; // Long | Id of the sub-account organization
try {
    SubAccountDetailsResponse result = apiInstance.corporateSubAccountIdGet(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountIdGet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Long**| Id of the sub-account organization |

### Return type

[**SubAccountDetailsResponse**](SubAccountDetailsResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountIdPlanPut"></a>
# **corporateSubAccountIdPlanPut**
> corporateSubAccountIdPlanPut(id, updatePlanDetails)

Update sub-account plan

This endpoint will update the sub-account plan

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
Long id = 789L; // Long | Id of the sub-account organization
SubAccountUpdatePlanRequest updatePlanDetails = new SubAccountUpdatePlanRequest(); // SubAccountUpdatePlanRequest | Values to update a sub-account plan
try {
    apiInstance.corporateSubAccountIdPlanPut(id, updatePlanDetails);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountIdPlanPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Long**| Id of the sub-account organization |
 **updatePlanDetails** | [**SubAccountUpdatePlanRequest**](SubAccountUpdatePlanRequest.md)| Values to update a sub-account plan |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountKeyPost"></a>
# **corporateSubAccountKeyPost**
> CreateApiKeyResponse corporateSubAccountKeyPost(createApiKeyRequest)

Create an API key for a sub-account

This endpoint will generate an API v3 key for a sub account

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
CreateApiKeyRequest createApiKeyRequest = new CreateApiKeyRequest(); // CreateApiKeyRequest | Values to generate API key for sub-account
try {
    CreateApiKeyResponse result = apiInstance.corporateSubAccountKeyPost(createApiKeyRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountKeyPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createApiKeyRequest** | [**CreateApiKeyRequest**](CreateApiKeyRequest.md)| Values to generate API key for sub-account |

### Return type

[**CreateApiKeyResponse**](CreateApiKeyResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountPost"></a>
# **corporateSubAccountPost**
> CreateSubAccountResponse corporateSubAccountPost(subAccountCreate)

Create a new sub-account under a master account.

This endpoint will create a new sub-account under a master account

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
CreateSubAccount subAccountCreate = new CreateSubAccount(); // CreateSubAccount | values to create new sub-account
try {
    CreateSubAccountResponse result = apiInstance.corporateSubAccountPost(subAccountCreate);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subAccountCreate** | [**CreateSubAccount**](CreateSubAccount.md)| values to create new sub-account |

### Return type

[**CreateSubAccountResponse**](CreateSubAccountResponse.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateSubAccountSsoTokenPost"></a>
# **corporateSubAccountSsoTokenPost**
> GetSsoToken corporateSubAccountSsoTokenPost(ssoTokenRequest)

Generate SSO token to access sub-account

This endpoint generates an sso token to authenticate and access a sub-account of the master using the account endpoint https://account-app.brevo.com/account/login/sub-account/sso/[token], where [token] will be replaced by the actual token.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
SsoTokenRequest ssoTokenRequest = new SsoTokenRequest(); // SsoTokenRequest | Values to generate SSO token for sub-account
try {
    GetSsoToken result = apiInstance.corporateSubAccountSsoTokenPost(ssoTokenRequest);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateSubAccountSsoTokenPost");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ssoTokenRequest** | [**SsoTokenRequest**](SsoTokenRequest.md)| Values to generate SSO token for sub-account |

### Return type

[**GetSsoToken**](GetSsoToken.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateUserInvitationActionEmailPut"></a>
# **corporateUserInvitationActionEmailPut**
> InlineResponse200 corporateUserInvitationActionEmailPut(action, email)

Resend / cancel admin user invitation

This endpoint will allow the user to:  - Resend an admin user invitation - Cancel an admin user invitation 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String action = "action_example"; // String | Action to be performed (cancel / resend)
String email = "email_example"; // String | Email address of the recipient
try {
    InlineResponse200 result = apiInstance.corporateUserInvitationActionEmailPut(action, email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateUserInvitationActionEmailPut");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **action** | **String**| Action to be performed (cancel / resend) |
 **email** | **String**| Email address of the recipient |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="corporateUserRevokeEmailDelete"></a>
# **corporateUserRevokeEmailDelete**
> corporateUserRevokeEmailDelete(email)

Revoke an admin user

This endpoint allows to revoke/remove an invited member of your Admin account

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String email = "email_example"; // String | Email of the invited user
try {
    apiInstance.corporateUserRevokeEmailDelete(email);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#corporateUserRevokeEmailDelete");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| Email of the invited user |

### Return type

null (empty response body)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getAccountActivity"></a>
# **getAccountActivity**
> GetAccountActivity getAccountActivity(startDate, endDate, limit, offset)

Get user activity logs

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String startDate = "startDate_example"; // String | Mandatory if endDate is used. Enter start date in UTC date (YYYY-MM-DD) format to filter the activity in your account. Maximum time period that can be selected is one month. Additionally, you can retrieve activity logs from the past 12 months from the date of your search.
String endDate = "endDate_example"; // String | Mandatory if startDate is used. Enter end date in UTC date (YYYY-MM-DD) format to filter the activity in your account. Maximum time period that can be selected is one month.
Long limit = 10L; // Long | Number of documents per page
Long offset = 0L; // Long | Index of the first document in the page.
try {
    GetAccountActivity result = apiInstance.getAccountActivity(startDate, endDate, limit, offset);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#getAccountActivity");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **String**| Mandatory if endDate is used. Enter start date in UTC date (YYYY-MM-DD) format to filter the activity in your account. Maximum time period that can be selected is one month. Additionally, you can retrieve activity logs from the past 12 months from the date of your search. | [optional]
 **endDate** | **String**| Mandatory if startDate is used. Enter end date in UTC date (YYYY-MM-DD) format to filter the activity in your account. Maximum time period that can be selected is one month. | [optional]
 **limit** | **Long**| Number of documents per page | [optional] [default to 10]
 **offset** | **Long**| Index of the first document in the page. | [optional] [default to 0]

### Return type

[**GetAccountActivity**](GetAccountActivity.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCorporateInvitedUsersList"></a>
# **getCorporateInvitedUsersList**
> GetCorporateInvitedUsersList getCorporateInvitedUsersList()

Get the list of all admin users

This endpoint allows you to list all Admin users of your Admin account

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
try {
    GetCorporateInvitedUsersList result = apiInstance.getCorporateInvitedUsersList();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#getCorporateInvitedUsersList");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetCorporateInvitedUsersList**](GetCorporateInvitedUsersList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getCorporateUserPermission"></a>
# **getCorporateUserPermission**
> GetCorporateUserPermission getCorporateUserPermission(email)

Check admin user permissions

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
String email = "email_example"; // String | Email of the invited user
try {
    GetCorporateUserPermission result = apiInstance.getCorporateUserPermission(email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#getCorporateUserPermission");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| Email of the invited user |

### Return type

[**GetCorporateUserPermission**](GetCorporateUserPermission.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getSubAccountGroups"></a>
# **getSubAccountGroups**
> List&lt;InlineResponse2001&gt; getSubAccountGroups()

Get the list of groups

This endpoint allows you to list all groups created on your Admin account.

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
try {
    List<InlineResponse2001> result = apiInstance.getSubAccountGroups();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#getSubAccountGroups");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;InlineResponse2001&gt;**](InlineResponse2001.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="inviteAdminUser"></a>
# **inviteAdminUser**
> InviteAdminUser inviteAdminUser(sendInvitation)

Send invitation to an admin user

&#x60;This endpoint allows you to invite a member to manage the Admin account  Features and their respective permissions are as below:  - &#x60;my_plan&#x60;:   - &quot;all&quot; - &#x60;api&#x60;:   - &quot;none&quot; - &#x60;user_management&#x60;:   - &quot;all&quot; - &#x60;app_management&#x60; | Not available in ENTv2:   - &quot;all&quot;  **Note**: - If &#x60;all_features_access: false&#x60; then only privileges are required otherwise if &#x60;true&#x60; then it&#39;s assumed that all permissions will be there for the invited admin user. 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.MasterAccountApi;

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

MasterAccountApi apiInstance = new MasterAccountApi();
InviteAdminUser sendInvitation = new InviteAdminUser(); // InviteAdminUser | Payload to send an invitation
try {
    InviteAdminUser result = apiInstance.inviteAdminUser(sendInvitation);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling MasterAccountApi#inviteAdminUser");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendInvitation** | [**InviteAdminUser**](InviteAdminUser.md)| Payload to send an invitation |

### Return type

[**InviteAdminUser**](InviteAdminUser.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

