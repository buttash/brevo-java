
# GetWebhook

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** | URL of the webhook | 
**id** | **Long** | ID of the webhook | 
**description** | **String** | Description of the webhook | 
**events** | **List&lt;String&gt;** |  | 
**type** | [**TypeEnum**](#TypeEnum) | Type of webhook (marketing or transactional) | 
**createdAt** | **String** | Creation UTC date-time of the webhook (YYYY-MM-DDTHH:mm:ss.SSSZ) | 
**modifiedAt** | **String** | Last modification UTC date-time of the webhook (YYYY-MM-DDTHH:mm:ss.SSSZ) | 
**batched** | **Boolean** | To send batched webhooks |  [optional]
**auth** | [**GetWebhookAuth**](GetWebhookAuth.md) |  |  [optional]
**headers** | [**List&lt;GetWebhookHeaders&gt;**](GetWebhookHeaders.md) | Custom headers to be send with webhooks |  [optional]


<a name="TypeEnum"></a>
## Enum: TypeEnum
Name | Value
---- | -----
MARKETING | &quot;marketing&quot;
TRANSACTIONAL | &quot;transactional&quot;



