# Zippendo\Sdk\WebhooksApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrgWebhook()**](WebhooksApi.md#createOrgWebhook) | **POST** /orgs/{orgId}/webhooks | Create webhook |
| [**deleteOrgWebhook()**](WebhooksApi.md#deleteOrgWebhook) | **DELETE** /orgs/{orgId}/webhooks/{webhookId} | Delete webhook |
| [**getOrgWebhook()**](WebhooksApi.md#getOrgWebhook) | **GET** /orgs/{orgId}/webhooks/{webhookId} | Get webhook |
| [**listOrgWebhookDeliveries()**](WebhooksApi.md#listOrgWebhookDeliveries) | **GET** /orgs/{orgId}/webhooks/{webhookId}/deliveries | List webhook deliveries |
| [**listOrgWebhooks()**](WebhooksApi.md#listOrgWebhooks) | **GET** /orgs/{orgId}/webhooks | List webhooks |
| [**testOrgWebhook()**](WebhooksApi.md#testOrgWebhook) | **POST** /orgs/{orgId}/webhooks/{webhookId}/test | Test webhook |
| [**updateOrgWebhook()**](WebhooksApi.md#updateOrgWebhook) | **PATCH** /orgs/{orgId}/webhooks/{webhookId} | Update webhook |


## `createOrgWebhook()`

```php
createOrgWebhook($org_id, $create_org_webhook_request): \Zippendo\Sdk\Model\CreateOrgWebhook201Response
```

Create webhook

Create a new webhook endpoint for an organization that receives event notifications.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$create_org_webhook_request = new \Zippendo\Sdk\Model\CreateOrgWebhookRequest(); // \Zippendo\Sdk\Model\CreateOrgWebhookRequest

try {
    $result = $apiInstance->createOrgWebhook($org_id, $create_org_webhook_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->createOrgWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_org_webhook_request** | [**\Zippendo\Sdk\Model\CreateOrgWebhookRequest**](../Model/CreateOrgWebhookRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateOrgWebhook201Response**](../Model/CreateOrgWebhook201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteOrgWebhook()`

```php
deleteOrgWebhook($org_id, $webhook_id): \Zippendo\Sdk\Model\DeleteOrgWebhook200Response
```

Delete webhook

Permanently delete a webhook and all its delivery logs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_clx1a2b3c4; // string | Organization ID
$webhook_id = wh_clx1a2b3c4; // string | Webhook ID

try {
    $result = $apiInstance->deleteOrgWebhook($org_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->deleteOrgWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **webhook_id** | **string**| Webhook ID | |

### Return type

[**\Zippendo\Sdk\Model\DeleteOrgWebhook200Response**](../Model/DeleteOrgWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrgWebhook()`

```php
getOrgWebhook($org_id, $webhook_id): \Zippendo\Sdk\Model\CreateOrgWebhook201Response
```

Get webhook

Get a specific webhook including its signing secret.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_clx1a2b3c4; // string | Organization ID
$webhook_id = wh_clx1a2b3c4; // string | Webhook ID

try {
    $result = $apiInstance->getOrgWebhook($org_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->getOrgWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **webhook_id** | **string**| Webhook ID | |

### Return type

[**\Zippendo\Sdk\Model\CreateOrgWebhook201Response**](../Model/CreateOrgWebhook201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOrgWebhookDeliveries()`

```php
listOrgWebhookDeliveries($org_id, $webhook_id, $page, $limit): \Zippendo\Sdk\Model\ListOrgWebhookDeliveries200Response
```

List webhook deliveries

List the delivery history for a specific webhook.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_clx1a2b3c4; // string | Organization ID
$webhook_id = wh_clx1a2b3c4; // string | Webhook ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)

try {
    $result = $apiInstance->listOrgWebhookDeliveries($org_id, $webhook_id, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->listOrgWebhookDeliveries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **webhook_id** | **string**| Webhook ID | |
| **page** | **int**| Page number (1-based) | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100) | [optional] [default to 20] |

### Return type

[**\Zippendo\Sdk\Model\ListOrgWebhookDeliveries200Response**](../Model/ListOrgWebhookDeliveries200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOrgWebhooks()`

```php
listOrgWebhooks($org_id, $page, $limit, $brand_id, $brand_scope): \Zippendo\Sdk\Model\ListOrgWebhooks200Response
```

List webhooks

List all webhooks belonging to an organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)
$brand_id = brnd_8f3kd92ld0; // string | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
$brand_scope = own; // string | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.

try {
    $result = $apiInstance->listOrgWebhooks($org_id, $page, $limit, $brand_id, $brand_scope);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->listOrgWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **page** | **int**| Page number (1-based) | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100) | [optional] [default to 20] |
| **brand_id** | **string**| Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brand_scope** | **string**| How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] |

### Return type

[**\Zippendo\Sdk\Model\ListOrgWebhooks200Response**](../Model/ListOrgWebhooks200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testOrgWebhook()`

```php
testOrgWebhook($org_id, $webhook_id): \Zippendo\Sdk\Model\TestOrgWebhook200Response
```

Test webhook

Send a test ping event to the webhook endpoint to verify connectivity.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_clx1a2b3c4; // string | Organization ID
$webhook_id = wh_clx1a2b3c4; // string | Webhook ID

try {
    $result = $apiInstance->testOrgWebhook($org_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->testOrgWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **webhook_id** | **string**| Webhook ID | |

### Return type

[**\Zippendo\Sdk\Model\TestOrgWebhook200Response**](../Model/TestOrgWebhook200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrgWebhook()`

```php
updateOrgWebhook($org_id, $webhook_id, $update_org_webhook_request): \Zippendo\Sdk\Model\CreateOrgWebhook201Response
```

Update webhook

Update the configuration of an existing webhook.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\WebhooksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_clx1a2b3c4; // string | Organization ID
$webhook_id = wh_clx1a2b3c4; // string | Webhook ID
$update_org_webhook_request = new \Zippendo\Sdk\Model\UpdateOrgWebhookRequest(); // \Zippendo\Sdk\Model\UpdateOrgWebhookRequest

try {
    $result = $apiInstance->updateOrgWebhook($org_id, $webhook_id, $update_org_webhook_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhooksApi->updateOrgWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **webhook_id** | **string**| Webhook ID | |
| **update_org_webhook_request** | [**\Zippendo\Sdk\Model\UpdateOrgWebhookRequest**](../Model/UpdateOrgWebhookRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateOrgWebhook201Response**](../Model/CreateOrgWebhook201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
