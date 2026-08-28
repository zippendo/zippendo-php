# BatchSendShipments200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shipment_id** | **string** | The shipment this result refers to. |
**status** | **string** | &#x60;sent&#x60; when the carrier booked it, &#x60;failed&#x60; when the carrier or Zippendo rejected it, and &#x60;skipped&#x60; when the batch ran out of time before reaching it. A &#x60;skipped&#x60; shipment was never sent to the carrier and is safe to submit again. |
**code** | **string** | Canonical machine-readable error code, present when &#x60;status&#x60; is &#x60;failed&#x60; or &#x60;skipped&#x60;. | [optional]
**message** | **string** | Human-readable detail, present when &#x60;status&#x60; is &#x60;failed&#x60; or &#x60;skipped&#x60;. | [optional]
**errors** | [**\Zippendo\Sdk\Model\SendShipment422ResponseErrorsInner[]**](SendShipment422ResponseErrorsInner.md) | Carrier-specific errors, present when the carrier rejected the booking. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
