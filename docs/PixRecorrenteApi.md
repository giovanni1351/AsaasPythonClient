# asaas.PixRecorrenteApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                       | HTTP request                                               | Description                      |
| -------------------------------------------------------------------------------------------- | ---------------------------------------------------------- | -------------------------------- |
| [**cancelar_item_de_uma_recorrencia**](PixRecorrenteApi.md#cancelar_item_de_uma_recorrencia) | **POST** /v3/pix/transactions/recurrings/items/{id}/cancel | Cancelar item de uma recorrência |
| [**cancelar_uma_recorrencia**](PixRecorrenteApi.md#cancelar_uma_recorrencia)                 | **POST** /v3/pix/transactions/recurrings/{id}/cancel       | Cancelar uma recorrência         |
| [**listar_itens_de_uma_recorrencia**](PixRecorrenteApi.md#listar_itens_de_uma_recorrencia)   | **GET** /v3/pix/transactions/recurrings/{id}/items         | Listar itens de uma recorrência  |
| [**listar_recorrencias**](PixRecorrenteApi.md#listar_recorrencias)                           | **GET** /v3/pix/transactions/recurrings                    | Listar recorrências              |
| [**recuperar_uma_unica_recorrencia**](PixRecorrenteApi.md#recuperar_uma_unica_recorrencia)   | **GET** /v3/pix/transactions/recurrings/{id}               | Recuperar uma única recorrência  |

# **cancelar_item_de_uma_recorrencia**

> PixRecurringTransactionGetItemResponseDTO cancelar_item_de_uma_recorrencia(id, body=body)

Cancelar item de uma recorrência

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_recurring_transaction_get_item_response_dto import PixRecurringTransactionGetItemResponseDTO
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
    api_instance = asaas.PixRecorrenteApi(api_client)
    id = '71ae9d73-468f-4d04-8b87-a541128f9c46' # str | Identificador único do item de uma recorrência no Asaas
    body = None # object |  (optional)

    try:
        # Cancelar item de uma recorrência
        api_response = api_instance.cancelar_item_de_uma_recorrencia(id, body=body)
        print("The response of PixRecorrenteApi->cancelar_item_de_uma_recorrencia:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixRecorrenteApi->cancelar_item_de_uma_recorrencia: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                                             | Notes      |
| -------- | ---------- | ------------------------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único do item de uma recorrência no Asaas |
| **body** | **object** |                                                         | [optional] |

### Return type

[**PixRecurringTransactionGetItemResponseDTO**](PixRecurringTransactionGetItemResponseDTO.md)

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

# **cancelar_uma_recorrencia**

> PixRecurringTransactionGetResponseDTO cancelar_uma_recorrencia(id, body=body)

Cancelar uma recorrência

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_recurring_transaction_get_response_dto import PixRecurringTransactionGetResponseDTO
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
    api_instance = asaas.PixRecorrenteApi(api_client)
    id = '35363f6e-93e2-11ec-b9d9-96f4053b1bd4' # str | Identificador único da recorrência no Asaas
    body = None # object |  (optional)

    try:
        # Cancelar uma recorrência
        api_response = api_instance.cancelar_uma_recorrencia(id, body=body)
        print("The response of PixRecorrenteApi->cancelar_uma_recorrencia:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixRecorrenteApi->cancelar_uma_recorrencia: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                                 | Notes      |
| -------- | ---------- | ------------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da recorrência no Asaas |
| **body** | **object** |                                             | [optional] |

### Return type

[**PixRecurringTransactionGetResponseDTO**](PixRecurringTransactionGetResponseDTO.md)

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

# **listar_itens_de_uma_recorrencia**

> RecurringPixTransactionListItemsResponseDTO listar_itens_de_uma_recorrencia(id, offset=offset, limit=limit)

Listar itens de uma recorrência

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.recurring_pix_transaction_list_items_response_dto import RecurringPixTransactionListItemsResponseDTO
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
    api_instance = asaas.PixRecorrenteApi(api_client)
    id = '35363f6e-93e2-11ec-b9d9-96f4053b1bd4' # str | Identificador único da recorrência no Asaas
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)

    try:
        # Listar itens de uma recorrência
        api_response = api_instance.listar_itens_de_uma_recorrencia(id, offset=offset, limit=limit)
        print("The response of PixRecorrenteApi->listar_itens_de_uma_recorrencia:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixRecorrenteApi->listar_itens_de_uma_recorrencia: %s\n" % e)
```

### Parameters

| Name       | Type    | Description                                 | Notes      |
| ---------- | ------- | ------------------------------------------- | ---------- |
| **id**     | **str** | Identificador único da recorrência no Asaas |
| **offset** | **int** | Elemento inicial da lista                   | [optional] |
| **limit**  | **int** | Número de elementos da lista (max: 100)     | [optional] |

### Return type

[**RecurringPixTransactionListItemsResponseDTO**](RecurringPixTransactionListItemsResponseDTO.md)

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

# **listar_recorrencias**

> PixRecurringTransactionListResponseDTO listar_recorrencias(offset=offset, limit=limit, status=status, value=value, search_text=search_text)

Listar recorrências

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_recurring_transaction_list_response_dto import PixRecurringTransactionListResponseDTO
from asaas.models.recurring_pix_transaction_list_request_pix_recurring_transaction_status import RecurringPixTransactionListRequestPixRecurringTransactionStatus
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
    api_instance = asaas.PixRecorrenteApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    status = asaas.RecurringPixTransactionListRequestPixRecurringTransactionStatus() # RecurringPixTransactionListRequestPixRecurringTransactionStatus | Filtrar pelo status da recorrência (optional)
    value = 100 # float | Filtrar pelo valor da recorrência (optional)
    search_text = 'search_text_example' # str | Filtrar pelo nome do recebedor (optional)

    try:
        # Listar recorrências
        api_response = api_instance.listar_recorrencias(offset=offset, limit=limit, status=status, value=value, search_text=search_text)
        print("The response of PixRecorrenteApi->listar_recorrencias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixRecorrenteApi->listar_recorrencias: %s\n" % e)
```

### Parameters

| Name            | Type                                                                       | Description                             | Notes      |
| --------------- | -------------------------------------------------------------------------- | --------------------------------------- | ---------- |
| **offset**      | **int**                                                                    | Elemento inicial da lista               | [optional] |
| **limit**       | **int**                                                                    | Número de elementos da lista (max: 100) | [optional] |
| **status**      | [**RecurringPixTransactionListRequestPixRecurringTransactionStatus**](.md) | Filtrar pelo status da recorrência      | [optional] |
| **value**       | **float**                                                                  | Filtrar pelo valor da recorrência       | [optional] |
| **search_text** | **str**                                                                    | Filtrar pelo nome do recebedor          | [optional] |

### Return type

[**PixRecurringTransactionListResponseDTO**](PixRecurringTransactionListResponseDTO.md)

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

# **recuperar_uma_unica_recorrencia**

> PixRecurringTransactionGetResponseDTO recuperar_uma_unica_recorrencia(id)

Recuperar uma única recorrência

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_recurring_transaction_get_response_dto import PixRecurringTransactionGetResponseDTO
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
    api_instance = asaas.PixRecorrenteApi(api_client)
    id = '35363f6e-93e2-11ec-b9d9-96f4053b1bd4' # str | Identificador único da recorrência no Asaas

    try:
        # Recuperar uma única recorrência
        api_response = api_instance.recuperar_uma_unica_recorrencia(id)
        print("The response of PixRecorrenteApi->recuperar_uma_unica_recorrencia:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixRecorrenteApi->recuperar_uma_unica_recorrencia: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                 | Notes |
| ------ | ------- | ------------------------------------------- | ----- |
| **id** | **str** | Identificador único da recorrência no Asaas |

### Return type

[**PixRecurringTransactionGetResponseDTO**](PixRecurringTransactionGetResponseDTO.md)

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
