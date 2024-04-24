
# GetAllExternalFeedsFeeds

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | ID of the feed | 
**name** | **String** | Name of the feed | 
**url** | **String** | URL of the feed | 
**authType** | [**AuthTypeEnum**](#AuthTypeEnum) | Auth type of the feed: * &#x60;basic&#x60; * &#x60;token&#x60; * &#x60;noAuth&#x60;  | 
**username** | **String** | Username for authType &#x60;basic&#x60; |  [optional]
**password** | **String** | Password for authType &#x60;basic&#x60; |  [optional]
**token** | **String** | Token for authType &#x60;token&#x60; |  [optional]
**headers** | [**List&lt;GetExternalFeedByUUIDHeaders&gt;**](GetExternalFeedByUUIDHeaders.md) | Custom headers for the feed | 
**maxRetries** | **Integer** | Maximum number of retries on the feed url | 
**cache** | **Boolean** | Toggle caching of feed url response | 
**createdAt** | [**OffsetDateTime**] | Datetime on which the feed was created | 
**modifiedAt** | [**OffsetDateTime**] | Datetime on which the feed was modified | 


<a name="AuthTypeEnum"></a>
## Enum: AuthTypeEnum
Name | Value
---- | -----
BASIC | &quot;basic&quot;
TOKEN | &quot;token&quot;
NOAUTH | &quot;noAuth&quot;



