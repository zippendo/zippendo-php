# ListShippingRules200ResponseDataInnerConditionsInnerOneOf1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Condition type discriminator |
**price_type** | **string** | Whether to compare against subtotal (before discounts) or total (after discounts) | [default to 'total']
**operator** | **string** | Comparison operator |
**value** | **float** | Price value to compare against |
**shipping_price** | **float** | Shipping price when condition matches |
**currency** | **string** | ISO 4217 currency code |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
