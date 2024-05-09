
# GetExtendedContactDetails

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **String** | Email address of the contact for which you requested the details |  [optional]
**id** | **Long** | ID of the contact for which you requested the details | 
**emailBlacklisted** | **Boolean** | Blacklist status for email campaigns (true&#x3D;blacklisted, false&#x3D;not blacklisted) | 
**smsBlacklisted** | **Boolean** | Blacklist status for SMS campaigns (true&#x3D;blacklisted, false&#x3D;not blacklisted) | 
**createdAt** | **String** | Creation UTC date-time of the contact (YYYY-MM-DDTHH:mm:ss.SSSZ) | 
**modifiedAt** | **String** | Last modification UTC date-time of the contact (YYYY-MM-DDTHH:mm:ss.SSSZ) | 
**listIds** | **List&lt;Long&gt;** |  | 
**listUnsubscribed** | **List&lt;Long&gt;** |  |  [optional]
**attributes** | **Object** | Set of attributes of the contact | 
**statistics** | [**GetExtendedContactDetailsStatistics**](GetExtendedContactDetailsStatistics.md) |  | 



