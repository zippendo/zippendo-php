# SplitShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parcel_id** | **string** | Parcel whose order lines are split into a new shipment. |
**order_line_ids** | **string[]** | Order line IDs to move. If omitted, all order lines in the parcel are moved. | [optional]
**carrier_id** | **string** | Carrier for the new shipment. Copied from the original if omitted. | [optional]
**product_id** | **string** | Carrier product for the new shipment. Copied from the original if omitted. | [optional]
**services** | **string[]** | Service codes for the new shipment. Copied from the original if omitted. | [optional]
**additional_parameters** | **array<string,mixed>** | Carrier-specific parameters for the new shipment. | [optional]
**reference** | **string** | Reference for the new shipment. Defaults to the original reference with a suffix. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
