# BatchSplitShipmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parcel_id** | **string** | Parcel whose order lines are split across new shipments. |
**shipments** | [**\Zippendo\Sdk\Model\BatchSplitShipmentRequestShipmentsInner[]**](BatchSplitShipmentRequestShipmentsInner.md) | New shipments to create from the split parcel. |
**carrier_id** | **string** | Carrier for all new shipments. Copied from the original if omitted. | [optional]
**product_id** | **string** | Carrier product for all new shipments. Copied from the original if omitted. | [optional]
**services** | **string[]** | Service codes for all new shipments. Copied from the original if omitted. | [optional]
**additional_parameters** | [**array<string,\Zippendo\Sdk\Model\CreateShippingRuleRequestAdditionalParametersValue>**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific parameters for all new shipments. Copied from the original if omitted. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
