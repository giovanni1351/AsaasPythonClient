# asaas.NotificaesApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**atualizar_notificacao_existente**](NotificaesApi.md#atualizar_notificacao_existente) | **PUT** /v3/notifications/{id} | Atualizar notificação existente
[**atualizar_notificacoes_existentes_em_lote**](NotificaesApi.md#atualizar_notificacoes_existentes_em_lote) | **PUT** /v3/notifications/batch | Atualizar notificações existentes em lote


# **atualizar_notificacao_existente**
> NotificationGetResponseDTO atualizar_notificacao_existente(id, notification_update_request_dto=notification_update_request_dto)

Atualizar notificação existente



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.notification_get_response_dto import NotificationGetResponseDTO
from asaas.models.notification_update_request_dto import NotificationUpdateRequestDTO
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
    api_instance = asaas.NotificaesApi(api_client)
    id = 'not_wuGp97JeCr7G' # str | Identificador único da notificação a ser atualizada
    notification_update_request_dto = asaas.NotificationUpdateRequestDTO() # NotificationUpdateRequestDTO |  (optional)

    try:
        # Atualizar notificação existente
        api_response = api_instance.atualizar_notificacao_existente(id, notification_update_request_dto=notification_update_request_dto)
        print("The response of NotificaesApi->atualizar_notificacao_existente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotificaesApi->atualizar_notificacao_existente: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da notificação a ser atualizada | 
 **notification_update_request_dto** | [**NotificationUpdateRequestDTO**](NotificationUpdateRequestDTO.md)|  | [optional] 

### Return type

[**NotificationGetResponseDTO**](NotificationGetResponseDTO.md)

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

# **atualizar_notificacoes_existentes_em_lote**
> NotificationBatchUpdateResponseDTO atualizar_notificacoes_existentes_em_lote(notification_batch_update_request_dto=notification_batch_update_request_dto)

Atualizar notificações existentes em lote

É possível personalizar várias notificações, independente do canal de comunicação que utilizar (email, SMS e voz) e quem deve receber a notificação(você e/ou seu cliente) enviando qual o id do cliente e as notificações a serem atualizadas.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.notification_batch_update_request_dto import NotificationBatchUpdateRequestDTO
from asaas.models.notification_batch_update_response_dto import NotificationBatchUpdateResponseDTO
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
    api_instance = asaas.NotificaesApi(api_client)
    notification_batch_update_request_dto = asaas.NotificationBatchUpdateRequestDTO() # NotificationBatchUpdateRequestDTO |  (optional)

    try:
        # Atualizar notificações existentes em lote
        api_response = api_instance.atualizar_notificacoes_existentes_em_lote(notification_batch_update_request_dto=notification_batch_update_request_dto)
        print("The response of NotificaesApi->atualizar_notificacoes_existentes_em_lote:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotificaesApi->atualizar_notificacoes_existentes_em_lote: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **notification_batch_update_request_dto** | [**NotificationBatchUpdateRequestDTO**](NotificationBatchUpdateRequestDTO.md)|  | [optional] 

### Return type

[**NotificationBatchUpdateResponseDTO**](NotificationBatchUpdateResponseDTO.md)

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

