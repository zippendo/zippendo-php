# ListCarrierProducts200ResponseInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Display name of the carrier product |
**product_id** | **string** | Unique carrier product identifier |
**type** | **string** | Direction of the shipment for this product |
**description** | **string** | Description of the carrier product | [optional]
**available_countries** | **string[]** | Receiver countries this product delivers to |
**available_sender_countries** | **string[]** | Sender countries supported by this product |
**is_service_point** | **bool** | Whether this product delivers to a service point | [default to false]
**is_pickup_available** | **bool** | Whether carrier pickup is available for this product | [default to false]
**services** | [**\Zippendo\Sdk\Model\ListCarrierProducts200ResponseInnerServicesInner[]**](ListCarrierProducts200ResponseInnerServicesInner.md) | Additional services available for this product | [optional]
**additional_parameters** | [**\Zippendo\Sdk\Model\ListCarrierProducts200ResponseInnerAdditionalParametersInner[]**](ListCarrierProducts200ResponseInnerAdditionalParametersInner.md) | Extra parameters that can or must be supplied for this product | [optional]
**weight_limits** | [**\Zippendo\Sdk\Model\ListCarrierProducts200ResponseInnerWeightLimits**](ListCarrierProducts200ResponseInnerWeightLimits.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
