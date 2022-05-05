# SwaggerClient-php
API Мессенджера - набор методов для получения списка чатов пользователя на Авито, получения сообщений в чате, отправки сообщения в чат и другие Через API Мессенджера можно организовать интеграцию между мессенджером Авито и сторонней системой в обе стороны  **Авито API для бизнеса предоставляется согласно [Условиям использования](https://api.avito.ru/docs/public/APITermsOfServiceV1.pdf).**

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1
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
    require_once('vendor/autoload.php');
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

## Documentation for API Endpoints

All URIs are relative to *https://api.avito.ru/*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*MessengerApi* | [**chatRead**](docs/Api/MessengerApi.md#chatread) | **POST** /messenger/v1/accounts/{user_id}/chats/{chat_id}/read | Прочитать чат
*MessengerApi* | [**deleteMessage**](docs/Api/MessengerApi.md#deletemessage) | **POST** /messenger/v1/accounts/{user_id}/chats/{chat_id}/messages/{message_id} | Удаление сообщения
*MessengerApi* | [**getChatById**](docs/Api/MessengerApi.md#getchatbyid) | **GET** /messenger/v1/accounts/{user_id}/chats/{chat_id} | Получение информации по чату
*MessengerApi* | [**getChats**](docs/Api/MessengerApi.md#getchats) | **GET** /messenger/v1/accounts/{user_id}/chats | Получение информации по чатам
*MessengerApi* | [**getMessages**](docs/Api/MessengerApi.md#getmessages) | **GET** /messenger/v1/accounts/{user_id}/chats/{chat_id}/messages/ | Получение списка сообщений
*MessengerApi* | [**getMessagesV2**](docs/Api/MessengerApi.md#getmessagesv2) | **GET** /messenger/v2/accounts/{user_id}/chats/{chat_id}/messages/ | Получение списка сообщений V2
*MessengerApi* | [**postBlacklist**](docs/Api/MessengerApi.md#postblacklist) | **POST** /messenger/v1/accounts/{user_id}/blacklist | Добавление пользователя в blacklist
*MessengerApi* | [**postSendMessage**](docs/Api/MessengerApi.md#postsendmessage) | **POST** /messenger/v1/accounts/{user_id}/chats/{chat_id}/messages | Отправление сообщения
*MessengerApi* | [**postWebhook**](docs/Api/MessengerApi.md#postwebhook) | **POST** /messenger/v1/webhook | Включение уведомлений (webhooks)
*MessengerApi* | [**postWebhookUnsubscribe**](docs/Api/MessengerApi.md#postwebhookunsubscribe) | **POST** /messenger/v1/webhook/unsubscribe | Отключение уведомлений (webhooks)
*MessengerApi* | [**postWebhookV2**](docs/Api/MessengerApi.md#postwebhookv2) | **POST** /messenger/v2/webhook | Включение уведомлений V2 (webhooks)

## Documentation For Models

 - [AddBlacklistRequestBody](docs/Model/AddBlacklistRequestBody.md)
 - [AddBlacklistRequestBodyContext](docs/Model/AddBlacklistRequestBodyContext.md)
 - [AddBlacklistRequestBodyUsers](docs/Model/AddBlacklistRequestBodyUsers.md)
 - [AuthError](docs/Model/AuthError.md)
 - [AuthErrorError](docs/Model/AuthErrorError.md)
 - [BadRequestError](docs/Model/BadRequestError.md)
 - [BadRequestErrorError](docs/Model/BadRequestErrorError.md)
 - [Chat](docs/Model/Chat.md)
 - [ChatContext](docs/Model/ChatContext.md)
 - [ChatContextValue](docs/Model/ChatContextValue.md)
 - [ChatContextValueImages](docs/Model/ChatContextValueImages.md)
 - [ChatContextValueImagesMain](docs/Model/ChatContextValueImagesMain.md)
 - [ChatLastMessage](docs/Model/ChatLastMessage.md)
 - [ChatLastMessageContent](docs/Model/ChatLastMessageContent.md)
 - [ChatLastMessageContentLink](docs/Model/ChatLastMessageContentLink.md)
 - [ChatPublicUserProfile](docs/Model/ChatPublicUserProfile.md)
 - [ChatPublicUserProfileAvatar](docs/Model/ChatPublicUserProfileAvatar.md)
 - [ChatPublicUserProfileAvatarImages](docs/Model/ChatPublicUserProfileAvatarImages.md)
 - [ChatUsers](docs/Model/ChatUsers.md)
 - [Chats](docs/Model/Chats.md)
 - [ForbiddenError](docs/Model/ForbiddenError.md)
 - [ForbiddenErrorError](docs/Model/ForbiddenErrorError.md)
 - [InlineResponse200](docs/Model/InlineResponse200.md)
 - [InlineResponse2001](docs/Model/InlineResponse2001.md)
 - [InlineResponse200Content](docs/Model/InlineResponse200Content.md)
 - [Messages](docs/Model/Messages.md)
 - [MessagesInner](docs/Model/MessagesInner.md)
 - [NotFoundError](docs/Model/NotFoundError.md)
 - [NotFoundErrorError](docs/Model/NotFoundErrorError.md)
 - [PurchasingError](docs/Model/PurchasingError.md)
 - [PurchasingErrorError](docs/Model/PurchasingErrorError.md)
 - [SendMessageRequestBody](docs/Model/SendMessageRequestBody.md)
 - [SendMessageRequestBodyMessage](docs/Model/SendMessageRequestBodyMessage.md)
 - [ServiceError](docs/Model/ServiceError.md)
 - [ServiceErrorError](docs/Model/ServiceErrorError.md)
 - [ServiceUnavailableError](docs/Model/ServiceUnavailableError.md)
 - [ServiceUnavailableErrorError](docs/Model/ServiceUnavailableErrorError.md)
 - [ValidatingError](docs/Model/ValidatingError.md)
 - [ValidatingErrorError](docs/Model/ValidatingErrorError.md)
 - [WebhookSubscribeRequestBody](docs/Model/WebhookSubscribeRequestBody.md)

## Documentation For Authorization


## AuthorizationCode

- **Type**: OAuth
- **Flow**: accessCode
- **Authorization URL**: https://avito.ru/oauth
- **Scopes**: 
 - **autoload:reports**: Получение отчетов Автозагрузки
 - **items:apply_vas**: Применение дополнительных услуг
 - **items:info**: Получение информации об объявлениях
 - **job:cv**: Получение информации резюме
 - **job:negotiations**: Получение информации об откликах на вакансии
 - **job:write**: Изменение объявлений вертикали Работа
 - **messenger:read**: Чтение сообщений в мессенджере Авито
 - **messenger:write**: Модифицирование сообщений в мессенджере Авито
 - **short_term_rent:read**: Получение информации об объявлениях краткосрочной аренды
 - **short_term_rent:write**: Изменение объявлений краткосрочной аренды
 - **stats:read**: Получение статистики объявлений
 - **user:read**: Получение информации о пользователе
 - **user_balance:read**: Получение баланса пользователя
 - **user_operations:read**: Получение истории операций пользователя

## ClientCredentials

- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 


## Author

supportautoload@avito.ru

