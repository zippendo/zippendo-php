# GetOrder200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique order ID. |
**order_number** | **string** | Human-readable order number. |
**external_id** | **string** | Identifier of the order in the source platform. | [optional]
**customer_name** | **string** | Customer full name. | [optional]
**customer_email** | **string** | Customer email address. | [optional]
**shipping_address** | [**\Zippendo\Sdk\Model\CreateOrder201ResponseShippingAddress**](CreateOrder201ResponseShippingAddress.md) |  | [optional]
**order_lines** | [**\Zippendo\Sdk\Model\CreateOrder201ResponseOrderLinesInner[]**](CreateOrder201ResponseOrderLinesInner.md) | Line items in the order. |
**subtotal_amount** | **float** | Order subtotal before shipping and tax. | [optional]
**total_amount** | **float** | Order grand total. | [optional]
**currency** | **string** | ISO 4217 currency code. | [optional]
**status** | **string** | Order fulfilment status derived from its shipments. |
**shipping_rule_id** | **string** | ID of the applied shipping rule. | [optional]
**notes** | **string** | Free-form internal notes. | [optional]
**external_data** | **array<string,mixed>** | Raw platform-specific payload for reference. | [optional]
**order_channel_id** | **string** | ID of the order channel this order belongs to. |
**org_id** | **string** | Owning organization ID. |
**created_at** | **string** | Creation timestamp (ISO 8601). |
**updated_at** | **string** | Last update timestamp (ISO 8601). |
**order_channel** | [**\Zippendo\Sdk\Model\ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  |
**shipping_rule** | [**\Zippendo\Sdk\Model\GetOrder200ResponseShippingRule**](GetOrder200ResponseShippingRule.md) |  | [optional]
**shipments** | [**\Zippendo\Sdk\Model\GetOrder200ResponseShipmentsInner[]**](GetOrder200ResponseShipmentsInner.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
