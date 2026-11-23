# ListCarrierProducts200ResponseInnerDangerousGoodsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **string** | &#x60;limited_quantity&#x60;: dangerous goods packed in limited quantities (LQ). &#x60;regulated&#x60;: fully regulated dangerous goods (ADR). |
**service_id** | **string** | The service that declares these dangerous goods to the carrier. |
**parameters** | [**\Zippendo\Sdk\Model\ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters**](ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters.md) |  |
**owned_parameters** | **string[]** | Every additional parameter that describes the declared goods, including those &#x60;parameters&#x60; does not fill. A declaration replaces them all, so a value saved for other goods is never sent. | [optional]
**single_parcel** | **bool** | The carrier takes this declaration on a shipment of one parcel only. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
