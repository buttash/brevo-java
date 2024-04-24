
# ExportWebhooksHistory

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**days** | **Integer** | Number of days in the past including today (positive integer). _Not compatible with &#39;startDate&#39; and &#39;endDate&#39;_ |  [optional]
**startDate** | **String** | Mandatory if endDate is used. Starting date of the history (YYYY-MM-DD). Must be lower than equal to endDate |  [optional]
**endDate** | **String** | Mandatory if startDate is used. Ending date of the report (YYYY-MM-DD). Must be greater than equal to startDate |  [optional]
**sort** | **String** | Sorting order of records (asc or desc) |  [optional]
**type** | [**TypeEnum**](#TypeEnum) | Filter the history based on webhook type | 
**event** | [**EventEnum**](#EventEnum) | Filter the history for a specific event type | 
**notifyURL** | **String** | Webhook URL to receive CSV file link | 
**webhookId** | **Integer** | Filter the history for a specific webhook id |  [optional]
**email** | **String** | Filter the history for a specific email |  [optional]
**messageId** | **Integer** | Filter the history for a specific message id. Applicable only for transactional webhooks. |  [optional]


<a name="TypeEnum"></a>
## Enum: TypeEnum
Name | Value
---- | -----
TRANSACTIONAL | &quot;transactional&quot;
MARKETING | &quot;marketing&quot;


<a name="EventEnum"></a>
## Enum: EventEnum
Name | Value
---- | -----
INVALID_PARAMETER | &quot;invalid_parameter&quot;
MISSING_PARAMETER | &quot;missing_parameter&quot;
HARDBOUNCE | &quot;hardBounce&quot;
SOFTBOUNCE | &quot;softBounce&quot;
DELIVERED | &quot;delivered&quot;
SPAM | &quot;spam&quot;
REQUEST | &quot;request&quot;
OPENED | &quot;opened&quot;
CLICK | &quot;click&quot;
INVALID | &quot;invalid&quot;
DEFERRED | &quot;deferred&quot;
BLOCKED | &quot;blocked&quot;
UNSUBSCRIBED | &quot;unsubscribed&quot;
ERROR | &quot;error&quot;
UNIQUEOPENED | &quot;uniqueOpened&quot;
LOADEDBYPROXY | &quot;loadedByProxy&quot;
ALLEVENTS | &quot;allEvents&quot;



