# ListOrders200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique order ID. |
**order_number** | **string** | Human-readable order number. |
**customer_name** | **string** | Customer full name. | [optional]
**customer_email** | **string** | Customer email address. | [optional]
**status** | **string** | Order fulfilment status derived from its shipments. |
**brand_id** | **string** | Brand this record belongs to, or null when it is organization-wide |
**subtotal_amount** | **float** | Order subtotal before shipping and tax. | [optional]
**total_amount** | **float** | Order grand total. | [optional]
**currency** | **string** | ISO 4217 currency code. | [optional]
**shipment_count** | **int** | Number of shipments created for the order. |
**order_channel** | [**\Zippendo\Sdk\Model\ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  |
**created_at** | **string** | Creation timestamp (ISO 8601). |
**updated_at** | **string** | Last update timestamp (ISO 8601). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
