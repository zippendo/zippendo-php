# CreateOrderRequestOrderLinesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sku** | **string** | Stock keeping unit identifier. | [optional]
**name** | **string** | Product name. |
**quantity** | **int** | Quantity ordered. |
**unit_price** | **float** | Price per unit. | [optional]
**total_price** | **float** | Total price for the line. | [optional]
**currency** | **string** | ISO 4217 currency code. | [optional]
**weight** | **float** | Item weight in the given unit. | [optional]
**weight_unit** | **string** | Unit of the weight value. | [optional]
**variant_id** | **string** | Platform variant identifier. | [optional]
**product_id** | **string** | Platform product identifier. | [optional]
**image_url** | **string** | Product image URL. | [optional]
**hs_code** | **string** | Harmonized System customs code (6-13 digits). | [optional]
**country_of_origin** | **string** | ISO 3166-1 alpha-2 country of origin. | [optional]
**province_of_origin** | **string** | ISO 3166-2 province of origin. | [optional]
**barcode** | **string** | Item barcode (EAN/UPC). | [optional]
**requires_shipping** | **bool** | Whether the item requires shipping. | [optional]
**taxable** | **bool** | Whether the item is taxable. | [optional]
**gift_card** | **bool** | Whether the item is a gift card. | [optional]
**vendor** | **string** | Vendor or brand name. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
