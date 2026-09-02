# CreateOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_number** | **string** | Human-readable order number. |
**external_id** | **string** | Identifier of the order in the source platform. | [optional]
**order_channel_id** | **string** | ID of the order channel this order belongs to. |
**customer_name** | **string** | Customer full name. | [optional]
**customer_email** | **string** | Customer email address. | [optional]
**shipping_address** | [**\Zippendo\Sdk\Model\CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  | [optional]
**order_lines** | [**\Zippendo\Sdk\Model\CreateOrderRequestOrderLinesInner[]**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. |
**subtotal_amount** | **float** | Order subtotal before shipping and tax. | [optional]
**total_amount** | **float** | Order grand total. | [optional]
**currency** | **string** | ISO 4217 currency code. | [optional]
**notes** | **string** | Free-form internal notes. | [optional]
**shipping_rule_id** | **string** | Shipping rule to ship this order with. When set, a shipment is created immediately (and dispatched if the channel has autoShipOnCreate enabled). | [optional]
**shipping_method_title** | **string** | Shipping-method title from the source checkout; matched against the order channel&#39;s shipping-method mappings to pick a shipping rule. | [optional]
**external_data** | **array<string,mixed>** | Raw platform-specific payload for reference. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
