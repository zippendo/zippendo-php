# Zippendo\Sdk\AddressesApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAddress()**](AddressesApi.md#createAddress) | **POST** /orgs/{orgId}/addresses | Create address |
| [**deleteAddress()**](AddressesApi.md#deleteAddress) | **DELETE** /orgs/{orgId}/addresses/{addressId} | Delete address |
| [**getAddress()**](AddressesApi.md#getAddress) | **GET** /orgs/{orgId}/addresses/{addressId} | Get address |
| [**listAddresses()**](AddressesApi.md#listAddresses) | **GET** /orgs/{orgId}/addresses | List addresses |
| [**updateAddress()**](AddressesApi.md#updateAddress) | **PUT** /orgs/{orgId}/addresses/{addressId} | Update address |


## `createAddress()`

```php
createAddress($org_id, $create_address_request): \Zippendo\Sdk\Model\ListAddresses200ResponseDataInner
```

Create address

Creates a new sender, pickup or return address for the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$create_address_request = new \Zippendo\Sdk\Model\CreateAddressRequest(); // \Zippendo\Sdk\Model\CreateAddressRequest

try {
    $result = $apiInstance->createAddress($org_id, $create_address_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->createAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_address_request** | [**\Zippendo\Sdk\Model\CreateAddressRequest**](../Model/CreateAddressRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListAddresses200ResponseDataInner**](../Model/ListAddresses200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteAddress()`

```php
deleteAddress($org_id, $address_id): string
```

Delete address

Deletes an address belonging to the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$address_id = addr_01HZX9K2QF; // string | Address ID

try {
    $result = $apiInstance->deleteAddress($org_id, $address_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->deleteAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **address_id** | **string**| Address ID | |

### Return type

**string**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAddress()`

```php
getAddress($org_id, $address_id): \Zippendo\Sdk\Model\ListAddresses200ResponseDataInner
```

Get address

Returns a single address belonging to the organization, identified by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$address_id = addr_01HZX9K2QF; // string | Address ID

try {
    $result = $apiInstance->getAddress($org_id, $address_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->getAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **address_id** | **string**| Address ID | |

### Return type

[**\Zippendo\Sdk\Model\ListAddresses200ResponseDataInner**](../Model/ListAddresses200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listAddresses()`

```php
listAddresses($org_id, $page, $limit, $type, $brand_id, $brand_scope): \Zippendo\Sdk\Model\ListAddresses200Response
```

List addresses

Returns a paginated list of addresses for the organization, optionally filtered by type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)
$type = sender; // string | Filter by address type (sender, pickup, return)
$brand_id = brnd_8f3kd92ld0; // string | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
$brand_scope = own; // string | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.

try {
    $result = $apiInstance->listAddresses($org_id, $page, $limit, $type, $brand_id, $brand_scope);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->listAddresses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **page** | **int**| Page number (1-based) | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100) | [optional] [default to 20] |
| **type** | **string**| Filter by address type (sender, pickup, return) | [optional] |
| **brand_id** | **string**| Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brand_scope** | **string**| How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] |

### Return type

[**\Zippendo\Sdk\Model\ListAddresses200Response**](../Model/ListAddresses200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateAddress()`

```php
updateAddress($org_id, $address_id, $update_address_request): \Zippendo\Sdk\Model\ListAddresses200ResponseDataInner
```

Update address

Updates an existing address belonging to the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\AddressesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$address_id = addr_01HZX9K2QF; // string | Address ID
$update_address_request = new \Zippendo\Sdk\Model\UpdateAddressRequest(); // \Zippendo\Sdk\Model\UpdateAddressRequest

try {
    $result = $apiInstance->updateAddress($org_id, $address_id, $update_address_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressesApi->updateAddress: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **address_id** | **string**| Address ID | |
| **update_address_request** | [**\Zippendo\Sdk\Model\UpdateAddressRequest**](../Model/UpdateAddressRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListAddresses200ResponseDataInner**](../Model/ListAddresses200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
