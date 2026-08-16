# ListShippingRules200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique shipping rule identifier |
**name** | **string** | Shipping rule name |
**description** | **string** | Optional description |
**direction** | **string** | Whether this rule is for outbound or inbound (return) shipments | [default to 'outbound']
**carrier_id** | **string** | Carrier ID |
**product_id** | **string** | Product ID from carrier |
**services** | **string[]** | List of selected services |
**additional_parameters** | [**array<string,\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInnerAdditionalParametersValue>**](ListShippingRules200ResponseDataInnerAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60;. |
**address_id** | **string** | Sender address ID |
**receiving_countries** | **string[]** | List of supported country codes |
**email_notification** | **bool** | Send email notification to recipient | [default to false]
**phone_notification** | **bool** | Send SMS notification to recipient | [default to false]
**min_weight** | **float** | Minimum required weight in kg. Orders below this are excluded from the rule. |
**max_weight** | **float** | Maximum allowed weight in kg. Orders exceeding this are excluded from the rule. |
**min_order_value** | **float** | Minimum required order value in currency units. Orders below this are excluded from the rule. |
**max_order_value** | **float** | Maximum allowed order value in currency units. Orders exceeding this are excluded from the rule. |
**conditions** | [**\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInnerConditionsInner[]**](ListShippingRules200ResponseDataInnerConditionsInner.md) | Rule conditions (weight/price/quantity) |
**generate_proforma_invoice** | **bool** | Generate proforma invoice for shipments | [default to false]
**generate_commercial_invoice** | **bool** | Generate commercial invoice for international shipments | [default to false]
**generate_packing_list** | **bool** | Generate packing slip with package and item details | [default to false]
**auto_print_labels** | **bool** | Automatically print labels when shipment is sent | [default to false]
**auto_print_documents** | **bool** | Automatically print documents when shipment is sent | [default to false]
**label_printer_id** | **string** | ID of the label printer |
**document_printer_id** | **string** | ID of the document printer |
**return_shipping_rule_id** | **string** | ID of the return shipping rule |
**auto_create_return_shipment** | **bool** | Automatically create and send a return shipment on dispatch | [default to false]
**org_id** | **string** | Owning organization ID |
**brand_id** | **string** | Brand this record belongs to, or null when it is organization-wide |
**created_at** | **string** | Creation timestamp (ISO 8601) |
**updated_at** | **string** | Last update timestamp (ISO 8601) |
**carrier** | [**\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInnerCarrier**](ListShippingRules200ResponseDataInnerCarrier.md) |  |
**address** | [**\Zippendo\Sdk\Model\ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md) |  |
**label_printer** | [**\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInnerLabelPrinter**](ListShippingRules200ResponseDataInnerLabelPrinter.md) |  | [optional]
**document_printer** | [**\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInnerLabelPrinter**](ListShippingRules200ResponseDataInnerLabelPrinter.md) |  | [optional]
**return_shipping_rule** | [**\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInnerReturnShippingRule**](ListShippingRules200ResponseDataInnerReturnShippingRule.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
