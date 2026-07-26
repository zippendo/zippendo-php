# CreateShippingRuleRequestConditionsInnerOneOf2

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Condition type discriminator |
**price_type** | **string** | Whether to compare against subtotal (before discounts) or total (after discounts) | [optional] [default to 'total']
**min** | **float** | Minimum cart value (inclusive) |
**max** | **float** | Maximum cart value (inclusive) |
**shipping_price** | **float** | Shipping price when condition matches |
**currency** | **string** | ISO 4217 currency code |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
