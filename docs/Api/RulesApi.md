# Zippendo\Sdk\RulesApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createShippingRule()**](RulesApi.md#createShippingRule) | **POST** /orgs/{orgId}/shipping-rules | Create shipping rule |
| [**deleteShippingRule()**](RulesApi.md#deleteShippingRule) | **DELETE** /orgs/{orgId}/shipping-rules/{ruleId} | Delete shipping rule |
| [**getShippingRule()**](RulesApi.md#getShippingRule) | **GET** /orgs/{orgId}/shipping-rules/{ruleId} | Get shipping rule |
| [**listShippingRules()**](RulesApi.md#listShippingRules) | **GET** /orgs/{orgId}/shipping-rules | List shipping rules |
| [**updateShippingRule()**](RulesApi.md#updateShippingRule) | **PATCH** /orgs/{orgId}/shipping-rules/{ruleId} | Update shipping rule |


## `createShippingRule()`

```php
createShippingRule($org_id, $create_shipping_rule_request): \Zippendo\Sdk\Model\CreateShippingRule201Response
```

Create shipping rule

Creates a new shipping rule with conditions and carrier product for the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$create_shipping_rule_request = new \Zippendo\Sdk\Model\CreateShippingRuleRequest(); // \Zippendo\Sdk\Model\CreateShippingRuleRequest

try {
    $result = $apiInstance->createShippingRule($org_id, $create_shipping_rule_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->createShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_shipping_rule_request** | [**\Zippendo\Sdk\Model\CreateShippingRuleRequest**](../Model/CreateShippingRuleRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateShippingRule201Response**](../Model/CreateShippingRule201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteShippingRule()`

```php
deleteShippingRule($org_id, $rule_id): \Zippendo\Sdk\Model\DeleteShippingRule200Response
```

Delete shipping rule

Deletes a shipping rule belonging to the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$rule_id = rule_01HZX9K2QF; // string | Shipping Rule ID

try {
    $result = $apiInstance->deleteShippingRule($org_id, $rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->deleteShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **rule_id** | **string**| Shipping Rule ID | |

### Return type

[**\Zippendo\Sdk\Model\DeleteShippingRule200Response**](../Model/DeleteShippingRule200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getShippingRule()`

```php
getShippingRule($org_id, $rule_id): \Zippendo\Sdk\Model\ListShippingRules200ResponseDataInner
```

Get shipping rule

Returns a single shipping rule with its carrier, address and printer relations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$rule_id = rule_01HZX9K2QF; // string | Shipping Rule ID

try {
    $result = $apiInstance->getShippingRule($org_id, $rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->getShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **rule_id** | **string**| Shipping Rule ID | |

### Return type

[**\Zippendo\Sdk\Model\ListShippingRules200ResponseDataInner**](../Model/ListShippingRules200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listShippingRules()`

```php
listShippingRules($org_id, $page, $limit, $brand_id, $brand_scope): \Zippendo\Sdk\Model\ListShippingRules200Response
```

List shipping rules

Returns a paginated list of shipping rules for the organization with their relations.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)
$brand_id = brnd_8f3kd92ld0; // string | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
$brand_scope = own; // string | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.

try {
    $result = $apiInstance->listShippingRules($org_id, $page, $limit, $brand_id, $brand_scope);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->listShippingRules: ', $e->getMessage(), PHP_EOL;
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

[**\Zippendo\Sdk\Model\ListShippingRules200Response**](../Model/ListShippingRules200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateShippingRule()`

```php
updateShippingRule($org_id, $rule_id, $update_shipping_rule_request): \Zippendo\Sdk\Model\CreateShippingRule201Response
```

Update shipping rule

Updates an existing shipping rule for the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$rule_id = rule_01HZX9K2QF; // string | Shipping Rule ID
$update_shipping_rule_request = new \Zippendo\Sdk\Model\UpdateShippingRuleRequest(); // \Zippendo\Sdk\Model\UpdateShippingRuleRequest

try {
    $result = $apiInstance->updateShippingRule($org_id, $rule_id, $update_shipping_rule_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->updateShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **rule_id** | **string**| Shipping Rule ID | |
| **update_shipping_rule_request** | [**\Zippendo\Sdk\Model\UpdateShippingRuleRequest**](../Model/UpdateShippingRuleRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateShippingRule201Response**](../Model/CreateShippingRule201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
