
# GetCouponCollection

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The id of the collection. | 
**name** | **String** | The name of the collection. | 
**defaultCoupon** | **String** | The default coupon of the collection. | 
**createdAt** | [**OffsetDateTime**] | Datetime on which the collection was created. | 
**totalCoupons** | **Long** | Total number of coupons in the collection. | 
**remainingCoupons** | **Long** | Number of coupons that have not been sent yet. | 
**expirationDate** | [**OffsetDateTime**] | Expiration date for the coupon collection in RFC3339 format. |  [optional]
**remainingDaysAlert** | **Integer** | If present, an email notification is going to be sent the defined amount of days before the expiration date. |  [optional]
**remainingCouponsAlert** | **Integer** | If present, an email notification is going to be sent when the total number of available coupons falls below the defined threshold. |  [optional]



