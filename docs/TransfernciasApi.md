# asaas.TransfernciasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                                     | HTTP request                         | Description                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------ | ------------------------------------------------------- |
| [**cancelar_uma_transferncia**](TransfernciasApi.md#cancelar_uma_transferncia)                                                             | **DELETE** /v3/transfers/{id}/cancel | Cancelar uma transferência                              |
| [**listar_transferencias**](TransfernciasApi.md#listar_transferencias)                                                                     | **GET** /v3/transfers                | Listar transferências                                   |
| [**recuperar_uma_unica_transferencia**](TransfernciasApi.md#recuperar_uma_unica_transferencia)                                             | **GET** /v3/transfers/{id}           | Recuperar uma única transferência                       |
| [**transferir_para_conta_asaas**](TransfernciasApi.md#transferir_para_conta_asaas)                                                         | **POST** /v3/transfers/              | Transferir para conta Asaas                             |
| [**transferir_para_conta_de_outra_instituicao_ou_chave_pix**](TransfernciasApi.md#transferir_para_conta_de_outra_instituicao_ou_chave_pix) | **POST** /v3/transfers               | Transferir para conta de outra Instituição ou chave Pix |

# **cancelar_uma_transferncia**

> TransferGetResponseDTO cancelar_uma_transferncia(id)

Cancelar uma transferência

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.transfer_get_response_dto import TransferGetResponseDTO
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
    api_instance = asaas.TransfernciasApi(api_client)
    id = '777eb7c8-b1a2-4356-8fd8-a1b0644b5282' # str | Identificador único da transferência no Asaas

    try:
        # Cancelar uma transferência
        api_response = api_instance.cancelar_uma_transferncia(id)
        print("The response of TransfernciasApi->cancelar_uma_transferncia:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransfernciasApi->cancelar_uma_transferncia: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                   | Notes |
| ------ | ------- | --------------------------------------------- | ----- |
| **id** | **str** | Identificador único da transferência no Asaas |

### Return type

[**TransferGetResponseDTO**](TransferGetResponseDTO.md)

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

# **listar_transferencias**

> TransferListResponseDTO listar_transferencias(date_created_ge=date_created_ge, date_created_le=date_created_le, transfer_date_ge=transfer_date_ge, transfer_date_le=transfer_date_le, type=type)

Listar transferências

Este método retorna uma lista paginada com todas as transferências para o filtro informado.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.transfer_list_response_dto import TransferListResponseDTO
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
    api_instance = asaas.TransfernciasApi(api_client)
    date_created_ge = 'date_created_ge_example' # str | Filtrar pela data de criação inicial (optional)
    date_created_le = 'date_created_le_example' # str | Filtrar pela data de criação final (optional)
    transfer_date_ge = 'transfer_date_ge_example' # str | Filtrar pela data inicial de efetivação de transferência (optional)
    transfer_date_le = 'transfer_date_le_example' # str | Filtrar pela data final de efetivação de transferência (optional)
    type = 'ASAAS_ACCOUNT' # str | Filtrar por tipo da transferência (optional)

    try:
        # Listar transferências
        api_response = api_instance.listar_transferencias(date_created_ge=date_created_ge, date_created_le=date_created_le, transfer_date_ge=transfer_date_ge, transfer_date_le=transfer_date_le, type=type)
        print("The response of TransfernciasApi->listar_transferencias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransfernciasApi->listar_transferencias: %s\n" % e)
```

### Parameters

| Name                 | Type    | Description                                              | Notes      |
| -------------------- | ------- | -------------------------------------------------------- | ---------- |
| **date_created_ge**  | **str** | Filtrar pela data de criação inicial                     | [optional] |
| **date_created_le**  | **str** | Filtrar pela data de criação final                       | [optional] |
| **transfer_date_ge** | **str** | Filtrar pela data inicial de efetivação de transferência | [optional] |
| **transfer_date_le** | **str** | Filtrar pela data final de efetivação de transferência   | [optional] |
| **type**             | **str** | Filtrar por tipo da transferência                        | [optional] |

### Return type

[**TransferListResponseDTO**](TransferListResponseDTO.md)

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

# **recuperar_uma_unica_transferencia**

> TransferGetResponseDTO recuperar_uma_unica_transferencia(id)

Recuperar uma única transferência

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.transfer_get_response_dto import TransferGetResponseDTO
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
    api_instance = asaas.TransfernciasApi(api_client)
    id = '777eb7c8-b1a2-4356-8fd8-a1b0644b528' # str | Identificador único da transferência no Asaas

    try:
        # Recuperar uma única transferência
        api_response = api_instance.recuperar_uma_unica_transferencia(id)
        print("The response of TransfernciasApi->recuperar_uma_unica_transferencia:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransfernciasApi->recuperar_uma_unica_transferencia: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                   | Notes |
| ------ | ------- | --------------------------------------------- | ----- |
| **id** | **str** | Identificador único da transferência no Asaas |

### Return type

[**TransferGetResponseDTO**](TransferGetResponseDTO.md)

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

# **transferir_para_conta_asaas**

> TransferSaveInternalTransferResponseDTO transferir_para_conta_asaas(transfer_save_internal_transfer_request_dto=transfer_save_internal_transfer_request_dto)

Transferir para conta Asaas

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.transfer_save_internal_transfer_request_dto import TransferSaveInternalTransferRequestDTO
from asaas.models.transfer_save_internal_transfer_response_dto import TransferSaveInternalTransferResponseDTO
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
    api_instance = asaas.TransfernciasApi(api_client)
    transfer_save_internal_transfer_request_dto = asaas.TransferSaveInternalTransferRequestDTO() # TransferSaveInternalTransferRequestDTO |  (optional)

    try:
        # Transferir para conta Asaas
        api_response = api_instance.transferir_para_conta_asaas(transfer_save_internal_transfer_request_dto=transfer_save_internal_transfer_request_dto)
        print("The response of TransfernciasApi->transferir_para_conta_asaas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransfernciasApi->transferir_para_conta_asaas: %s\n" % e)
```

### Parameters

| Name                                            | Type                                                                                    | Description | Notes      |
| ----------------------------------------------- | --------------------------------------------------------------------------------------- | ----------- | ---------- |
| **transfer_save_internal_transfer_request_dto** | [**TransferSaveInternalTransferRequestDTO**](TransferSaveInternalTransferRequestDTO.md) |             | [optional] |

### Return type

[**TransferSaveInternalTransferResponseDTO**](TransferSaveInternalTransferResponseDTO.md)

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

# **transferir_para_conta_de_outra_instituicao_ou_chave_pix**

> TransferGetResponseDTO transferir_para_conta_de_outra_instituicao_ou_chave_pix(transfer_save_request_dto=transfer_save_request_dto)

Transferir para conta de outra Instituição ou chave Pix

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.transfer_get_response_dto import TransferGetResponseDTO
from asaas.models.transfer_save_request_dto import TransferSaveRequestDTO
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
    api_instance = asaas.TransfernciasApi(api_client)
    transfer_save_request_dto = asaas.TransferSaveRequestDTO() # TransferSaveRequestDTO |  (optional)

    try:
        # Transferir para conta de outra Instituição ou chave Pix
        api_response = api_instance.transferir_para_conta_de_outra_instituicao_ou_chave_pix(transfer_save_request_dto=transfer_save_request_dto)
        print("The response of TransfernciasApi->transferir_para_conta_de_outra_instituicao_ou_chave_pix:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransfernciasApi->transferir_para_conta_de_outra_instituicao_ou_chave_pix: %s\n" % e)
```

### Parameters

| Name                          | Type                                                    | Description | Notes      |
| ----------------------------- | ------------------------------------------------------- | ----------- | ---------- |
| **transfer_save_request_dto** | [**TransferSaveRequestDTO**](TransferSaveRequestDTO.md) |             | [optional] |

### Return type

[**TransferGetResponseDTO**](TransferGetResponseDTO.md)

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
