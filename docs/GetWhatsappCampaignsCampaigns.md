
# GetWhatsappCampaignsCampaigns

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **Long** | ID of the WhatsApp Campaign | 
**campaignName** | **String** | Name of the WhatsApp Campaign | 
**templateId** | **String** | Id of the WhatsApp template | 
**campaignStatus** | [**CampaignStatusEnum**](#CampaignStatusEnum) | Status of the WhatsApp Campaign | 
**scheduledAt** | **String** | UTC date-time on which WhatsApp campaign is scheduled. Should be in YYYY-MM-DDTHH:mm:ss.SSSZ format | 
**errorReason** | **String** | Error reason in the campaign creation |  [optional]
**invalidatedContacts** | **Long** | Count of invalidated contacts |  [optional]
**readPercentage** | **Float** | Read percentage of the the WhatsApp campaign created |  [optional]
**stats** | [**WhatsappCampStats**](WhatsappCampStats.md) |  |  [optional]
**createdAt** | **String** | Creation UTC date-time of the WhatsApp campaign (YYYY-MM-DDTHH:mm:ss.SSSZ) | 
**modifiedAt** | **String** | UTC date-time of last modification of the whatsapp template (YYYY-MM-DDTHH:mm:ss.SSSZ) | 


<a name="CampaignStatusEnum"></a>
## Enum: CampaignStatusEnum
Name | Value
---- | -----
DRAFT | &quot;draft&quot;
SCHEDULED | &quot;scheduled&quot;
PENDING | &quot;pending&quot;
APPROVED | &quot;approved&quot;
RUNNING | &quot;running&quot;
SUSPENDED | &quot;suspended&quot;
REJECTED | &quot;rejected&quot;
SENT | &quot;sent&quot;



