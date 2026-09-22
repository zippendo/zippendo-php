# CreateAddressRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Company or person the parcel is sent from, printed on labels |
**description** | **string** | Internal label for this address; never printed or sent to a carrier | [optional]
**att_contact** | **string** | Contact person at this address, printed as the att. line | [optional]
**address1** | **string** | Address line 1 |
**address2** | **string** | Address line 2 | [optional]
**zipcode** | **string** | Postal/ZIP code |
**city** | **string** | City |
**phone** | **string** | Phone number |
**country_code** | **string** | Country code (ISO 2 or 3 letter) |
**state** | **string** | State/Province | [optional]
**email** | **string** | Email address |
**customs** | **array<string,string>** | Customs identifiers (voec, eori, sprn, ioss, fda, duns) | [optional]
**address_types** | **string[]** | Address types (sender, pickup, return) | [optional]
**brand_id** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
