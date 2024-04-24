
# CreateExternalFeed

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Name of the feed | 
**url** | **String** | URL of the feed | 
**authType** | [**AuthTypeEnum**](#AuthTypeEnum) | Auth type of the feed:   * &#x60;basic&#x60;   * &#x60;token&#x60;   * &#x60;noAuth&#x60;  |  [optional]
**username** | **String** | Username for authType &#x60;basic&#x60; |  [optional]
**password** | **String** | Password for authType &#x60;basic&#x60; |  [optional]
**token** | **String** | Token for authType &#x60;token&#x60; |  [optional]
**headers** | [**List&lt;GetExternalFeedByUUIDHeaders&gt;**](GetExternalFeedByUUIDHeaders.md) | Custom headers for the feed |  [optional]
**maxRetries** | **Integer** | Maximum number of retries on the feed url |  [optional]
**cache** | **Boolean** | Toggle caching of feed url response |  [optional]


<a name="AuthTypeEnum"></a>
## Enum: AuthTypeEnum
Name | Value
---- | -----
BASIC | &quot;basic&quot;
TOKEN | &quot;token&quot;
NOAUTH | &quot;noAuth&quot;



