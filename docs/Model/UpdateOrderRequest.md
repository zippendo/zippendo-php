# UpdateOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_number** | **string** | Human-readable order number. | [optional]
**customer_name** | **string** | Customer full name. | [optional]
**customer_email** | **string** | Customer email address. | [optional]
**shipping_address** | [**\Zippendo\Sdk\Model\CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  | [optional]
**order_lines** | [**\Zippendo\Sdk\Model\CreateOrderRequestOrderLinesInner[]**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. | [optional]
**subtotal_amount** | **float** | Order subtotal before shipping and tax. | [optional]
**total_amount** | **float** | Order grand total. | [optional]
**currency** | **string** | ISO 4217 currency code. | [optional]
**notes** | **string** | Free-form internal notes. | [optional]
**status** | **string** | Order fulfilment status derived from its shipments. | [optional]
**shipping_rule_id** | **string** | ID of the shipping rule to apply. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
