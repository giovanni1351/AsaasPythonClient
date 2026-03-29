# asaas.ClientesApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                          | HTTP request                             | Description                          |
| ----------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------------------------ |
| [**atualizar_cliente_existente**](ClientesApi.md#atualizar_cliente_existente)                   | **PUT** /v3/customers/{id}               | Atualizar cliente existente          |
| [**criar_novo_cliente**](ClientesApi.md#criar_novo_cliente)                                     | **POST** /v3/customers                   | Criar novo cliente                   |
| [**listar_clientes**](ClientesApi.md#listar_clientes)                                           | **GET** /v3/customers                    | Listar clientes                      |
| [**recuperar_notificacoes_de_um_cliente**](ClientesApi.md#recuperar_notificacoes_de_um_cliente) | **GET** /v3/customers/{id}/notifications | Recuperar notificações de um cliente |
| [**recuperar_um_unico_cliente**](ClientesApi.md#recuperar_um_unico_cliente)                     | **GET** /v3/customers/{id}               | Recuperar um único cliente           |
| [**remover_cliente**](ClientesApi.md#remover_cliente)                                           | **DELETE** /v3/customers/{id}            | Remover cliente                      |
| [**restaurar_cliente_removido**](ClientesApi.md#restaurar_cliente_removido)                     | **POST** /v3/customers/{id}/restore      | Restaurar cliente removido           |

# **atualizar_cliente_existente**

> CustomerGetResponseDTO atualizar_cliente_existente(id, customer_update_request_dto=customer_update_request_dto)

Atualizar cliente existente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_get_response_dto import CustomerGetResponseDTO
from asaas.models.customer_update_request_dto import CustomerUpdateRequestDTO
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
    api_instance = asaas.ClientesApi(api_client)
    id = 'cus_000005401844' # str | Identificador único do cliente a ser atualizado
    customer_update_request_dto = asaas.CustomerUpdateRequestDTO() # CustomerUpdateRequestDTO |  (optional)

    try:
        # Atualizar cliente existente
        api_response = api_instance.atualizar_cliente_existente(id, customer_update_request_dto=customer_update_request_dto)
        print("The response of ClientesApi->atualizar_cliente_existente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->atualizar_cliente_existente: %s\n" % e)
```

### Parameters

| Name                            | Type                                                        | Description                                     | Notes      |
| ------------------------------- | ----------------------------------------------------------- | ----------------------------------------------- | ---------- |
| **id**                          | **str**                                                     | Identificador único do cliente a ser atualizado |
| **customer_update_request_dto** | [**CustomerUpdateRequestDTO**](CustomerUpdateRequestDTO.md) |                                                 | [optional] |

### Return type

[**CustomerGetResponseDTO**](CustomerGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **criar_novo_cliente**

> CustomerGetResponseDTO criar_novo_cliente(customer_save_request_dto=customer_save_request_dto)

Criar novo cliente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_get_response_dto import CustomerGetResponseDTO
from asaas.models.customer_save_request_dto import CustomerSaveRequestDTO
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
    api_instance = asaas.ClientesApi(api_client)
    customer_save_request_dto = asaas.CustomerSaveRequestDTO() # CustomerSaveRequestDTO |  (optional)

    try:
        # Criar novo cliente
        api_response = api_instance.criar_novo_cliente(customer_save_request_dto=customer_save_request_dto)
        print("The response of ClientesApi->criar_novo_cliente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->criar_novo_cliente: %s\n" % e)
```

### Parameters

| Name                          | Type                                                    | Description | Notes      |
| ----------------------------- | ------------------------------------------------------- | ----------- | ---------- |
| **customer_save_request_dto** | [**CustomerSaveRequestDTO**](CustomerSaveRequestDTO.md) |             | [optional] |

### Return type

[**CustomerGetResponseDTO**](CustomerGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **listar_clientes**

> CustomerListResponseDTO listar_clientes(offset=offset, limit=limit, name=name, email=email, cpf_cnpj=cpf_cnpj, group_name=group_name, external_reference=external_reference)

Listar clientes

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_list_response_dto import CustomerListResponseDTO
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
    api_instance = asaas.ClientesApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    name = 'John Doe' # str | Filtrar por nome (optional)
    email = 'john.doe@asaas.com.br' # str | Filtrar por email (optional)
    cpf_cnpj = '24971563792' # str | Filtrar por CPF ou CNPJ (optional)
    group_name = 'group_name_example' # str | Filtrar por grupo (optional)
    external_reference = 'external_reference_example' # str | Filtrar pelo Identificador do seu sistema (optional)

    try:
        # Listar clientes
        api_response = api_instance.listar_clientes(offset=offset, limit=limit, name=name, email=email, cpf_cnpj=cpf_cnpj, group_name=group_name, external_reference=external_reference)
        print("The response of ClientesApi->listar_clientes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->listar_clientes: %s\n" % e)
```

### Parameters

| Name                   | Type    | Description                               | Notes      |
| ---------------------- | ------- | ----------------------------------------- | ---------- |
| **offset**             | **int** | Elemento inicial da lista                 | [optional] |
| **limit**              | **int** | Número de elementos da lista (max: 100)   | [optional] |
| **name**               | **str** | Filtrar por nome                          | [optional] |
| **email**              | **str** | Filtrar por email                         | [optional] |
| **cpf_cnpj**           | **str** | Filtrar por CPF ou CNPJ                   | [optional] |
| **group_name**         | **str** | Filtrar por grupo                         | [optional] |
| **external_reference** | **str** | Filtrar pelo Identificador do seu sistema | [optional] |

### Return type

[**CustomerListResponseDTO**](CustomerListResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_notificacoes_de_um_cliente**

> NotificationListResponseDTO recuperar_notificacoes_de_um_cliente(id)

Recuperar notificações de um cliente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.notification_list_response_dto import NotificationListResponseDTO
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
    api_instance = asaas.ClientesApi(api_client)
    id = 'cus_000005401844' # str | Identificador único do cliente no Asaas

    try:
        # Recuperar notificações de um cliente
        api_response = api_instance.recuperar_notificacoes_de_um_cliente(id)
        print("The response of ClientesApi->recuperar_notificacoes_de_um_cliente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->recuperar_notificacoes_de_um_cliente: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                             | Notes |
| ------ | ------- | --------------------------------------- | ----- |
| **id** | **str** | Identificador único do cliente no Asaas |

### Return type

[**NotificationListResponseDTO**](NotificationListResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_um_unico_cliente**

> CustomerGetResponseDTO recuperar_um_unico_cliente(id)

Recuperar um único cliente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_get_response_dto import CustomerGetResponseDTO
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
    api_instance = asaas.ClientesApi(api_client)
    id = 'cus_000005401844' # str | Identificador único do cliente no Asaas

    try:
        # Recuperar um único cliente
        api_response = api_instance.recuperar_um_unico_cliente(id)
        print("The response of ClientesApi->recuperar_um_unico_cliente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->recuperar_um_unico_cliente: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                             | Notes |
| ------ | ------- | --------------------------------------- | ----- |
| **id** | **str** | Identificador único do cliente no Asaas |

### Return type

[**CustomerGetResponseDTO**](CustomerGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **remover_cliente**

> CustomerDeleteResponseDTO remover_cliente(id)

Remover cliente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_delete_response_dto import CustomerDeleteResponseDTO
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
    api_instance = asaas.ClientesApi(api_client)
    id = 'cus_000005401844' # str | Identificador único do cliente a ser removido.

    try:
        # Remover cliente
        api_response = api_instance.remover_cliente(id)
        print("The response of ClientesApi->remover_cliente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->remover_cliente: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                    | Notes |
| ------ | ------- | ---------------------------------------------- | ----- |
| **id** | **str** | Identificador único do cliente a ser removido. |

### Return type

[**CustomerDeleteResponseDTO**](CustomerDeleteResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **restaurar_cliente_removido**

> CustomerGetResponseDTO restaurar_cliente_removido(id, body=body)

Restaurar cliente removido

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_get_response_dto import CustomerGetResponseDTO
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
    api_instance = asaas.ClientesApi(api_client)
    id = 'cus_000005401844' # str | Identificador único do cliente a ser restaurado.
    body = None # object |  (optional)

    try:
        # Restaurar cliente removido
        api_response = api_instance.restaurar_cliente_removido(id, body=body)
        print("The response of ClientesApi->restaurar_cliente_removido:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClientesApi->restaurar_cliente_removido: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                                      | Notes      |
| -------- | ---------- | ------------------------------------------------ | ---------- |
| **id**   | **str**    | Identificador único do cliente a ser restaurado. |
| **body** | **object** |                                                  | [optional] |

### Return type

[**CustomerGetResponseDTO**](CustomerGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)
