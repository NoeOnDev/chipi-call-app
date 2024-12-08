# OAuthClientCredentials
No description provided (generated by Swagger Codegen https://github.com/swagger-api/swagger-codegen)

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 
- Package version: 1.0.8
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/abantecart/ups-oauth-client-credentials.git"
    }
  ],
  "require": {
    "abantecart/ups-oauth-client-credentials": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/OAuthClientCredentials/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure HTTP basic authorization: basicAuth
$config = UPS\OAuthClientCredentials\Configuration::getDefaultConfiguration()
    ->setUsername('YOUR_USERNAME')
    ->setPassword('YOUR_PASSWORD');

$apiInstance = new UPS\OAuthClientCredentials\Request\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$grant_type = "grant_type_example"; // string | 
$x_merchant_id = "x_merchant_id_example"; // string | 6-digit UPS account number.

try {
    $result = $apiInstance->createToken($grant_type, $x_merchant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->createToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://wwwcie.ups.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**createToken**](docs/Api/DefaultApi.md#createtoken) | **POST** /security/v1/oauth/token | Create Token

## Documentation For Models

 - [ErrorResponseWrapper](docs/Model/ErrorResponseWrapper.md)
 - [Errors](docs/Model/Errors.md)
 - [OauthTokenBody](docs/Model/OauthTokenBody.md)
 - [TokenErrorResponse](docs/Model/TokenErrorResponse.md)
 - [TokenSuccessResponse](docs/Model/TokenSuccessResponse.md)

## Documentation For Authorization


## basicAuth

- **Type**: HTTP basic authentication


## Author


