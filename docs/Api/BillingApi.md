# Zippendo\Sdk\BillingApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getBillingUsage()**](BillingApi.md#getBillingUsage) | **GET** /orgs/{orgId}/billing/usage | Get usage |


## `getBillingUsage()`

```php
getBillingUsage($org_id): \Zippendo\Sdk\Model\GetBillingUsage200Response
```

Get usage

Get detailed usage statistics for the current billing period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID

try {
    $result = $apiInstance->getBillingUsage($org_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->getBillingUsage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |

### Return type

[**\Zippendo\Sdk\Model\GetBillingUsage200Response**](../Model/GetBillingUsage200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
