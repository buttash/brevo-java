
# GetWhatsappEventReportEvents

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contactNumber** | **String** | WhatsApp Number with country code. Example, 85264318721 | 
**date** | **String** | UTC date-time on which the event has been generated | 
**messageId** | **String** | Message ID which generated the event | 
**event** | [**EventEnum**](#EventEnum) | Event which occurred | 
**reason** | **String** | Reason for the event (will be there in case of &#x60;error&#x60; and &#x60;soft-bounce&#x60; events) |  [optional]
**body** | **String** | Text of the reply (will be there only in case of &#x60;reply&#x60; event with text) |  [optional]
**mediaUrl** | **String** | Url of the media reply (will be there only in case of &#x60;reply&#x60; event with media) |  [optional]
**senderNumber** | **String** | WhatsApp Number with country code. Example, 85264318721 | 


<a name="EventEnum"></a>
## Enum: EventEnum
Name | Value
---- | -----
SENT | &quot;sent&quot;
DELIVERED | &quot;delivered&quot;
READ | &quot;read&quot;
ERROR | &quot;error&quot;
UNSUBSCRIBE | &quot;unsubscribe&quot;
REPLY | &quot;reply&quot;
SOFT_BOUNCE | &quot;soft-bounce&quot;



