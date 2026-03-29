# asaas.ConfiguraesDeWebhooksApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**atualizar_webhook_existente**](ConfiguraesDeWebhooksApi.md#atualizar_webhook_existente) | **PUT** /v3/webhooks/{id} | Atualizar webhook existente
[**criar_novo_webhook**](ConfiguraesDeWebhooksApi.md#criar_novo_webhook) | **POST** /v3/webhooks | Criar novo webhook
[**listar_webhooks**](ConfiguraesDeWebhooksApi.md#listar_webhooks) | **GET** /v3/webhooks | Listar webhooks
[**recuperar_um_unico_webhook**](ConfiguraesDeWebhooksApi.md#recuperar_um_unico_webhook) | **GET** /v3/webhooks/{id} | Recuperar um único webhook
[**remover_penalizacao_webhook**](ConfiguraesDeWebhooksApi.md#remover_penalizacao_webhook) | **POST** /v3/webhooks/{id}/removeBackoff | Remover penalização de webhook
[**remover_webhook**](ConfiguraesDeWebhooksApi.md#remover_webhook) | **DELETE** /v3/webhooks/{id} | Remover um webhook


# **atualizar_webhook_existente**
> WebhookConfigGetResponseDTO atualizar_webhook_existente(id, webhook_config_update_request_dto=webhook_config_update_request_dto)

Atualizar webhook existente

Utilize este endpoint para atualizar informações de um webhook já cadastrado.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.webhook_config_get_response_dto import WebhookConfigGetResponseDTO
from asaas.models.webhook_config_update_request_dto import WebhookConfigUpdateRequestDTO
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.ConfiguraesDeWebhooksApi(api_client)
    id = 'bbf67496-1379-4b6d-a348-fd5fa229f1c' # str | Identificador único do Webhook
    webhook_config_update_request_dto = asaas.WebhookConfigUpdateRequestDTO() # WebhookConfigUpdateRequestDTO |  (optional)

    try:
        # Atualizar webhook existente
        api_response = api_instance.atualizar_webhook_existente(id, webhook_config_update_request_dto=webhook_config_update_request_dto)
        print("The response of ConfiguraesDeWebhooksApi->atualizar_webhook_existente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConfiguraesDeWebhooksApi->atualizar_webhook_existente: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único do Webhook | 
 **webhook_config_update_request_dto** | [**WebhookConfigUpdateRequestDTO**](WebhookConfigUpdateRequestDTO.md)|  | [optional] 

### Return type

[**WebhookConfigGetResponseDTO**](WebhookConfigGetResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**404** | Not found |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **criar_novo_webhook**
> WebhookConfigGetResponseDTO criar_novo_webhook(webhook_config_save_request_dto=webhook_config_save_request_dto)

Criar novo webhook



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.webhook_config_get_response_dto import WebhookConfigGetResponseDTO
from asaas.models.webhook_config_save_request_dto import WebhookConfigSaveRequestDTO
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.ConfiguraesDeWebhooksApi(api_client)
    webhook_config_save_request_dto = asaas.WebhookConfigSaveRequestDTO() # WebhookConfigSaveRequestDTO |  (optional)

    try:
        # Criar novo webhook
        api_response = api_instance.criar_novo_webhook(webhook_config_save_request_dto=webhook_config_save_request_dto)
        print("The response of ConfiguraesDeWebhooksApi->criar_novo_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConfiguraesDeWebhooksApi->criar_novo_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_config_save_request_dto** | [**WebhookConfigSaveRequestDTO**](WebhookConfigSaveRequestDTO.md)|  | [optional] 

### Return type

[**WebhookConfigGetResponseDTO**](WebhookConfigGetResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listar_webhooks**
> WebhookConfigListResponseDTO listar_webhooks(offset=offset, limit=limit)

Listar webhooks

Endpoint para listar todos os Webhooks cadastrados na sua conta.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.webhook_config_list_response_dto import WebhookConfigListResponseDTO
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.ConfiguraesDeWebhooksApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)

    try:
        # Listar webhooks
        api_response = api_instance.listar_webhooks(offset=offset, limit=limit)
        print("The response of ConfiguraesDeWebhooksApi->listar_webhooks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConfiguraesDeWebhooksApi->listar_webhooks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 

### Return type

[**WebhookConfigListResponseDTO**](WebhookConfigListResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **recuperar_um_unico_webhook**
> WebhookConfigGetResponseDTO recuperar_um_unico_webhook(id)

Recuperar um único webhook

Este endpoint recupera um único webhook de acordo com o ID informado.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.webhook_config_get_response_dto import WebhookConfigGetResponseDTO
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.ConfiguraesDeWebhooksApi(api_client)
    id = 'bbf67496-1379-4b6d-a348-fd5fa229f1c' # str | Identificador único do webhook

    try:
        # Recuperar um único webhook
        api_response = api_instance.recuperar_um_unico_webhook(id)
        print("The response of ConfiguraesDeWebhooksApi->recuperar_um_unico_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConfiguraesDeWebhooksApi->recuperar_um_unico_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único do webhook | 

### Return type

[**WebhookConfigGetResponseDTO**](WebhookConfigGetResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. |  -  |
**404** | Not found |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remover_penalizacao_webhook**
> remover_penalizacao_webhook(id, body=body)

Remover penalização de webhook

Utilize este endpoint para remover a penalização de todos os webhooks penalizados de uma configuração.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.ConfiguraesDeWebhooksApi(api_client)
    id = 'bbf67496-1379-4b6d-a348-fd5fa229f1ca' # str | Identificador único da configuração de webhook
    body = None # object |  (optional)

    try:
        # Remover penalização de webhook
        api_instance.remover_penalizacao_webhook(id, body=body)
    except Exception as e:
        print("Exception when calling ConfiguraesDeWebhooksApi->remover_penalizacao_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da configuração de webhook | 
 **body** | **object**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | No Content |  -  |
**401** | Unauthorized |  -  |
**404** | Not found |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remover_webhook**
> WebhookConfigDeleteResponseDTO remover_webhook(id)

Remover um webhook

Este endpoint remove um webhook.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.webhook_config_delete_response_dto import WebhookConfigDeleteResponseDTO
from asaas.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api-sandbox.asaas.com
# See configuration.py for a list of all supported configuration parameters.
configuration = asaas.Configuration(
    host = "https://api-sandbox.asaas.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: Authorization
configuration.api_key['Authorization'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# Enter a context with an instance of the API client
with asaas.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = asaas.ConfiguraesDeWebhooksApi(api_client)
    id = 'bbf67496-1379-4b6d-a348-fd5fa229f1c' # str | Identificador único do webhook

    try:
        # Remover um webhook
        api_response = api_instance.remover_webhook(id)
        print("The response of ConfiguraesDeWebhooksApi->remover_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConfiguraesDeWebhooksApi->remover_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único do webhook | 

### Return type

[**WebhookConfigDeleteResponseDTO**](WebhookConfigDeleteResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**404** | Not found |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

