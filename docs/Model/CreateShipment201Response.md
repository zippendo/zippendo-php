# CreateShipment201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique shipment identifier. |
**reference** | **string** | Customer-facing shipment reference. |
**address_id** | **string** | Sender address identifier. | [optional]
**service_point_id** | **string** | Selected carrier service point identifier. | [optional]
**parties** | [**\Zippendo\Sdk\Model\CreateShipment201ResponsePartiesInner[]**](CreateShipment201ResponsePartiesInner.md) | Parties involved in the shipment (sender, receiver, etc.). |
**type** | **string** | Direction of the shipment relative to the organization. |
**carrier_settings** | [**\Zippendo\Sdk\Model\ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |
**parcels** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseParcelsInner[]**](CreateShipment201ResponseParcelsInner.md) | Parcels included in the shipment. |
**pickup_details** | [**\Zippendo\Sdk\Model\CreateShipment201ResponsePickupDetails**](CreateShipment201ResponsePickupDetails.md) |  | [optional]
**term_of_trade** | **string** | Incoterm governing the shipment. | [default to 'DAP']
**documents** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseDocumentsInner[]**](CreateShipment201ResponseDocumentsInner.md) | Documents generated for the shipment (labels, invoices). | [optional]
**errors** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseErrorsInner[]**](CreateShipment201ResponseErrorsInner.md) | Carrier errors recorded for the shipment. |
**tracking** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  | [optional]
**status** | **string** | Lifecycle status of the shipment. |
**org_id** | **string** | Owning organization identifier. |
**order_id** | **string** | Associated order identifier. | [optional]
**shipping_rule_id** | **string** | Applied shipping rule identifier. | [optional]
**shipping_rule** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseShippingRule**](CreateShipment201ResponseShippingRule.md) |  | [optional]
**label_printer_id** | **string** | Printer assigned for labels on this shipment. | [optional]
**document_printer_id** | **string** | Printer assigned for documents on this shipment. | [optional]
**logs** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseLogsInner[]**](CreateShipment201ResponseLogsInner.md) | Request/response logs captured during carrier interactions. |
**activities** | [**\Zippendo\Sdk\Model\CreateShipment201ResponseActivitiesInner[]**](CreateShipment201ResponseActivitiesInner.md) | Chronological activity history of the shipment. |
**created_at** | **string** | Timestamp when the shipment was created. |
**updated_at** | **string** | Timestamp when the shipment was last updated. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
