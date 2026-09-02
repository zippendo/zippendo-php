# CreateOrderChannelRequestSettingsShippingMethodMappingsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**match** | **string** | Shipping-method title to match against imported orders (trimmed, case-insensitive, exact). |
**shipping_rule_id** | **string** | Shipping rule applied to orders whose shipping-method title matches. |
**service_point_selection** | **string** | For rules whose product delivers to a service point: &#39;nearest&#39; auto-selects the closest point to the recipient address; &#39;manual&#39; keeps the shipment in draft for manual selection. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
