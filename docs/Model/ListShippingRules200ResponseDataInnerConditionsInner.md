# ListShippingRules200ResponseDataInnerConditionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Condition type discriminator |
**min** | **float** | Minimum cart value (inclusive) |
**max** | **float** | Maximum cart value (inclusive) |
**shipping_price** | **float** | Flat shipping price |
**currency** | **string** | ISO 4217 currency code |
**price_type** | **string** | Whether to compare against subtotal (before discounts) or total (after discounts) | [default to 'total']
**operator** | **string** | Comparison operator |
**value** | **int** | Quantity value to compare against |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
