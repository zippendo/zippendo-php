# CreateShipment201ResponseTracking

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | Public carrier tracking URL. | [optional]
**number** | **string** | Carrier tracking number. | [optional]
**label_free_code** | **string** | Label-free drop-off code. | [optional]
**qr_code_link** | **string** | DEPRECATED — use &#x60;qrCodeDataUri&#x60; (embeddable data URI) or &#x60;qrCodeUrl&#x60; (hosted link). Catch-all that carries whichever applies, kept populated for backwards compatibility during the migration and until it is disabled. | [optional]
**qr_code_data_uri** | **string** | Embeddable &#x60;data:&#x60; URI of the QR code image for label-free drop-off — base64 image bytes you can drop straight into an &lt;img&gt;/email. Null when the carrier returns a hosted link instead (see &#x60;qrCodeUrl&#x60;). | [optional]
**qr_code_url** | **string** | Carrier-hosted URL of the QR code image for label-free drop-off, returned by carriers (e.g. Bring) that link to the image rather than embedding it. Null when the carrier returns embeddable bytes (see &#x60;qrCodeDataUri&#x60;). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
