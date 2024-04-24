
# UpdateWhatsAppCampaign

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**campaignName** | **String** | Name of the campaign |  [optional]
**campaignStatus** | [**CampaignStatusEnum**](#CampaignStatusEnum) | Status of the campaign |  [optional]
**rescheduleFor** | **String** | Reschedule the sending UTC date-time (YYYY-MM-DDTHH:mm:ss.SSSZ) of campaign. **Prefer to pass your timezone in date-time format for accurate result.For example: **2017-06-01T12:30:00+02:00** Use this field to update the scheduledAt of any existing draft or scheduled WhatsApp campaign.  |  [optional]
**recipients** | [**CreateWhatsAppCampaignRecipients**](CreateWhatsAppCampaignRecipients.md) |  |  [optional]


<a name="CampaignStatusEnum"></a>
## Enum: CampaignStatusEnum
Name | Value
---- | -----
SCHEDULED | &quot;scheduled&quot;
SUSPENDED | &quot;suspended&quot;



