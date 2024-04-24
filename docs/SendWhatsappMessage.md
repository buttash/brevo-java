
# SendWhatsappMessage

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**templateId** | **Integer** | ID of the template to send |  [optional]
**text** | **String** | Text to be sent as message body (will be overridden if templateId is passed in the same request) |  [optional]
**senderNumber** | **String** | WhatsApp Number with country code. Example, 85264318721 | 
**params** | **Object** | Pass the set of attributes to customize the template. For example, {&quot;FNAME&quot;:&quot;Joe&quot;, &quot;LNAME&quot;:&quot;Doe&quot;}. |  [optional]
**contactNumbers** | **List&lt;String&gt;** | List of phone numbers of the contacts | 



