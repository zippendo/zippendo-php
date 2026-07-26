# Zippendo\Sdk\SystemApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**healthCheck()**](SystemApi.md#healthCheck) | **GET** /health | Health check |


## `healthCheck()`

```php
healthCheck(): \Zippendo\Sdk\Model\HealthCheck200Response
```

Health check

Return the service health status, current timestamp, and version.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\SystemApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->healthCheck();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SystemApi->healthCheck: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Zippendo\Sdk\Model\HealthCheck200Response**](../Model/HealthCheck200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
