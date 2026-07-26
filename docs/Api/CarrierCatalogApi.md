# Zippendo\Sdk\CarrierCatalogApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listAvailableCarriers()**](CarrierCatalogApi.md#listAvailableCarriers) | **GET** /orgs/{orgId}/available-carriers | List available carriers |


## `listAvailableCarriers()`

```php
listAvailableCarriers($org_id): \Zippendo\Sdk\Model\ListAvailableCarriers200ResponseInner[]
```

List available carriers

Returns the carriers available to connect, as supported by the carrier server.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarrierCatalogApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID

try {
    $result = $apiInstance->listAvailableCarriers($org_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarrierCatalogApi->listAvailableCarriers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |

### Return type

[**\Zippendo\Sdk\Model\ListAvailableCarriers200ResponseInner[]**](../Model/ListAvailableCarriers200ResponseInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
