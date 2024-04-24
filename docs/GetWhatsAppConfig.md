
# GetWhatsAppConfig

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**whatsappBusinessAccountId** | **String** | Id of the WhatsApp business account |  [optional]
**sendingLimit** | **String** | Sending limit Information of the WhatsApp API account |  [optional]
**phoneNumberQuality** | [**PhoneNumberQualityEnum**](#PhoneNumberQualityEnum) | Quality status of phone number associated with WhatsApp account. There are three quality ratings. example - **High (GREEN) , Medium (YELLOW) and Low(RED)** |  [optional]
**whatsappBusinessAccountStatus** | **String** | Status information related to WhatsApp Api account |  [optional]
**businessStatus** | **String** | Verification status information of the Business account |  [optional]
**phoneNumberNameStatus** | [**PhoneNumberNameStatusEnum**](#PhoneNumberNameStatusEnum) | Status of the name associated with WhatsApp Phone number |  [optional]


<a name="PhoneNumberQualityEnum"></a>
## Enum: PhoneNumberQualityEnum
Name | Value
---- | -----
GREEN | &quot;GREEN&quot;
YELLOW | &quot;YELLOW&quot;
RED | &quot;RED&quot;


<a name="PhoneNumberNameStatusEnum"></a>
## Enum: PhoneNumberNameStatusEnum
Name | Value
---- | -----
APPROVED | &quot;APPROVED&quot;
PENDING | &quot;PENDING&quot;
REJECTED | &quot;REJECTED&quot;



