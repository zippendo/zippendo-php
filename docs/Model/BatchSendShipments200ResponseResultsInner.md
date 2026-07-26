# BatchSendShipments200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shipment_id** | **string** | The shipment this result refers to. |
**status** | **string** | Whether this shipment was successfully booked with its carrier. |
**code** | **string** | Canonical machine-readable error code, present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional]
**message** | **string** | Human-readable failure detail, present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional]
**errors** | [**\Zippendo\Sdk\Model\SendShipment422ResponseErrorsInner[]**](SendShipment422ResponseErrorsInner.md) | Carrier-specific errors, present when the carrier rejected the booking. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
