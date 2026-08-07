# ListShipments200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique shipment identifier. |
**reference** | **string** | Customer-facing shipment reference. |
**type** | **string** | Direction of the shipment relative to the organization. |
**carrier_settings** | [**\Zippendo\Sdk\Model\ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |
**status** | **string** | Lifecycle status of the shipment. |
**brand_id** | **string** | Brand this record belongs to, or null when it is organization-wide |
**address** | [**\Zippendo\Sdk\Model\ListShipments200ResponseDataInnerAddress**](ListShipments200ResponseDataInnerAddress.md) |  | [optional]
**created_at** | **string** | Timestamp when the shipment was created. |
**updated_at** | **string** | Timestamp when the shipment was last updated. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
