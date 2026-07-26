# UpdateShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reference** | **string** | Customer-facing shipment reference. | [optional]
**address_id** | **string** | Sender address identifier. | [optional]
**service_point_id** | **string** | Selected carrier service point identifier. | [optional]
**parties** | [**\Zippendo\Sdk\Model\CreateShipmentRequestPartiesInner[]**](CreateShipmentRequestPartiesInner.md) | Parties involved in the shipment. Optional when orderId is provided. | [optional]
**type** | **string** | Direction of the shipment relative to the organization. | [optional]
**carrier_settings** | [**\Zippendo\Sdk\Model\CreateShipmentRequestCarrierSettings**](CreateShipmentRequestCarrierSettings.md) |  | [optional]
**parcels** | [**\Zippendo\Sdk\Model\CreateShipmentRequestParcelsInner[]**](CreateShipmentRequestParcelsInner.md) | Parcels to include. Optional when orderId is provided. | [optional]
**pickup_details** | [**\Zippendo\Sdk\Model\CreateShipmentRequestPickupDetails**](CreateShipmentRequestPickupDetails.md) |  | [optional]
**term_of_trade** | **string** | Incoterm governing the shipment. | [optional] [default to 'DAP']
**status** | **string** | Lifecycle status of the shipment. | [optional] [default to 'pending']
**order_id** | **string** | Order to derive parties and parcels from. | [optional]
**label_printer_id** | **string** | Printer to assign for labels. | [optional]
**document_printer_id** | **string** | Printer to assign for documents. | [optional]
**shipping_rule_id** | **string** | Shipping rule to apply to the shipment. Pass null to clear. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
