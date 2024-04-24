
# GetPaymentRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reference** | **String** | Reference of the payment request, it will appear on the payment page.  | 
**status** | [**StatusEnum**](#StatusEnum) | Status of the payment request. | 
**_configuration** | [**ModelConfiguration**](ModelConfiguration.md) |  |  [optional]
**contactId** | **Long** | Brevo ID of the contact requested to pay.  |  [optional]
**cart** | [**Cart**](Cart.md) |  | 
**notification** | [**Notification**](Notification.md) |  | 


<a name="StatusEnum"></a>
## Enum: StatusEnum
Name | Value
---- | -----
CREATED | &quot;created&quot;
SENT | &quot;sent&quot;
REMINDERSENT_PAID | &quot;reminderSent - paid&quot;



