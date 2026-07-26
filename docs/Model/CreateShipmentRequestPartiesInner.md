# CreateShipmentRequestPartiesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Role of the party in the shipment. |
**name** | **string** | Full name or company name of the party. |
**attention** | **string** | Attention contact at the party. | [optional]
**address1** | **string** | Primary street address line. |
**address2** | **string** | Secondary address line. | [optional]
**postal_code** | **string** | Postal code of the party address. |
**city** | **string** | City of the party address. |
**country_code** | **string** | ISO 3166-1 alpha-2 country code. |
**email** | **string** | Email address of the party. | [optional]
**phone** | **string** | Phone number of the party in E.164 format. | [optional]
**attributes** | [**\Zippendo\Sdk\Model\CreateShipmentRequestPartiesInnerAttributesInner[]**](CreateShipmentRequestPartiesInnerAttributesInner.md) | Additional carrier-specific attributes for the party. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
