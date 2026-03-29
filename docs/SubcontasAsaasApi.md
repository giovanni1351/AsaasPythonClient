# asaas.SubcontasAsaasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                    | HTTP request                                              | Description                            |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- | -------------------------------------- |
| [**atualizar_chave_de_api_de_uma_subconta**](SubcontasAsaasApi.md#atualizar_chave_de_api_de_uma_subconta) | **PUT** /v3/accounts/{id}/accessTokens/{accessTokenId}    | Atualizar chave de API de uma subconta |
| [**criar_chave_de_api_para_uma_subconta**](SubcontasAsaasApi.md#criar_chave_de_api_para_uma_subconta)     | **POST** /v3/accounts/{id}/accessTokens                   | Criar chave de API para uma subconta   |
| [**criar_subconta**](SubcontasAsaasApi.md#criar_subconta)                                                 | **POST** /v3/accounts                                     | Criar subconta                         |
| [**excluir_chave_de_api_de_uma_subconta**](SubcontasAsaasApi.md#excluir_chave_de_api_de_uma_subconta)     | **DELETE** /v3/accounts/{id}/accessTokens/{accessTokenId} | Excluir chave de API de uma subconta   |
| [**listar_chaves_de_api_de_uma_subconta**](SubcontasAsaasApi.md#listar_chaves_de_api_de_uma_subconta)     | **GET** /v3/accounts/{id}/accessTokens                    | Listar chaves de API de uma subconta   |
| [**listar_subcontas**](SubcontasAsaasApi.md#listar_subcontas)                                             | **GET** /v3/accounts                                      | Listar subcontas                       |
| [**recuperar_uma_unica_subconta**](SubcontasAsaasApi.md#recuperar_uma_unica_subconta)                     | **GET** /v3/accounts/{id}                                 | Recuperar uma única subconta           |

# **atualizar_chave_de_api_de_uma_subconta**

> CustomerApiAccessTokenBaseResponseDTO atualizar_chave_de_api_de_uma_subconta(id, access_token_id, customer_api_access_token_update_request_dto=customer_api_access_token_update_request_dto)

Atualizar chave de API de uma subconta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_api_access_token_base_response_dto import CustomerApiAccessTokenBaseResponseDTO
from asaas.models.customer_api_access_token_update_request_dto import CustomerApiAccessTokenUpdateRequestDTO
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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    id = 'b6bff0c5-38c6-496a-a3a8-105b31d5bcfe' # str | Identificador único da subconta no Asaas
    access_token_id = '279baa3b-2cfd-4d41-b04b-e3299ae4b645' # str | ID da chave de API
    customer_api_access_token_update_request_dto = asaas.CustomerApiAccessTokenUpdateRequestDTO() # CustomerApiAccessTokenUpdateRequestDTO |  (optional)

    try:
        # Atualizar chave de API de uma subconta
        api_response = api_instance.atualizar_chave_de_api_de_uma_subconta(id, access_token_id, customer_api_access_token_update_request_dto=customer_api_access_token_update_request_dto)
        print("The response of SubcontasAsaasApi->atualizar_chave_de_api_de_uma_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->atualizar_chave_de_api_de_uma_subconta: %s\n" % e)
```

### Parameters

| Name                                             | Type                                                                                    | Description                              | Notes      |
| ------------------------------------------------ | --------------------------------------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                                           | **str**                                                                                 | Identificador único da subconta no Asaas |
| **access_token_id**                              | **str**                                                                                 | ID da chave de API                       |
| **customer_api_access_token_update_request_dto** | [**CustomerApiAccessTokenUpdateRequestDTO**](CustomerApiAccessTokenUpdateRequestDTO.md) |                                          | [optional] |

### Return type

[**CustomerApiAccessTokenBaseResponseDTO**](CustomerApiAccessTokenBaseResponseDTO.md)

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

# **criar_chave_de_api_para_uma_subconta**

> CustomerApiAccessTokenSaveResponseDTO criar_chave_de_api_para_uma_subconta(id, customer_api_access_token_save_request_dto=customer_api_access_token_save_request_dto)

Criar chave de API para uma subconta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_api_access_token_save_request_dto import CustomerApiAccessTokenSaveRequestDTO
from asaas.models.customer_api_access_token_save_response_dto import CustomerApiAccessTokenSaveResponseDTO
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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    id = 'b6bff0c5-38c6-496a-a3a8-105b31d5bcfe' # str | Identificador único da subconta no Asaas
    customer_api_access_token_save_request_dto = asaas.CustomerApiAccessTokenSaveRequestDTO() # CustomerApiAccessTokenSaveRequestDTO |  (optional)

    try:
        # Criar chave de API para uma subconta
        api_response = api_instance.criar_chave_de_api_para_uma_subconta(id, customer_api_access_token_save_request_dto=customer_api_access_token_save_request_dto)
        print("The response of SubcontasAsaasApi->criar_chave_de_api_para_uma_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->criar_chave_de_api_para_uma_subconta: %s\n" % e)
```

### Parameters

| Name                                           | Type                                                                                | Description                              | Notes      |
| ---------------------------------------------- | ----------------------------------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                                         | **str**                                                                             | Identificador único da subconta no Asaas |
| **customer_api_access_token_save_request_dto** | [**CustomerApiAccessTokenSaveRequestDTO**](CustomerApiAccessTokenSaveRequestDTO.md) |                                          | [optional] |

### Return type

[**CustomerApiAccessTokenSaveResponseDTO**](CustomerApiAccessTokenSaveResponseDTO.md)

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

# **criar_subconta**

> AccountSaveResponseDTO criar_subconta(account_save_request_dto=account_save_request_dto)

Criar subconta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_save_request_dto import AccountSaveRequestDTO
from asaas.models.account_save_response_dto import AccountSaveResponseDTO
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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    account_save_request_dto = asaas.AccountSaveRequestDTO() # AccountSaveRequestDTO |  (optional)

    try:
        # Criar subconta
        api_response = api_instance.criar_subconta(account_save_request_dto=account_save_request_dto)
        print("The response of SubcontasAsaasApi->criar_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->criar_subconta: %s\n" % e)
```

### Parameters

| Name                         | Type                                                  | Description | Notes      |
| ---------------------------- | ----------------------------------------------------- | ----------- | ---------- |
| **account_save_request_dto** | [**AccountSaveRequestDTO**](AccountSaveRequestDTO.md) |             | [optional] |

### Return type

[**AccountSaveResponseDTO**](AccountSaveResponseDTO.md)

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

# **excluir_chave_de_api_de_uma_subconta**

> excluir_chave_de_api_de_uma_subconta(id, access_token_id)

Excluir chave de API de uma subconta

### Example

- Api Key Authentication (Authorization):

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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    id = 'b6bff0c5-38c6-496a-a3a8-105b31d5bcfe' # str | Identificador único da subconta no Asaas
    access_token_id = '279baa3b-2cfd-4d41-b04b-e3299ae4b645' # str | ID da chave de API

    try:
        # Excluir chave de API de uma subconta
        api_instance.excluir_chave_de_api_de_uma_subconta(id, access_token_id)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->excluir_chave_de_api_de_uma_subconta: %s\n" % e)
```

### Parameters

| Name                | Type    | Description                              | Notes |
| ------------------- | ------- | ---------------------------------------- | ----- |
| **id**              | **str** | Identificador único da subconta no Asaas |
| **access_token_id** | **str** | ID da chave de API                       |

### Return type

void (empty response body)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **204**     | No Content   | -                |
| **401**     | Unauthorized | -                |
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **listar_chaves_de_api_de_uma_subconta**

> CustomerApiAccessTokenListResponseDTO listar_chaves_de_api_de_uma_subconta(id)

Listar chaves de API de uma subconta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.customer_api_access_token_list_response_dto import CustomerApiAccessTokenListResponseDTO
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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    id = '4f468235-cec3-482f-b3d0-348af4c7194' # str | Identificador único da subconta no Asaas

    try:
        # Listar chaves de API de uma subconta
        api_response = api_instance.listar_chaves_de_api_de_uma_subconta(id)
        print("The response of SubcontasAsaasApi->listar_chaves_de_api_de_uma_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->listar_chaves_de_api_de_uma_subconta: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da subconta no Asaas |

### Return type

[**CustomerApiAccessTokenListResponseDTO**](CustomerApiAccessTokenListResponseDTO.md)

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

# **listar_subcontas**

> AccountListResponseDTO listar_subcontas(offset=offset, limit=limit, cpf_cnpj=cpf_cnpj, email=email, name=name, wallet_id=wallet_id)

Listar subcontas

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_list_response_dto import AccountListResponseDTO
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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    cpf_cnpj = 'cpf_cnpj_example' # str | Filtrar pelo cpf ou cnpj da subconta (optional)
    email = 'email_example' # str | Filtrar pelo email da subconta (optional)
    name = 'name_example' # str | Filtrar pelo nome da subconta (optional)
    wallet_id = 'wallet_id_example' # str | Filtrar pelo walletId da subconta (optional)

    try:
        # Listar subcontas
        api_response = api_instance.listar_subcontas(offset=offset, limit=limit, cpf_cnpj=cpf_cnpj, email=email, name=name, wallet_id=wallet_id)
        print("The response of SubcontasAsaasApi->listar_subcontas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->listar_subcontas: %s\n" % e)
```

### Parameters

| Name          | Type    | Description                             | Notes      |
| ------------- | ------- | --------------------------------------- | ---------- |
| **offset**    | **int** | Elemento inicial da lista               | [optional] |
| **limit**     | **int** | Número de elementos da lista (max: 100) | [optional] |
| **cpf_cnpj**  | **str** | Filtrar pelo cpf ou cnpj da subconta    | [optional] |
| **email**     | **str** | Filtrar pelo email da subconta          | [optional] |
| **name**      | **str** | Filtrar pelo nome da subconta           | [optional] |
| **wallet_id** | **str** | Filtrar pelo walletId da subconta       | [optional] |

### Return type

[**AccountListResponseDTO**](AccountListResponseDTO.md)

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

# **recuperar_uma_unica_subconta**

> AccountGetResponseDTO recuperar_uma_unica_subconta(id)

Recuperar uma única subconta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_get_response_dto import AccountGetResponseDTO
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
    api_instance = asaas.SubcontasAsaasApi(api_client)
    id = '4f468235-cec3-482f-b3d0-348af4c7194' # str | Identificador único da subconta no Asaas

    try:
        # Recuperar uma única subconta
        api_response = api_instance.recuperar_uma_unica_subconta(id)
        print("The response of SubcontasAsaasApi->recuperar_uma_unica_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubcontasAsaasApi->recuperar_uma_unica_subconta: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da subconta no Asaas |

### Return type

[**AccountGetResponseDTO**](AccountGetResponseDTO.md)

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
