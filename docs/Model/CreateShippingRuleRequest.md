# CreateShippingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Shipping rule name |
**description** | **string** | Optional description | [optional]
**direction** | **string** | Whether this rule is for outbound or inbound (return) shipments | [optional] [default to 'outbound']
**carrier_id** | **string** | Carrier ID |
**product_id** | **string** | Product ID from carrier |
**services** | **string[]** | List of selected services |
**additional_parameters** | [**array<string,\Zippendo\Sdk\Model\CreateShippingRuleRequestAdditionalParametersValue>**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60; (e.g. &#x60;returnFunctionality&#x60;). | [optional]
**address_id** | **string** | Sender address ID |
**receiving_countries** | **string[]** | List of supported country codes |
**email_notification** | **bool** | Send email notification to recipient | [optional] [default to false]
**phone_notification** | **bool** | Send SMS notification to recipient | [optional] [default to false]
**min_weight** | **float** | Minimum required weight in kg | [optional]
**max_weight** | **float** | Maximum allowed weight in kg | [optional]
**min_order_value** | **float** | Minimum required order value in currency units | [optional]
**max_order_value** | **float** | Maximum allowed order value in currency units | [optional]
**conditions** | [**\Zippendo\Sdk\Model\CreateShippingRuleRequestConditionsInner[]**](CreateShippingRuleRequestConditionsInner.md) | Rule conditions (weight/price/quantity) |
**generate_proforma_invoice** | **bool** | Generate proforma invoice for shipments | [optional] [default to false]
**generate_commercial_invoice** | **bool** | Generate commercial invoice for international shipments | [optional] [default to false]
**generate_packing_list** | **bool** | Generate packing slip with package and item details | [optional] [default to false]
**auto_print_labels** | **bool** | Automatically print labels when shipment is sent | [optional] [default to false]
**auto_print_documents** | **bool** | Automatically print documents when shipment is sent | [optional] [default to false]
**label_printer_id** | **string** | ID of the label printer | [optional]
**document_printer_id** | **string** | ID of the document printer | [optional]
**return_shipping_rule_id** | **string** | ID of the return shipping rule | [optional]
**auto_create_return_shipment** | **bool** | Automatically create and send a return shipment on dispatch | [optional] [default to false]
**brand_id** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
