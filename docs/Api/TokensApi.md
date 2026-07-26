# Zippendo\Sdk\TokensApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApiToken()**](TokensApi.md#createApiToken) | **POST** /orgs/{orgId}/api-tokens | Create API keys |
| [**getApiToken()**](TokensApi.md#getApiToken) | **GET** /orgs/{orgId}/api-tokens/{tokenId} | Get API keys |
| [**listApiTokens()**](TokensApi.md#listApiTokens) | **GET** /orgs/{orgId}/api-tokens | List API keys |
| [**revokeApiToken()**](TokensApi.md#revokeApiToken) | **DELETE** /orgs/{orgId}/api-tokens/{tokenId} | Revoke API keys |
| [**updateApiToken()**](TokensApi.md#updateApiToken) | **PATCH** /orgs/{orgId}/api-tokens/{tokenId} | Update API keys |
| [**verifyApiToken()**](TokensApi.md#verifyApiToken) | **POST** /api-tokens/verify | Verify API keys |


## `createApiToken()`

```php
createApiToken($org_id, $create_api_token_request): \Zippendo\Sdk\Model\CreateApiToken201Response
```

Create API keys

Creates a new API token for the specified organization. The full token is only shown once.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_4d8af01qw2; // string | Organization ID
$create_api_token_request = new \Zippendo\Sdk\Model\CreateApiTokenRequest(); // \Zippendo\Sdk\Model\CreateApiTokenRequest

try {
    $result = $apiInstance->createApiToken($org_id, $create_api_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->createApiToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_api_token_request** | [**\Zippendo\Sdk\Model\CreateApiTokenRequest**](../Model/CreateApiTokenRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateApiToken201Response**](../Model/CreateApiToken201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApiToken()`

```php
getApiToken($org_id, $token_id): \Zippendo\Sdk\Model\ListApiTokens200ResponseDataInner
```

Get API keys

Returns metadata for a specific API token. The token secret is never returned.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_4d8af01qw2; // string | Organization ID
$token_id = tok_6e2fa83ij9; // string | API Token ID

try {
    $result = $apiInstance->getApiToken($org_id, $token_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->getApiToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **token_id** | **string**| API Token ID | |

### Return type

[**\Zippendo\Sdk\Model\ListApiTokens200ResponseDataInner**](../Model/ListApiTokens200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listApiTokens()`

```php
listApiTokens($org_id, $page, $limit): \Zippendo\Sdk\Model\ListApiTokens200Response
```

List API keys

Returns a paginated list of API tokens belonging to the specified organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_4d8af01qw2; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)

try {
    $result = $apiInstance->listApiTokens($org_id, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->listApiTokens: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **page** | **int**| Page number (1-based) | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100) | [optional] [default to 20] |

### Return type

[**\Zippendo\Sdk\Model\ListApiTokens200Response**](../Model/ListApiTokens200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeApiToken()`

```php
revokeApiToken($org_id, $token_id): \Zippendo\Sdk\Model\RevokeApiToken200Response
```

Revoke API keys

Revokes and deletes an API token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_4d8af01qw2; // string | Organization ID
$token_id = tok_6e2fa83ij9; // string | API Token ID

try {
    $result = $apiInstance->revokeApiToken($org_id, $token_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->revokeApiToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **token_id** | **string**| API Token ID | |

### Return type

[**\Zippendo\Sdk\Model\RevokeApiToken200Response**](../Model/RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateApiToken()`

```php
updateApiToken($org_id, $token_id, $update_api_token_request): \Zippendo\Sdk\Model\ListApiTokens200ResponseDataInner
```

Update API keys

Updates the name of an API token.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_4d8af01qw2; // string | Organization ID
$token_id = tok_6e2fa83ij9; // string | API Token ID
$update_api_token_request = new \Zippendo\Sdk\Model\UpdateApiTokenRequest(); // \Zippendo\Sdk\Model\UpdateApiTokenRequest

try {
    $result = $apiInstance->updateApiToken($org_id, $token_id, $update_api_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->updateApiToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **token_id** | **string**| API Token ID | |
| **update_api_token_request** | [**\Zippendo\Sdk\Model\UpdateApiTokenRequest**](../Model/UpdateApiTokenRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListApiTokens200ResponseDataInner**](../Model/ListApiTokens200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verifyApiToken()`

```php
verifyApiToken($verify_api_token_request): \Zippendo\Sdk\Model\VerifyApiToken200Response
```

Verify API keys

Verifies whether an API token is valid and returns its metadata.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\TokensApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$verify_api_token_request = new \Zippendo\Sdk\Model\VerifyApiTokenRequest(); // \Zippendo\Sdk\Model\VerifyApiTokenRequest

try {
    $result = $apiInstance->verifyApiToken($verify_api_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokensApi->verifyApiToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **verify_api_token_request** | [**\Zippendo\Sdk\Model\VerifyApiTokenRequest**](../Model/VerifyApiTokenRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\VerifyApiToken200Response**](../Model/VerifyApiToken200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
