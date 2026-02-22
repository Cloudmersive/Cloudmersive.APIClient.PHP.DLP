# cloudmersive_dlp_api_client
Easily and directly scan and detect sensitive data (PII) in input text.

[Cloudmersive DLP API](https://cloudmersive.com/dlp-data-loss-prevention-api) allows you to scan input for Personally Identifiable Information (PII), Personal Health Information (PHI), Personal Financial Information and other types of sensitive data.  Advanced AI is used to both detect and redact with next-generation accuracy.

- API version: v1
- Package version: 3.0.0


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
      "url": "https://github.com/cloudmersive/cloudmersive_dlp_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_dlp_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_dlp_api_client/vendor/autoload.php');
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

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DetectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpDocumentDetectionRequest(); // \Swagger\Client\Model\DlpDocumentDetectionRequest | Input request

try {
    $result = $apiInstance->detectDocument($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DetectApi->detectDocument: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DetectApi* | [**detectDocument**](docs/Api/DetectApi.md#detectdocument) | **POST** /dlp/detect/document | Detect User Data in Document Image
*DetectApi* | [**detectDocumentAdvanced**](docs/Api/DetectApi.md#detectdocumentadvanced) | **POST** /dlp/detect/document/advanced | Detect User Data in Document Image (Advanced)
*DetectApi* | [**detectText**](docs/Api/DetectApi.md#detecttext) | **POST** /dlp/detect/text | Detect User Data in Input Text
*DetectApi* | [**detectTextAdvanced**](docs/Api/DetectApi.md#detecttextadvanced) | **POST** /dlp/detect/text/advanced | Detect User Data in Input Text (Advanced)
*RedactApi* | [**redactDocument**](docs/Api/RedactApi.md#redactdocument) | **POST** /dlp/redact/document | Redact User Data in Document
*RedactApi* | [**redactDocumentAdvanced**](docs/Api/RedactApi.md#redactdocumentadvanced) | **POST** /dlp/redact/document/advanced | Redact User Data in Document (Advanced)
*RedactApi* | [**redactText**](docs/Api/RedactApi.md#redacttext) | **POST** /dlp/redact/text | Redact User Data in Input Text
*RedactApi* | [**redactTextAdvanced**](docs/Api/RedactApi.md#redacttextadvanced) | **POST** /dlp/redact/text/advanced | Redact User Data in Input Text (Advanced)


## Documentation For Models

 - [DlpAdvancedDetectionRequest](docs/Model/DlpAdvancedDetectionRequest.md)
 - [DlpAdvancedDetectionResponse](docs/Model/DlpAdvancedDetectionResponse.md)
 - [DlpAdvancedDocumentDetectionRequest](docs/Model/DlpAdvancedDocumentDetectionRequest.md)
 - [DlpAdvancedDocumentRedactionRequest](docs/Model/DlpAdvancedDocumentRedactionRequest.md)
 - [DlpAdvancedDocumentRedactionResponse](docs/Model/DlpAdvancedDocumentRedactionResponse.md)
 - [DlpAdvancedRedactionRequest](docs/Model/DlpAdvancedRedactionRequest.md)
 - [DlpAdvancedRedactionResponse](docs/Model/DlpAdvancedRedactionResponse.md)
 - [DlpDetectionRequest](docs/Model/DlpDetectionRequest.md)
 - [DlpDetectionResponse](docs/Model/DlpDetectionResponse.md)
 - [DlpDocumentDetectionRequest](docs/Model/DlpDocumentDetectionRequest.md)
 - [DlpDocumentRedactionRequest](docs/Model/DlpDocumentRedactionRequest.md)
 - [DlpDocumentRedactionResponse](docs/Model/DlpDocumentRedactionResponse.md)
 - [DlpRedactionRequest](docs/Model/DlpRedactionRequest.md)
 - [DlpRedactionResponse](docs/Model/DlpRedactionResponse.md)
 - [RedactedPageInfo](docs/Model/RedactedPageInfo.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




