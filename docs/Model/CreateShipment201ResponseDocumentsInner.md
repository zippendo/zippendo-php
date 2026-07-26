# CreateShipment201ResponseDocumentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique document identifier. |
**shipment_id** | **string** | Identifier of the shipment this document belongs to. |
**document_type** | **string** | Type of shipment document. |
**format** | **string** | File format of the document content. |
**content** | **string** | Base64-encoded document/label content. |
**size** | **string** | Physical print size of the document. | [default to 'A4']
**created_at** | **string** | Timestamp when the document was created. |
**updated_at** | **string** | Timestamp when the document was last updated. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
