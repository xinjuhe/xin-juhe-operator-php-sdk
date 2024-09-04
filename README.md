# OpenAPIClient-php

运营商业务API接口平台应用程序接口文档

For more information, please visit [https://juhe.xin](https://juhe.xin).

## Installation & Usage

### Requirements

PHP 7.2 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: Authorization
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BalanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BalanceApi->getBalance: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.juhe.xin*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BalanceApi* | [**getBalance**](docs/Api/BalanceApi.md#getbalance) | **POST** /user/api/v1/balance | 获取用户余额
*OauthApi* | [**getToken**](docs/Api/OauthApi.md#gettoken) | **POST** /oauth2/token | 获取Token
*OauthApi* | [**getUserInfo**](docs/Api/OauthApi.md#getuserinfo) | **GET** /oauth2/userInfo | 获取用户信息
*OauthApi* | [**getUserInfo1**](docs/Api/OauthApi.md#getuserinfo1) | **POST** /oauth2/userInfo | 获取用户信息
*OperatorApi* | [**request**](docs/Api/OperatorApi.md#request) | **POST** /sw/api/v1/code/request | 请求下发验证码接口
*OperatorApi* | [**verify**](docs/Api/OperatorApi.md#verify) | **POST** /sw/api/v1/code/verify | 请求校验验证码接口

## Models

- [Balance](docs/Model/Balance.md)
- [CodeRequest](docs/Model/CodeRequest.md)
- [CodeResponse](docs/Model/CodeResponse.md)
- [CodeVerify](docs/Model/CodeVerify.md)
- [HttpEntity](docs/Model/HttpEntity.md)
- [OutResponseOfBalance](docs/Model/OutResponseOfBalance.md)
- [OutResponseOfCodeResponse](docs/Model/OutResponseOfCodeResponse.md)

## Authorization

### Authorization

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: 
    - **all**: All scope is trusted!

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

henryxm@163.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
