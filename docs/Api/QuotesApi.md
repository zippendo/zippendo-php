# Zippendo\Sdk\QuotesApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createShippingQuote()**](QuotesApi.md#createShippingQuote) | **POST** /orgs/{orgId}/shipping-quote | Calculate shipping rates |


## `createShippingQuote()`

```php
createShippingQuote($org_id, $create_shipping_quote_request): \Zippendo\Sdk\Model\CreateShippingQuote200Response
```

Calculate shipping rates

Calculates shipping rates from configured shipping rules based on cart items and destination.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\QuotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$create_shipping_quote_request = new \Zippendo\Sdk\Model\CreateShippingQuoteRequest(); // \Zippendo\Sdk\Model\CreateShippingQuoteRequest

try {
    $result = $apiInstance->createShippingQuote($org_id, $create_shipping_quote_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QuotesApi->createShippingQuote: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_shipping_quote_request** | [**\Zippendo\Sdk\Model\CreateShippingQuoteRequest**](../Model/CreateShippingQuoteRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateShippingQuote200Response**](../Model/CreateShippingQuote200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
