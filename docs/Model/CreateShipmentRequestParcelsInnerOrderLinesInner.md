# CreateShipmentRequestParcelsInnerOrderLinesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique order line identifier. | [optional]
**order_line_id** | **string** | ID of the order line this packed line came from. Null when the item did not originate from an order line, such as a free gift or a replacement part. | [optional]
**sku** | **string** | Stock keeping unit of the product. Optional — not every webshop assigns SKUs. | [optional]
**quantity** | **int** | Number of units in this order line. |
**description** | **string** | Human-readable product description. | [optional]
**unit_price** | **float** | Price per unit in the order line currency. | [optional]
**currency** | **string** | ISO 4217 currency code. | [optional]
**vat_percent** | **float** | VAT percentage applied to the unit price. | [optional]
**location** | **string** | Warehouse picking location. | [optional]
**country_of_origin** | **string** | ISO 3166-1 alpha-2 country of origin. | [optional]
**hs_code** | **string** | Harmonized System customs code. | [optional]
**tarrif_number** | **string** | Deprecated misspelling of &#x60;hsCode&#x60;, kept for backwards compatibility. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
