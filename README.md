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

## Brands

A brand is a sub-account inside an organization: one company running several consumer-facing labels
(say Pitaya and Kiwi) keeps each label's orders and shipments separate, with its own company name,
address and logo on the documents its shipments produce. Scope a request to one brand with the
`X-Zippendo-Brand` header, whose value is the brand's ID or slug.

The header is not a method argument — it applies uniformly to every operation, so put it on the
Guzzle client you hand to the resource clients, and every call they make carries it:

```php
$pitaya = new GuzzleHttp\Client([
    'headers' => ['X-Zippendo-Brand' => 'pitaya'], // brand ID or slug
]);

$shipments = new Zippendo\Sdk\Api\ShipmentsApi($pitaya, $config);
$shipments->listShipments('org_8f3kd92ld0', 1, 50); // Pitaya's shipments only
```

To address two brands from one process, build a Guzzle client per brand and pass each to its own
resource clients. Omit the header and the request covers the whole organization — the behaviour of
every existing token. A header naming a brand that does not exist in the organization is rejected
with `404 BRAND_NOT_FOUND`.

An API token created with a `brand_id` is permanently confined to that brand and needs no header.
Sending `X-Zippendo-Brand` naming a *different* brand on such a token is refused with
`403 BRAND_ACCESS_DENIED` — the binding is never widened.

Creating, updating and deleting brands is done in the Zippendo dashboard; brand management is not
part of this SDK.

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
