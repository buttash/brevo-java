
# InviteuserPrivileges

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**feature** | [**FeatureEnum**](#FeatureEnum) | Feature name |  [optional]
**permissions** | [**List&lt;PermissionsEnum&gt;**](#List&lt;PermissionsEnum&gt;) | Permissions for a given feature |  [optional]


<a name="FeatureEnum"></a>
## Enum: FeatureEnum
Name | Value
---- | -----
EMAIL_CAMPAIGNS | &quot;email_campaigns&quot;
SMS_CAMPAIGNS | &quot;sms_campaigns&quot;
CONTACTS | &quot;contacts&quot;
TEMPLATES | &quot;templates&quot;
WORKFLOWS | &quot;workflows&quot;
FACEBOOK_ADS | &quot;facebook_ads&quot;
LANDING_PAGES | &quot;landing_pages&quot;
TRANSACTIONAL_EMAILS | &quot;transactional_emails&quot;
SMTP_API | &quot;smtp_api&quot;
USER_MANAGEMENT | &quot;user_management&quot;
SALES_PLATFORM | &quot;sales_platform&quot;
PHONE | &quot;phone&quot;
CONVERSATIONS | &quot;conversations&quot;
SENDERS_DOMAINS_DEDICATED_IPS | &quot;senders_domains_dedicated_ips&quot;
PUSH_NOTIFICATIONS | &quot;push_notifications&quot;


<a name="List<PermissionsEnum>"></a>
## Enum: List&lt;PermissionsEnum&gt;
Name | Value
---- | -----
CREATE_EDIT_DELETE | &quot;create_edit_delete&quot;
SEND_SCHEDULE_SUSPEND | &quot;send_schedule_suspend&quot;
VIEW | &quot;view&quot;
IMPORT | &quot;import&quot;
EXPORT | &quot;export&quot;
LIST_AND_ATTRIBUTES | &quot;list_and_attributes&quot;
FORMS | &quot;forms&quot;
ACTIVATE_DEACTIVATE | &quot;activate_deactivate&quot;
ACTIVATE_DEACTIVATE_PAUSE | &quot;activate_deactivate_pause&quot;
SETTINGS | &quot;settings&quot;
SCHEDULE_PAUSE | &quot;schedule_pause&quot;
ALL | &quot;all&quot;
LOGS | &quot;logs&quot;
ACCESS | &quot;access&quot;
ASSIGN | &quot;assign&quot;
CONFIGURE | &quot;configure&quot;
MANAGE_OWNED_DEALS_TASKS_COMPANIES | &quot;manage_owned_deals_tasks_companies&quot;
MANAGE_OTHERS_DEALS_TASKS_COMPANIES | &quot;manage_others_deals_tasks_companies&quot;
REPORTS | &quot;reports&quot;
SENDERS_MANAGEMENT | &quot;senders_management&quot;
DOMAINS_MANAGEMENT | &quot;domains_management&quot;
DEDICATED_IPS_MANAGEMENT | &quot;dedicated_ips_management&quot;
SEND | &quot;send&quot;
SMTP | &quot;smtp&quot;
API_KEYS | &quot;api_keys&quot;
AUTHORIZED_IPS | &quot;authorized_ips&quot;
NONE | &quot;none&quot;



