# Swagger\Client\MessengerApi

All URIs are relative to *https://api.avito.ru/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatRead**](MessengerApi.md#chatread) | **POST** /messenger/v1/accounts/{user_id}/chats/{chat_id}/read | Прочитать чат
[**deleteMessage**](MessengerApi.md#deletemessage) | **POST** /messenger/v1/accounts/{user_id}/chats/{chat_id}/messages/{message_id} | Удаление сообщения
[**getChatById**](MessengerApi.md#getchatbyid) | **GET** /messenger/v1/accounts/{user_id}/chats/{chat_id} | Получение информации по чату
[**getChats**](MessengerApi.md#getchats) | **GET** /messenger/v1/accounts/{user_id}/chats | Получение информации по чатам
[**getMessages**](MessengerApi.md#getmessages) | **GET** /messenger/v1/accounts/{user_id}/chats/{chat_id}/messages/ | Получение списка сообщений
[**getMessagesV2**](MessengerApi.md#getmessagesv2) | **GET** /messenger/v2/accounts/{user_id}/chats/{chat_id}/messages/ | Получение списка сообщений V2
[**postBlacklist**](MessengerApi.md#postblacklist) | **POST** /messenger/v1/accounts/{user_id}/blacklist | Добавление пользователя в blacklist
[**postSendMessage**](MessengerApi.md#postsendmessage) | **POST** /messenger/v1/accounts/{user_id}/chats/{chat_id}/messages | Отправление сообщения
[**postWebhook**](MessengerApi.md#postwebhook) | **POST** /messenger/v1/webhook | Включение уведомлений (webhooks)
[**postWebhookUnsubscribe**](MessengerApi.md#postwebhookunsubscribe) | **POST** /messenger/v1/webhook/unsubscribe | Отключение уведомлений (webhooks)
[**postWebhookV2**](MessengerApi.md#postwebhookv2) | **POST** /messenger/v2/webhook | Включение уведомлений V2 (webhooks)

# **chatRead**
> \Swagger\Client\Model\InlineResponse2001 chatRead($authorization, $user_id, $chat_id)

Прочитать чат

После успешного получения списка сообщений необходимо вызвать этот метод для того, чтобы чат стал прочитанным.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$chat_id = "chat_id_example"; // string | Идентификатор чата (клиента)

try {
    $result = $apiInstance->chatRead($authorization, $user_id, $chat_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->chatRead: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **chat_id** | **string**| Идентификатор чата (клиента) |

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteMessage**
> object deleteMessage($authorization, $user_id, $chat_id, $message_id)

Удаление сообщения

Сообщение не пропадает из истории, а меняет свой тип на deleted. Удалять можно только те сообщения которые не старше часа с момента их создания.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$chat_id = "chat_id_example"; // string | Идентификатор чата (клиента)
$message_id = "message_id_example"; // string | Идентификатор сообщения

try {
    $result = $apiInstance->deleteMessage($authorization, $user_id, $chat_id, $message_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->deleteMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **chat_id** | **string**| Идентификатор чата (клиента) |
 **message_id** | **string**| Идентификатор сообщения |

### Return type

**object**

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChatById**
> \Swagger\Client\Model\Chat getChatById($authorization, $user_id, $chat_id)

Получение информации по чату

Возвращает данные чата и последнее сообщение в нем

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$chat_id = "chat_id_example"; // string | Идентификатор чата (клиента)

try {
    $result = $apiInstance->getChatById($authorization, $user_id, $chat_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->getChatById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **chat_id** | **string**| Идентификатор чата (клиента) |

### Return type

[**\Swagger\Client\Model\Chat**](../Model/Chat.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChats**
> \Swagger\Client\Model\Chats getChats($authorization, $user_id, $item_ids, $unread_only, $limit, $offset)

Получение информации по чатам

Возвращает список чатов

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$item_ids = "item_ids_example"; // string | 
$unread_only = true; // bool | 
$limit = 100; // int | Количество сообщений на странице (положительное число больше 0 и меньше 100)
$offset = 0; // int | 

try {
    $result = $apiInstance->getChats($authorization, $user_id, $item_ids, $unread_only, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->getChats: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **item_ids** | **string**|  | [optional]
 **unread_only** | **bool**|  | [optional]
 **limit** | **int**| Количество сообщений на странице (положительное число больше 0 и меньше 100) | [optional] [default to 100]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\Chats**](../Model/Chats.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMessages**
> \Swagger\Client\Model\Messages getMessages($authorization, $user_id, $chat_id, $limit, $offset)

Получение списка сообщений

Получение списка сообщений, используйте только для изначальной загрузки сообщений на экране, для получения новых сообщений в реальном времени используйте webhooks

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$chat_id = "chat_id_example"; // string | Идентификатор чата (клиента)
$limit = 100; // int | Количество сообщений на странице (положительное число больше 0 и меньше 100)
$offset = 0; // int | 

try {
    $result = $apiInstance->getMessages($authorization, $user_id, $chat_id, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->getMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **chat_id** | **string**| Идентификатор чата (клиента) |
 **limit** | **int**| Количество сообщений на странице (положительное число больше 0 и меньше 100) | [optional] [default to 100]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\Messages**](../Model/Messages.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getMessagesV2**
> \Swagger\Client\Model\Messages getMessagesV2($authorization, $user_id, $chat_id, $limit, $offset)

Получение списка сообщений V2

Получение списка сообщений.  **Не помечает чат прочитанным** После успешного списка сообщений необходимо вызвать [метод](https://api.avito.ru/docs/api.html#operation/chatRead), который сделат чат прочитанным.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$chat_id = "chat_id_example"; // string | Идентификатор чата (клиента)
$limit = 100; // int | Количество сообщений на странице (положительное число больше 0 и меньше 100)
$offset = 0; // int | 

try {
    $result = $apiInstance->getMessagesV2($authorization, $user_id, $chat_id, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->getMessagesV2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **chat_id** | **string**| Идентификатор чата (клиента) |
 **limit** | **int**| Количество сообщений на странице (положительное число больше 0 и меньше 100) | [optional] [default to 100]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\Messages**](../Model/Messages.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postBlacklist**
> postBlacklist($authorization, $user_id, $body)

Добавление пользователя в blacklist

Добавление пользователя в blacklist

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$body = new \Swagger\Client\Model\AddBlacklistRequestBody(); // \Swagger\Client\Model\AddBlacklistRequestBody | Добавление пользователя в blacklist

try {
    $apiInstance->postBlacklist($authorization, $user_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->postBlacklist: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **body** | [**\Swagger\Client\Model\AddBlacklistRequestBody**](../Model/AddBlacklistRequestBody.md)| Добавление пользователя в blacklist | [optional]

### Return type

void (empty response body)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postSendMessage**
> \Swagger\Client\Model\InlineResponse200 postSendMessage($authorization, $user_id, $chat_id, $body)

Отправление сообщения

На данный момент можно отправить только текстовое сообщение

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$user_id = 789; // int | Идентификатор пользователя (клиента)
$chat_id = "chat_id_example"; // string | Идентификатор чата (клиента)
$body = new \Swagger\Client\Model\SendMessageRequestBody(); // \Swagger\Client\Model\SendMessageRequestBody | Отправление сообщения

try {
    $result = $apiInstance->postSendMessage($authorization, $user_id, $chat_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->postSendMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **user_id** | **int**| Идентификатор пользователя (клиента) |
 **chat_id** | **string**| Идентификатор чата (клиента) |
 **body** | [**\Swagger\Client\Model\SendMessageRequestBody**](../Model/SendMessageRequestBody.md)| Отправление сообщения | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postWebhook**
> \Swagger\Client\Model\InlineResponse2001 postWebhook($authorization, $body)

Включение уведомлений (webhooks)

Включение уведомлений

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$body = new \Swagger\Client\Model\WebhookSubscribeRequestBody(); // \Swagger\Client\Model\WebhookSubscribeRequestBody | Url на который будут отправляться уведомления

try {
    $result = $apiInstance->postWebhook($authorization, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->postWebhook: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **body** | [**\Swagger\Client\Model\WebhookSubscribeRequestBody**](../Model/WebhookSubscribeRequestBody.md)| Url на который будут отправляться уведомления | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postWebhookUnsubscribe**
> \Swagger\Client\Model\InlineResponse2001 postWebhookUnsubscribe($authorization, $body)

Отключение уведомлений (webhooks)

Отключение уведомлений

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$body = new \Swagger\Client\Model\WebhookSubscribeRequestBody(); // \Swagger\Client\Model\WebhookSubscribeRequestBody | Url, на который необходимо перестать слать уведомления

try {
    $result = $apiInstance->postWebhookUnsubscribe($authorization, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->postWebhookUnsubscribe: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **body** | [**\Swagger\Client\Model\WebhookSubscribeRequestBody**](../Model/WebhookSubscribeRequestBody.md)| Url, на который необходимо перестать слать уведомления | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postWebhookV2**
> \Swagger\Client\Model\InlineResponse2001 postWebhookV2($authorization, $body)

Включение уведомлений V2 (webhooks)

Включение **V2** уведомлений. <LINK_TO_V2_WEBHOOKS>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: AuthorizationCode
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');
// Configure OAuth2 access token for authorization: ClientCredentials
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\MessengerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | Токен для авторизации
$body = new \Swagger\Client\Model\WebhookSubscribeRequestBody(); // \Swagger\Client\Model\WebhookSubscribeRequestBody | Url на который будут отправляться уведомления

try {
    $result = $apiInstance->postWebhookV2($authorization, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessengerApi->postWebhookV2: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| Токен для авторизации |
 **body** | [**\Swagger\Client\Model\WebhookSubscribeRequestBody**](../Model/WebhookSubscribeRequestBody.md)| Url на который будут отправляться уведомления | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[AuthorizationCode](../../README.md#AuthorizationCode), [ClientCredentials](../../README.md#ClientCredentials)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

