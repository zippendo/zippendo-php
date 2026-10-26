# UpdateShippingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Shipping rule name | [optional]
**description** | **string** | Optional description | [optional]
**translations** | [**array<string,\Zippendo\Sdk\Model\CreateShippingRuleRequestTranslationsValue>**](CreateShippingRuleRequestTranslationsValue.md) | Checkout name and description per language; a blank field falls back to the rule&#39;s own text | [optional]
**direction** | **string** | Whether this rule is for outbound or inbound (return) shipments | [optional]
**carrier_id** | **string** | Carrier ID | [optional]
**product_id** | **string** | Product ID from carrier | [optional]
**services** | **string[]** | List of selected services | [optional]
**additional_parameters** | [**array<string,\Zippendo\Sdk\Model\CreateShippingRuleRequestAdditionalParametersValue>**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60;. Omit to leave the rule&#39;s parameters unchanged. | [optional]
**address_id** | **string** | Sender address ID | [optional]
**receiving_countries** | **string[]** | List of supported country codes | [optional]
**email_notification** | **bool** | Send an email notification to the receiver | [optional]
**phone_notification** | **bool** | Send an SMS notification to the receiver | [optional]
**min_weight** | **float** | Minimum required weight in kg | [optional]
**max_weight** | **float** | Maximum allowed weight in kg | [optional]
**min_order_value** | **float** | Minimum required order value in currency units | [optional]
**max_order_value** | **float** | Maximum allowed order value in currency units | [optional]
**conditions** | [**\Zippendo\Sdk\Model\CreateShippingRuleRequestConditionsInner[]**](CreateShippingRuleRequestConditionsInner.md) | Rule conditions (weight/price/quantity) | [optional]
**generate_proforma_invoice** | **bool** | Generate proforma invoice for shipments | [optional]
**generate_commercial_invoice** | **bool** | Generate commercial invoice for international shipments | [optional]
**generate_packing_list** | **bool** | Generate a packing slip with parcel and item details | [optional]
**auto_print_labels** | **bool** | Automatically print labels when shipment is sent | [optional]
**auto_print_documents** | **bool** | Automatically print documents when shipment is sent | [optional]
**label_printer_id** | **string** | ID of the label printer | [optional]
**document_printer_id** | **string** | ID of the document printer | [optional]
**return_shipping_rule_id** | **string** | ID of the return shipping rule | [optional]
**auto_create_return_shipment** | **bool** | Automatically create and send a return shipment on dispatch | [optional]
**brand_id** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
