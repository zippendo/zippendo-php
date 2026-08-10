# CreateShipmentRequestParcelsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique parcel identifier. | [optional]
**weight** | **float** | Parcel weight in the given weight unit. |
**weight_unit** | **string** | Unit of measurement for parcel weight. |
**dimensions** | [**\Zippendo\Sdk\Model\CreateShipmentRequestParcelsInnerDimensions**](CreateShipmentRequestParcelsInnerDimensions.md) |  |
**order_lines** | [**\Zippendo\Sdk\Model\CreateShipmentRequestParcelsInnerOrderLinesInner[]**](CreateShipmentRequestParcelsInnerOrderLinesInner.md) | Order lines contained in this parcel. |
**tracking_number** | **string** | Carrier tracking number for this parcel. | [optional]
**tracking_url** | **string** | Public carrier tracking URL for this parcel. | [optional]
**label_free_code** | **string** | Label-free drop-off code for the parcel. | [optional]
**qr_code_link** | **string** | DEPRECATED — use &#x60;qrCodeDataUri&#x60; (embeddable data URI) or &#x60;qrCodeUrl&#x60; (hosted link). Catch-all that carries whichever applies, kept populated for backwards compatibility during the migration and until it is disabled. | [optional]
**qr_code_data_uri** | **string** | Embeddable &#x60;data:&#x60; URI of the QR code image for label-free drop-off — base64 image bytes you can drop straight into an &lt;img&gt;/email. Populated whenever the image bytes are available, including for carriers that host the image (it is fetched and inlined); null if the carrier published no QR code or its image could not be retrieved. | [optional]
**qr_code_url** | **string** | Carrier-hosted URL of the QR code image for label-free drop-off, returned by carriers (e.g. Bring) that link to the image rather than embedding it. Independent of &#x60;qrCodeDataUri&#x60; — both are set when the hosted image was inlined successfully; null for carriers that only return embedded bytes. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
