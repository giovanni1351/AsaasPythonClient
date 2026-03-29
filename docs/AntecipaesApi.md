# asaas.AntecipaesApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                        | HTTP request                             | Description                                |
| ------------------------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------------------------------ |
| [**atualizar_status_da_antecipacao_automatica**](AntecipaesApi.md#atualizar_status_da_antecipacao_automatica) | **PUT** /v3/anticipations/configurations | Atualizar status da antecipação automática |
| [**cancelar_antecipacao**](AntecipaesApi.md#cancelar_antecipacao)                                             | **POST** /v3/anticipations/{id}/cancel   | Cancelar antecipação                       |
| [**listar_antecipacoes**](AntecipaesApi.md#listar_antecipacoes)                                               | **GET** /v3/anticipations                | Listar antecipações                        |
| [**recuperar_limites_de_antecipacoes**](AntecipaesApi.md#recuperar_limites_de_antecipacoes)                   | **GET** /v3/anticipations/limits         | Recuperar limites de antecipações          |
| [**recuperar_status_da_antecipacao_automatica**](AntecipaesApi.md#recuperar_status_da_antecipacao_automatica) | **GET** /v3/anticipations/configurations | Recuperar status da antecipação automática |
| [**recuperar_uma_unica_antecipacao**](AntecipaesApi.md#recuperar_uma_unica_antecipacao)                       | **GET** /v3/anticipations/{id}           | Recuperar uma única antecipação            |
| [**simular_antecipao**](AntecipaesApi.md#simular_antecipao)                                                   | **POST** /v3/anticipations/simulate      | Simular antecipação                        |
| [**solicitar_antecipacao**](AntecipaesApi.md#solicitar_antecipacao)                                           | **POST** /v3/anticipations               | Solicitar antecipação                      |

# **atualizar_status_da_antecipacao_automatica**

> AnticipationConfigurationGetResponseDTO atualizar_status_da_antecipacao_automatica(anticipation_configuration_update_request_dto=anticipation_configuration_update_request_dto)

Atualizar status da antecipação automática

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_configuration_get_response_dto import AnticipationConfigurationGetResponseDTO
from asaas.models.anticipation_configuration_update_request_dto import AnticipationConfigurationUpdateRequestDTO
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
    api_instance = asaas.AntecipaesApi(api_client)
    anticipation_configuration_update_request_dto = asaas.AnticipationConfigurationUpdateRequestDTO() # AnticipationConfigurationUpdateRequestDTO |  (optional)

    try:
        # Atualizar status da antecipação automática
        api_response = api_instance.atualizar_status_da_antecipacao_automatica(anticipation_configuration_update_request_dto=anticipation_configuration_update_request_dto)
        print("The response of AntecipaesApi->atualizar_status_da_antecipacao_automatica:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->atualizar_status_da_antecipacao_automatica: %s\n" % e)
```

### Parameters

| Name                                              | Type                                                                                          | Description | Notes      |
| ------------------------------------------------- | --------------------------------------------------------------------------------------------- | ----------- | ---------- |
| **anticipation_configuration_update_request_dto** | [**AnticipationConfigurationUpdateRequestDTO**](AnticipationConfigurationUpdateRequestDTO.md) |             | [optional] |

### Return type

[**AnticipationConfigurationGetResponseDTO**](AnticipationConfigurationGetResponseDTO.md)

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

# **cancelar_antecipacao**

> AnticipationGetResponseDTO cancelar_antecipacao(id, body=body)

Cancelar antecipação

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_get_response_dto import AnticipationGetResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)
    id = 'id_example' # str | Identificador único da antecipação no Asaas
    body = None # object |  (optional)

    try:
        # Cancelar antecipação
        api_response = api_instance.cancelar_antecipacao(id, body=body)
        print("The response of AntecipaesApi->cancelar_antecipacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->cancelar_antecipacao: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                                 | Notes      |
| -------- | ---------- | ------------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da antecipação no Asaas |
| **body** | **object** |                                             | [optional] |

### Return type

[**AnticipationGetResponseDTO**](AnticipationGetResponseDTO.md)

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

# **listar_antecipacoes**

> AnticipationListResponseDTO listar_antecipacoes(offset=offset, limit=limit, payment=payment, installment=installment, status=status)

Listar antecipações

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_list_request_anticipation_status import AnticipationListRequestAnticipationStatus
from asaas.models.anticipation_list_response_dto import AnticipationListResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    payment = 'payment_example' # str | Filtrar antecipações de uma cobrança (optional)
    installment = 'installment_example' # str | Filtrar antecipações de um parcelamento (optional)
    status = asaas.AnticipationListRequestAnticipationStatus() # AnticipationListRequestAnticipationStatus | Filtrar por status (optional)

    try:
        # Listar antecipações
        api_response = api_instance.listar_antecipacoes(offset=offset, limit=limit, payment=payment, installment=installment, status=status)
        print("The response of AntecipaesApi->listar_antecipacoes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->listar_antecipacoes: %s\n" % e)
```

### Parameters

| Name            | Type                                                 | Description                             | Notes      |
| --------------- | ---------------------------------------------------- | --------------------------------------- | ---------- |
| **offset**      | **int**                                              | Elemento inicial da lista               | [optional] |
| **limit**       | **int**                                              | Número de elementos da lista (max: 100) | [optional] |
| **payment**     | **str**                                              | Filtrar antecipações de uma cobrança    | [optional] |
| **installment** | **str**                                              | Filtrar antecipações de um parcelamento | [optional] |
| **status**      | [**AnticipationListRequestAnticipationStatus**](.md) | Filtrar por status                      | [optional] |

### Return type

[**AnticipationListResponseDTO**](AnticipationListResponseDTO.md)

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

# **recuperar_limites_de_antecipacoes**

> AnticipationLimitsResponseDTO recuperar_limites_de_antecipacoes()

Recuperar limites de antecipações

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_limits_response_dto import AnticipationLimitsResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)

    try:
        # Recuperar limites de antecipações
        api_response = api_instance.recuperar_limites_de_antecipacoes()
        print("The response of AntecipaesApi->recuperar_limites_de_antecipacoes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->recuperar_limites_de_antecipacoes: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AnticipationLimitsResponseDTO**](AnticipationLimitsResponseDTO.md)

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

# **recuperar_status_da_antecipacao_automatica**

> AnticipationConfigurationGetResponseDTO recuperar_status_da_antecipacao_automatica()

Recuperar status da antecipação automática

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_configuration_get_response_dto import AnticipationConfigurationGetResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)

    try:
        # Recuperar status da antecipação automática
        api_response = api_instance.recuperar_status_da_antecipacao_automatica()
        print("The response of AntecipaesApi->recuperar_status_da_antecipacao_automatica:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->recuperar_status_da_antecipacao_automatica: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AnticipationConfigurationGetResponseDTO**](AnticipationConfigurationGetResponseDTO.md)

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

# **recuperar_uma_unica_antecipacao**

> AnticipationGetResponseDTO recuperar_uma_unica_antecipacao(id)

Recuperar uma única antecipação

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_get_response_dto import AnticipationGetResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)
    id = 'id_example' # str | Identificador único da antecipação no Asaas

    try:
        # Recuperar uma única antecipação
        api_response = api_instance.recuperar_uma_unica_antecipacao(id)
        print("The response of AntecipaesApi->recuperar_uma_unica_antecipacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->recuperar_uma_unica_antecipacao: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                 | Notes |
| ------ | ------- | ------------------------------------------- | ----- |
| **id** | **str** | Identificador único da antecipação no Asaas |

### Return type

[**AnticipationGetResponseDTO**](AnticipationGetResponseDTO.md)

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

# **simular_antecipao**

> AnticipationSimulateResponseDTO simular_antecipao(anticipation_simulate_request_dto=anticipation_simulate_request_dto)

Simular antecipação

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_simulate_request_dto import AnticipationSimulateRequestDTO
from asaas.models.anticipation_simulate_response_dto import AnticipationSimulateResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)
    anticipation_simulate_request_dto = asaas.AnticipationSimulateRequestDTO() # AnticipationSimulateRequestDTO |  (optional)

    try:
        # Simular antecipação
        api_response = api_instance.simular_antecipao(anticipation_simulate_request_dto=anticipation_simulate_request_dto)
        print("The response of AntecipaesApi->simular_antecipao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->simular_antecipao: %s\n" % e)
```

### Parameters

| Name                                  | Type                                                                    | Description | Notes      |
| ------------------------------------- | ----------------------------------------------------------------------- | ----------- | ---------- |
| **anticipation_simulate_request_dto** | [**AnticipationSimulateRequestDTO**](AnticipationSimulateRequestDTO.md) |             | [optional] |

### Return type

[**AnticipationSimulateResponseDTO**](AnticipationSimulateResponseDTO.md)

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

# **solicitar_antecipacao**

> AnticipationGetResponseDTO solicitar_antecipacao(installment=installment, payment=payment, documents=documents)

Solicitar antecipação

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.anticipation_get_response_dto import AnticipationGetResponseDTO
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
    api_instance = asaas.AntecipaesApi(api_client)
    installment = 'installment_example' # str | ID do parcelamento a ser antecipado (optional)
    payment = 'payment_example' # str | ID da cobrança a ser antecipada (optional)
    documents = None # bytes | Arquivo (optional)

    try:
        # Solicitar antecipação
        api_response = api_instance.solicitar_antecipacao(installment=installment, payment=payment, documents=documents)
        print("The response of AntecipaesApi->solicitar_antecipacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AntecipaesApi->solicitar_antecipacao: %s\n" % e)
```

### Parameters

| Name            | Type      | Description                         | Notes      |
| --------------- | --------- | ----------------------------------- | ---------- |
| **installment** | **str**   | ID do parcelamento a ser antecipado | [optional] |
| **payment**     | **str**   | ID da cobrança a ser antecipada     | [optional] |
| **documents**   | **bytes** | Arquivo                             | [optional] |

### Return type

[**AnticipationGetResponseDTO**](AnticipationGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)
