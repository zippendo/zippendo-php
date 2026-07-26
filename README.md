# Zippendo PHP SDK

Official PHP client for the [Zippendo](https://zippendo.com) shipping & logistics API. Requires
PHP 7.4+ and Composer.

## Install

```sh
composer require zippendo/zippendo-php
```

## Authentication

Create an API token in your Zippendo dashboard (**Settings → API tokens**) — a Bearer token prefixed
with `zipp_`. Set it on the configuration:

```php
<?php
require_once __DIR__ . "/vendor/autoload.php";

$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()
    ->setAccessToken(getenv("ZIPPENDO_API_TOKEN"));
```

The base URL defaults to `https://api.zippendo.com`.

## Resources & clients

The API is split into resource clients — `ShipmentsApi`, `OrdersApi`, `CarriersApi`, `AddressesApi`,
`RulesApi`, `WebhooksApi`, `TokensApi`, and more. Each takes an HTTP client and your config:

```php
$shipments = new Zippendo\Sdk\Api\ShipmentsApi(new GuzzleHttp\Client(), $config);
$orders = new Zippendo\Sdk\Api\OrdersApi(new GuzzleHttp\Client(), $config);
```

## The `org_id` parameter

Every call takes an `org_id` (your organization ID, found in the dashboard). It is explicit on each
call by design: one API token can be granted access to multiple organizations, and `org_id` selects
which one the request acts on.

## Listing & pagination

List endpoints accept `page` (1-based) and `limit`, and return a page with `getData()` plus
`getTotal()`, `getPage()`, `getLimit()`, and `getTotalPages()`:

```php
$result = $shipments->listShipments("org_8f3kd92ld0", 1, 50);
foreach ($result->getData() as $shipment) {
    echo $shipment->getId(), PHP_EOL;
}
echo $result->getTotal(), " / ", $result->getTotalPages(), PHP_EOL;
```

## Creating resources

```php
$order = $orders->createOrder("org_8f3kd92ld0", new \Zippendo\Sdk\Model\CreateOrderRequest([
    "order_number" => "1001",
    "order_channel_id" => "chan_7d2k1",
    "order_lines" => [
        new \Zippendo\Sdk\Model\CreateOrderRequestOrderLinesInner(["name" => "T-shirt", "quantity" => 2]),
    ],
]));
echo $order->getId(), PHP_EOL;
```

See [`./docs/Api`](./docs/Api) for the full request/response shape of every operation.

## Error handling

Non-2xx responses throw `ApiException`. The response body is Zippendo's canonical
`{ code, error, message }` — branch on the machine-readable `code`:

```php
try {
    $shipments->getShipment("org_8f3kd92ld0", "shp_missing");
} catch (\Zippendo\Sdk\ApiException $e) {
    echo $e->getCode(), PHP_EOL;           // HTTP status
    echo $e->getResponseBody(), PHP_EOL;   // JSON, e.g. {"code":"SHIPMENT_NOT_FOUND", ...}
}
```

## Configuration

Point the client at a different environment by overriding the host:

```php
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()
    ->setAccessToken(getenv("ZIPPENDO_API_TOKEN"))
    ->setHost("https://staging.api.zippendo.com");
```

## Reference

Full per-endpoint and per-model documentation is in [`./docs`](./docs). Hosted reference:
<https://www.zippendo.com/docs/api-reference/overview>.

## License

[MIT](./LICENSE.md)
