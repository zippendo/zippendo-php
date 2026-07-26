# GetOrder200ResponseShipmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique shipment identifier. |
**reference** | **string** | Customer-facing shipment reference. |
**status** | **string** | Lifecycle status of the shipment. |
**type** | **string** | Direction of the shipment relative to the organization. |
**tracking** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  | [optional]
**carrier_settings** | [**\Zippendo\Sdk\Model\ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |
**created_at** | **string** | Timestamp when the shipment was created. |
**updated_at** | **string** | Timestamp when the shipment was last updated. |
**shipping_rule_id** | **string** | ID of the shipping rule used for this shipment. | [optional]
**documents** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseDocumentsInner[]**](CreateShipment201ResponseDocumentsInner.md) | Documents (labels, customs forms) for this shipment. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
