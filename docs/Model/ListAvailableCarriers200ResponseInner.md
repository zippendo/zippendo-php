# ListAvailableCarriers200ResponseInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Display name of the carrier |
**slug** | **string** | Unique carrier slug identifier |
**group** | **string** | Carrier group or family name | [optional]
**description** | **string** | Short description of the carrier | [optional]
**logo** | **string** | URL to the carrier logo image | [optional]
**brand_color** | **string** | Carrier brand color (hex) | [optional]
**learn_more_url** | **string** | URL with more information about the carrier | [optional]
**required_fields** | [**\Zippendo\Sdk\Model\ListAvailableCarriers200ResponseInnerRequiredFieldsInner[]**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Configuration fields that must be provided to connect the carrier | [optional]
**optional_fields** | [**\Zippendo\Sdk\Model\ListAvailableCarriers200ResponseInnerRequiredFieldsInner[]**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Optional configuration fields for the carrier | [optional]
**deprecated** | **bool** | Whether this integration is deprecated (still works, but discouraged) | [optional]
**deprecation_message** | **string** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
