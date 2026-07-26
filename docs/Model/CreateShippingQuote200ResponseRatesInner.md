# CreateShippingQuote200ResponseRatesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service_name** | **string** | Display name of the shipping option |
**service_code** | **string** | Unique identifier for this shipping option |
**total_price** | **string** | Total shipping price in cents as string |
**currency** | **string** | ISO 4217 currency code |
**description** | **string** | Optional description | [optional]
**min_delivery_date** | **string** | Minimum delivery date (ISO 8601) | [optional]
**max_delivery_date** | **string** | Maximum delivery date (ISO 8601) | [optional]
**carrier_name** | **string** | Carrier display name | [optional]
**carrier_slug** | **string** | Carrier slug identifier | [optional]
**product_id** | **string** | Carrier product ID | [optional]
**shipping_rule_id** | **string** | Shipping rule ID that generated this rate |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
