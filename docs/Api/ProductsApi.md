# Swagger\Client\ProductsApi

All URIs are relative to *https://api.facestore.pt/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addProduct**](ProductsApi.md#addProduct) | **POST** /products | 
[**deleteProductById**](ProductsApi.md#deleteProductById) | **DELETE** /products/{id}/ | 
[**getProductById**](ProductsApi.md#getProductById) | **GET** /products/{id}/ | 
[**getProducts**](ProductsApi.md#getProducts) | **GET** /products | 
[**updateProductById**](ProductsApi.md#updateProductById) | **PUT** /products/{id}/ | 
[**updateProductById_0**](ProductsApi.md#updateProductById_0) | **PATCH** /products/{id}/ | 
[**uploadImages**](ProductsApi.md#uploadImages) | **POST** /products/{id}/uploads/ | Upload de images for product


# **addProduct**
> \Swagger\Client\Model\InlineResponse2014 addProduct($product)



Creates a new product in the store.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product = new \Swagger\Client\Model\Product(); // \Swagger\Client\Model\Product | Product to add to the store

try {
    $result = $apiInstance->addProduct($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->addProduct: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product** | [**\Swagger\Client\Model\Product**](../Model/Product.md)| Product to add to the store |

### Return type

[**\Swagger\Client\Model\InlineResponse2014**](../Model/InlineResponse2014.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteProductById**
> deleteProductById($id)



deletes a single product based on the ID supplied

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of product to delete

try {
    $apiInstance->deleteProductById($id);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->deleteProductById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of product to delete |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProductById**
> \Swagger\Client\Model\InlineResponse2014 getProductById($id, $includes, $limit)



Returns a product based on a single ID  ### Includes You can give the following values on includes parameter: `brands, categories, routes, stocks`

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of product to fetch
$includes = array("includes_example"); // string[] | Include associated objects within response
$limit = 56; // int | max records to return

try {
    $result = $apiInstance->getProductById($id, $includes, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->getProductById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of product to fetch |
 **includes** | [**string[]**](../Model/string.md)| Include associated objects within response | [optional]
 **limit** | **int**| max records to return | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2014**](../Model/InlineResponse2014.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getProducts**
> \Swagger\Client\Model\InlineResponse2008 getProducts($includes, $limit, $order_by)



Returns all products from the system that the user has access to  ### Includes You can give the following values on includes parameter: `brands, categories, routes, stocks`

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$includes = array("includes_example"); // string[] | Include associated objects within response
$limit = 56; // int | max records to return
$order_by = array("order_by_example"); // string[] | Specify the field to be sorted, examples:  - `?order_by=id|desc` - `?order_by=updated_at|desc,position|asc`

try {
    $result = $apiInstance->getProducts($includes, $limit, $order_by);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->getProducts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **includes** | [**string[]**](../Model/string.md)| Include associated objects within response | [optional]
 **limit** | **int**| max records to return | [optional]
 **order_by** | [**string[]**](../Model/string.md)| Specify the field to be sorted, examples:  - &#x60;?order_by&#x3D;id|desc&#x60; - &#x60;?order_by&#x3D;updated_at|desc,position|asc&#x60; | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2008**](../Model/InlineResponse2008.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateProductById**
> updateProductById($id, $tax)



update a single product based on the ID supplied

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of product to update
$tax = new \Swagger\Client\Model\Product(); // \Swagger\Client\Model\Product | Product to add to the store

try {
    $apiInstance->updateProductById($id, $tax);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->updateProductById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of product to update |
 **tax** | [**\Swagger\Client\Model\Product**](../Model/Product.md)| Product to add to the store |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateProductById_0**
> updateProductById_0($id, $tax)



update a single product based on the ID supplied

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of product to update
$tax = new \Swagger\Client\Model\Product(); // \Swagger\Client\Model\Product | Product to add to the store

try {
    $apiInstance->updateProductById_0($id, $tax);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->updateProductById_0: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of product to update |
 **tax** | [**\Swagger\Client\Model\Product**](../Model/Product.md)| Product to add to the store |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **uploadImages**
> uploadImages($id, $files)

Upload de images for product

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('APIToken', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('APIToken', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of product to update
$files = "/path/to/file.txt"; // \SplFileObject | File for product

try {
    $apiInstance->uploadImages($id, $files);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->uploadImages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of product to update |
 **files** | **\SplFileObject**| File for product | [optional]

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

