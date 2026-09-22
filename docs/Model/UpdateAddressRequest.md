# UpdateAddressRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Company or person the parcel is sent from, printed on labels | [optional]
**description** | **string** | Internal label for this address; send null or an empty string to clear it | [optional]
**att_contact** | **string** | Contact person at this address; send null or an empty string to clear it | [optional]
**address1** | **string** | Address line 1 | [optional]
**address2** | **string** | Address line 2; send null or an empty string to clear it | [optional]
**zipcode** | **string** | Postal/ZIP code | [optional]
**city** | **string** | City | [optional]
**phone** | **string** | Phone number | [optional]
**country_code** | **string** | ISO country code | [optional]
**state** | **string** | State/Province; send null or an empty string to clear it | [optional]
**email** | **string** | Email address | [optional]
**customs** | **array<string,string>** | Customs identifiers | [optional]
**address_types** | **string[]** | Address types (sender, pickup, return) | [optional]
**brand_id** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
