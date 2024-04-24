
# UpdateCouponCollection

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**defaultCoupon** | **String** | A default coupon to be used in case there are no coupons left |  [optional]
**expirationDate** | [**OffsetDateTime**] | Specify an expiration date for the coupon collection in RFC3339 format. Use null to remove the expiration date. |  [optional]
**remainingDaysAlert** | **Integer** | Send a notification alert (email) when the remaining days until the expiration date are equal or fall bellow this number. Use null to disable alerts. |  [optional]
**remainingCouponsAlert** | **Integer** | Send a notification alert (email) when the remaining coupons count is equal or fall bellow this number. Use null to disable alerts. |  [optional]



