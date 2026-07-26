# CreateShipment201ResponseShippingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique shipping rule identifier. |
**name** | **string** | Display name of the shipping rule. |
**carrier_id** | **string** | Carrier applied by the rule. |
**product_id** | **string** | Carrier product applied by the rule. |
**services** | **string[]** | Additional service codes applied by the rule. |
**address_id** | **string** | Sender address applied by the rule. |
**return_shipping_rule_id** | **string** | Shipping rule used for return shipments. | [optional]
**auto_create_return_shipment** | **bool** | Whether a return shipment is created automatically. | [optional]
**auto_print_labels** | **bool** | Whether labels are printed automatically on send. | [optional]
**auto_print_documents** | **bool** | Whether documents are printed automatically on send. | [optional]
**label_printer_id** | **string** | Printer used for labels. | [optional]
**document_printer_id** | **string** | Printer used for documents. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
