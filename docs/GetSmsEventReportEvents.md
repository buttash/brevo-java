
# GetSmsEventReportEvents

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phoneNumber** | **String** | Phone number which has generated the event |  [optional]
**date** | **String** | UTC date-time on which the event has been generated |  [optional]
**messageId** | **String** | Message ID which generated the event |  [optional]
**event** | [**EventEnum**](#EventEnum) | Event which occurred |  [optional]
**reason** | **String** | Reason of bounce (only available if the event is hardbounce or softbounce) |  [optional]
**reply** | **String** |  |  [optional]
**tag** | **String** | Tag of the SMS which generated the event |  [optional]


<a name="EventEnum"></a>
## Enum: EventEnum
Name | Value
---- | -----
BOUNCES | &quot;bounces&quot;
HARDBOUNCES | &quot;hardBounces&quot;
SOFTBOUNCES | &quot;softBounces&quot;
DELIVERED | &quot;delivered&quot;
SENT | &quot;sent&quot;
ACCEPTED | &quot;accepted&quot;
UNSUBSCRIPTION | &quot;unsubscription&quot;
REPLIES | &quot;replies&quot;
BLOCKED | &quot;blocked&quot;
REJECTED | &quot;rejected&quot;



