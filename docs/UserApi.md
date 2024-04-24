# UserApi

All URIs are relative to *https://api.brevo.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**editUserPermission**](UserApi.md#editUserPermission) | **POST** /organization/user/update/permissions | Update permission for a user
[**getInvitedUsersList**](UserApi.md#getInvitedUsersList) | **GET** /organization/invited/users | Get the list of all your users
[**getUserPermission**](UserApi.md#getUserPermission) | **GET** /organization/user/{email}/permissions | Check user permission
[**inviteuser**](UserApi.md#inviteuser) | **POST** /organization/user/invitation/send | Send invitation to user
[**putRevokeUserPermission**](UserApi.md#putRevokeUserPermission) | **PUT** /organization/user/invitation/revoke/{email} | Revoke user permission
[**putresendcancelinvitation**](UserApi.md#putresendcancelinvitation) | **PUT** /organization/user/invitation/{action}/{email} | Resend / Cancel invitation


<a name="editUserPermission"></a>
# **editUserPermission**
> Inviteuser editUserPermission(updatePermissions)

Update permission for a user

&#x60;Feature&#x60; - A Feature represents a specific functionality like Email campaign, Deals, Calls, Automations, etc. on Brevo. While inviting a user, determine which feature you want to manage access to. You must specify the feature accurately to avoid errors.  &#x60;Permission&#x60; - A Permission defines the level of access or control a user has over a specific feature. While inviting user, decide on the permission level required for the selected feature. Make sure the chosen permission is related to the selected feature.  Features and their respective permissions are as below:  - &#x60;email_campaigns&#x60;:   - &quot;create_edit_delete&quot;   - &quot;send_schedule_suspend&quot; - &#x60;sms_campaigns&#x60;:   - &quot;create_edit_delete&quot;   - &quot;send_schedule_suspend&quot; - &#x60;contacts&#x60;:   - &quot;view&quot;   - &quot;create_edit_delete&quot;   - &quot;import&quot;   - &quot;export&quot;   - &quot;list_and_attributes&quot;   - &quot;forms&quot; - &#x60;templates&#x60;:   - &quot;create_edit_delete&quot;   - &quot;activate_deactivate&quot; - &#x60;workflows&#x60;:   - &quot;create_edit_delete&quot;   - &quot;activate_deactivate_pause&quot;   - &quot;settings&quot; - &#x60;facebook_ads&#x60;:   - &quot;create_edit_delete&quot;   - &quot;schedule_pause&quot; - &#x60;landing_pages&#x60;:   - &quot;all&quot; - &#x60;transactional_emails&#x60;:   - &quot;settings&quot;   - &quot;logs&quot; - &#x60;smtp_api&#x60;:   - &quot;smtp&quot;   - &quot;api_keys&quot;   - &quot;authorized_ips&quot; - &#x60;user_management&#x60;:   - &quot;all&quot; - &#x60;sales_platform&#x60;:   - &quot;manage_owned_deals_tasks_companies&quot;   - &quot;manage_others_deals_tasks_companies&quot;   - &quot;reports&quot;   - &quot;settings&quot; - &#x60;phone&#x60;:   - &quot;all&quot; - &#x60;conversations&#x60;:   - &quot;access&quot;   - &quot;assign&quot;   - &quot;configure&quot; - &#x60;senders_domains_dedicated_ips&#x60;:   - &quot;senders_management&quot;   - &quot;domains_management&quot;   - &quot;dedicated_ips_management&quot; - &#x60;push_notifications&#x60;:   - &quot;view&quot;   - &quot;create_edit_delete&quot;   - &quot;send&quot;   - &quot;settings&quot;  **Note**: - The privileges array remains the same as in the send invitation; the user simply needs to provide the permissions that need to be updated. - The availability of feature and its permission depends on your current plan. Please select the features and permissions accordingly. 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.UserApi;

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

UserApi apiInstance = new UserApi();
Inviteuser updatePermissions = new Inviteuser(); // Inviteuser | Values to update permissions for an invited user
try {
    Inviteuser result = apiInstance.editUserPermission(updatePermissions);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserApi#editUserPermission");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **updatePermissions** | [**Inviteuser**](Inviteuser.md)| Values to update permissions for an invited user |

### Return type

[**Inviteuser**](Inviteuser.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getInvitedUsersList"></a>
# **getInvitedUsersList**
> GetInvitedUsersList getInvitedUsersList()

Get the list of all your users

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.UserApi;

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

UserApi apiInstance = new UserApi();
try {
    GetInvitedUsersList result = apiInstance.getInvitedUsersList();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserApi#getInvitedUsersList");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetInvitedUsersList**](GetInvitedUsersList.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getUserPermission"></a>
# **getUserPermission**
> GetUserPermission getUserPermission(email)

Check user permission

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.UserApi;

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

UserApi apiInstance = new UserApi();
String email = "email_example"; // String | Email of the invited user.
try {
    GetUserPermission result = apiInstance.getUserPermission(email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserApi#getUserPermission");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| Email of the invited user. |

### Return type

[**GetUserPermission**](GetUserPermission.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="inviteuser"></a>
# **inviteuser**
> Inviteuser inviteuser(sendInvitation)

Send invitation to user

&#x60;Feature&#x60; - A Feature represents a specific functionality like Email campaign, Deals, Calls, Automations, etc. on Brevo. While inviting a user, determine which feature you want to manage access to. You must specify the feature accurately to avoid errors.  &#x60;Permission&#x60; - A Permission defines the level of access or control a user has over a specific feature. While inviting user, decide on the permission level required for the selected feature. Make sure the chosen permission is related to the selected feature.  Features and their respective permissions are as below:  - &#x60;email_campaigns&#x60;:   - &quot;create_edit_delete&quot;   - &quot;send_schedule_suspend&quot; - &#x60;sms_campaigns&#x60;:   - &quot;create_edit_delete&quot;   - &quot;send_schedule_suspend&quot; - &#x60;contacts&#x60;:   - &quot;view&quot;   - &quot;create_edit_delete&quot;   - &quot;import&quot;   - &quot;export&quot;   - &quot;list_and_attributes&quot;   - &quot;forms&quot; - &#x60;templates&#x60;:   - &quot;create_edit_delete&quot;   - &quot;activate_deactivate&quot; - &#x60;workflows&#x60;:   - &quot;create_edit_delete&quot;   - &quot;activate_deactivate_pause&quot;   - &quot;settings&quot; - &#x60;facebook_ads&#x60;:   - &quot;create_edit_delete&quot;   - &quot;schedule_pause&quot; - &#x60;landing_pages&#x60;:   - &quot;all&quot; - &#x60;transactional_emails&#x60;:   - &quot;settings&quot;   - &quot;logs&quot; - &#x60;smtp_api&#x60;:   - &quot;smtp&quot;   - &quot;api_keys&quot;   - &quot;authorized_ips&quot; - &#x60;user_management&#x60;:   - &quot;all&quot; - &#x60;sales_platform&#x60;:   - &quot;manage_owned_deals_tasks_companies&quot;   - &quot;manage_others_deals_tasks_companies&quot;   - &quot;reports&quot;   - &quot;settings&quot; - &#x60;phone&#x60;:   - &quot;all&quot; - &#x60;conversations&#x60;:   - &quot;access&quot;   - &quot;assign&quot;   - &quot;configure&quot; - &#x60;senders_domains_dedicated_ips&#x60;:   - &quot;senders_management&quot;   - &quot;domains_management&quot;   - &quot;dedicated_ips_management&quot; - &#x60;push_notifications&#x60;:   - &quot;view&quot;   - &quot;create_edit_delete&quot;   - &quot;send&quot;   - &quot;settings&quot;  **Note**: - If &#x60;all_features_access: false&#x60; then only privileges are required otherwise if &#x60;true&#x60; then it&#39;s assumed that all permissions will be there for the invited user. - The availability of feature and its permission depends on your current plan. Please select the features and permissions accordingly. 

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.UserApi;

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

UserApi apiInstance = new UserApi();
Inviteuser sendInvitation = new Inviteuser(); // Inviteuser | Values to create an invitation
try {
    Inviteuser result = apiInstance.inviteuser(sendInvitation);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserApi#inviteuser");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendInvitation** | [**Inviteuser**](Inviteuser.md)| Values to create an invitation |

### Return type

[**Inviteuser**](Inviteuser.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="putRevokeUserPermission"></a>
# **putRevokeUserPermission**
> PutRevokeUserPermission putRevokeUserPermission(email)

Revoke user permission

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.UserApi;

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

UserApi apiInstance = new UserApi();
String email = "email_example"; // String | Email of the invited user.
try {
    PutRevokeUserPermission result = apiInstance.putRevokeUserPermission(email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserApi#putRevokeUserPermission");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| Email of the invited user. |

### Return type

[**PutRevokeUserPermission**](PutRevokeUserPermission.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="putresendcancelinvitation"></a>
# **putresendcancelinvitation**
> Putresendcancelinvitation putresendcancelinvitation(action, email)

Resend / Cancel invitation

### Example
```java
// Import classes:
//import brevo.ApiClient;
//import brevo.ApiException;
//import brevo.Configuration;
//import brevo.auth.*;
//import brevoApi.UserApi;

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

UserApi apiInstance = new UserApi();
String action = "action_example"; // String | action
String email = "email_example"; // String | Email of the invited user.
try {
    Putresendcancelinvitation result = apiInstance.putresendcancelinvitation(action, email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling UserApi#putresendcancelinvitation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **action** | **String**| action | [enum: resend, cancel]
 **email** | **String**| Email of the invited user. |

### Return type

[**Putresendcancelinvitation**](Putresendcancelinvitation.md)

### Authorization

[api-key](../README.md#api-key), [partner-key](../README.md#partner-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

