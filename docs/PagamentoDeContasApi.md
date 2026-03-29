# asaas.PagamentoDeContasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                     | HTTP request                  | Description                           |
| ---------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------------------------------- |
| [**cancelar_pagamento_de_contas**](PagamentoDeContasApi.md#cancelar_pagamento_de_contas)                   | **POST** /v3/bill/{id}/cancel | Cancelar pagamento de contas          |
| [**criar_um_pagamento_de_conta**](PagamentoDeContasApi.md#criar_um_pagamento_de_conta)                     | **POST** /v3/bill             | Criar um pagamento de conta           |
| [**listar_pagamento_de_contas**](PagamentoDeContasApi.md#listar_pagamento_de_contas)                       | **GET** /v3/bill              | Listar pagamento de contas            |
| [**recuperar_um_unico_pagamento_de_conta**](PagamentoDeContasApi.md#recuperar_um_unico_pagamento_de_conta) | **GET** /v3/bill/{id}         | Recuperar um único pagamento de conta |
| [**simular_um_pagamento_de_conta**](PagamentoDeContasApi.md#simular_um_pagamento_de_conta)                 | **POST** /v3/bill/simulate    | Simular um pagamento de conta         |

# **cancelar_pagamento_de_contas**

> BillGetResponseDTO cancelar_pagamento_de_contas(id, body=body)

Cancelar pagamento de contas

Permite o cancelamento do pagamento de conta. Utilize a propriedade `canBeCancelled` do objeto `bill` para verificar se o pagamento de conta pode ser cancelado.
Ao ser cancelado o pagamento da conta não será realizado.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.bill_get_response_dto import BillGetResponseDTO
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
    api_instance = asaas.PagamentoDeContasApi(api_client)
    id = '1bce822-6f37-4905-8de8-f1af9f2f4bab' # str | Identificador único do pagamento de conta a ser cancelado
    body = None # object |  (optional)

    try:
        # Cancelar pagamento de contas
        api_response = api_instance.cancelar_pagamento_de_contas(id, body=body)
        print("The response of PagamentoDeContasApi->cancelar_pagamento_de_contas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PagamentoDeContasApi->cancelar_pagamento_de_contas: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                                               | Notes      |
| -------- | ---------- | --------------------------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único do pagamento de conta a ser cancelado |
| **body** | **object** |                                                           | [optional] |

### Return type

[**BillGetResponseDTO**](BillGetResponseDTO.md)

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

# **criar_um_pagamento_de_conta**

> BillGetResponseDTO criar_um_pagamento_de_conta(bill_save_request_dto=bill_save_request_dto)

Criar um pagamento de conta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.bill_get_response_dto import BillGetResponseDTO
from asaas.models.bill_save_request_dto import BillSaveRequestDTO
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
    api_instance = asaas.PagamentoDeContasApi(api_client)
    bill_save_request_dto = asaas.BillSaveRequestDTO() # BillSaveRequestDTO |  (optional)

    try:
        # Criar um pagamento de conta
        api_response = api_instance.criar_um_pagamento_de_conta(bill_save_request_dto=bill_save_request_dto)
        print("The response of PagamentoDeContasApi->criar_um_pagamento_de_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PagamentoDeContasApi->criar_um_pagamento_de_conta: %s\n" % e)
```

### Parameters

| Name                      | Type                                            | Description | Notes      |
| ------------------------- | ----------------------------------------------- | ----------- | ---------- |
| **bill_save_request_dto** | [**BillSaveRequestDTO**](BillSaveRequestDTO.md) |             | [optional] |

### Return type

[**BillGetResponseDTO**](BillGetResponseDTO.md)

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

# **listar_pagamento_de_contas**

> BillListResponseDTO listar_pagamento_de_contas(offset=offset, limit=limit)

Listar pagamento de contas

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.bill_list_response_dto import BillListResponseDTO
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
    api_instance = asaas.PagamentoDeContasApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)

    try:
        # Listar pagamento de contas
        api_response = api_instance.listar_pagamento_de_contas(offset=offset, limit=limit)
        print("The response of PagamentoDeContasApi->listar_pagamento_de_contas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PagamentoDeContasApi->listar_pagamento_de_contas: %s\n" % e)
```

### Parameters

| Name       | Type    | Description                             | Notes      |
| ---------- | ------- | --------------------------------------- | ---------- |
| **offset** | **int** | Elemento inicial da lista               | [optional] |
| **limit**  | **int** | Número de elementos da lista (max: 100) | [optional] |

### Return type

[**BillListResponseDTO**](BillListResponseDTO.md)

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

# **recuperar_um_unico_pagamento_de_conta**

> BillGetResponseDTO recuperar_um_unico_pagamento_de_conta(id)

Recuperar um único pagamento de conta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.bill_get_response_dto import BillGetResponseDTO
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
    api_instance = asaas.PagamentoDeContasApi(api_client)
    id = 'f1bce822-6f37-4905-8de8-f1af9f2f4bab' # str | Identificador único do pagamento de conta no Asaas

    try:
        # Recuperar um único pagamento de conta
        api_response = api_instance.recuperar_um_unico_pagamento_de_conta(id)
        print("The response of PagamentoDeContasApi->recuperar_um_unico_pagamento_de_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PagamentoDeContasApi->recuperar_um_unico_pagamento_de_conta: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                        | Notes |
| ------ | ------- | -------------------------------------------------- | ----- |
| **id** | **str** | Identificador único do pagamento de conta no Asaas |

### Return type

[**BillGetResponseDTO**](BillGetResponseDTO.md)

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

# **simular_um_pagamento_de_conta**

> BillSimulateResponseDTO simular_um_pagamento_de_conta(bill_simulate_request_dto=bill_simulate_request_dto)

Simular um pagamento de conta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.bill_simulate_request_dto import BillSimulateRequestDTO
from asaas.models.bill_simulate_response_dto import BillSimulateResponseDTO
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
    api_instance = asaas.PagamentoDeContasApi(api_client)
    bill_simulate_request_dto = asaas.BillSimulateRequestDTO() # BillSimulateRequestDTO |  (optional)

    try:
        # Simular um pagamento de conta
        api_response = api_instance.simular_um_pagamento_de_conta(bill_simulate_request_dto=bill_simulate_request_dto)
        print("The response of PagamentoDeContasApi->simular_um_pagamento_de_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PagamentoDeContasApi->simular_um_pagamento_de_conta: %s\n" % e)
```

### Parameters

| Name                          | Type                                                    | Description | Notes      |
| ----------------------------- | ------------------------------------------------------- | ----------- | ---------- |
| **bill_simulate_request_dto** | [**BillSimulateRequestDTO**](BillSimulateRequestDTO.md) |             | [optional] |

### Return type

[**BillSimulateResponseDTO**](BillSimulateResponseDTO.md)

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
