# asaas.EnvioDeDocumentosWhiteLabelApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                 | HTTP request                                  | Description                    |
| ------------------------------------------------------------------------------------------------------ | --------------------------------------------- | ------------------------------ |
| [**atualizar_documento_enviado**](EnvioDeDocumentosWhiteLabelApi.md#atualizar_documento_enviado)       | **POST** /v3/myAccount/documents/files/{id}   | Atualizar documento enviado    |
| [**enviar_documentos**](EnvioDeDocumentosWhiteLabelApi.md#enviar_documentos)                           | **POST** /v3/myAccount/documents/{id}         | Enviar documentos              |
| [**remover_documento_enviado**](EnvioDeDocumentosWhiteLabelApi.md#remover_documento_enviado)           | **DELETE** /v3/myAccount/documents/files/{id} | Remover documento enviado      |
| [**verificar_documentos_pendentes**](EnvioDeDocumentosWhiteLabelApi.md#verificar_documentos_pendentes) | **GET** /v3/myAccount/documents               | Verificar documentos pendentes |
| [**visualizar_documento_enviado**](EnvioDeDocumentosWhiteLabelApi.md#visualizar_documento_enviado)     | **GET** /v3/myAccount/documents/files/{id}    | Visualizar documento enviado   |

# **atualizar_documento_enviado**

> AccountDocumentGetResponseDTO atualizar_documento_enviado(id, document_file)

Atualizar documento enviado

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_document_get_response_dto import AccountDocumentGetResponseDTO
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
    api_instance = asaas.EnvioDeDocumentosWhiteLabelApi(api_client)
    id = '8d257732-2220-11ec-b695-b6af4a64184d' # str | Identificador único do documento no Asaas
    document_file = None # bytes | Arquivo

    try:
        # Atualizar documento enviado
        api_response = api_instance.atualizar_documento_enviado(id, document_file)
        print("The response of EnvioDeDocumentosWhiteLabelApi->atualizar_documento_enviado:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvioDeDocumentosWhiteLabelApi->atualizar_documento_enviado: %s\n" % e)
```

### Parameters

| Name              | Type      | Description                               | Notes |
| ----------------- | --------- | ----------------------------------------- | ----- |
| **id**            | **str**   | Identificador único do documento no Asaas |
| **document_file** | **bytes** | Arquivo                                   |

### Return type

[**AccountDocumentGetResponseDTO**](AccountDocumentGetResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **enviar_documentos**

> AccountDocumentGetResponseDTO enviar_documentos(id, document_file=document_file, type=type)

Enviar documentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_document_get_response_dto import AccountDocumentGetResponseDTO
from asaas.models.account_document_save_request_account_document_type import AccountDocumentSaveRequestAccountDocumentType
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
    api_instance = asaas.EnvioDeDocumentosWhiteLabelApi(api_client)
    id = '8d257732-2220-11ec-b695-b6af4a64184d' # str | Identificador único do documento no Asaas
    document_file = None # bytes | Arquivo (optional)
    type = asaas.AccountDocumentSaveRequestAccountDocumentType() # AccountDocumentSaveRequestAccountDocumentType |  (optional)

    try:
        # Enviar documentos
        api_response = api_instance.enviar_documentos(id, document_file=document_file, type=type)
        print("The response of EnvioDeDocumentosWhiteLabelApi->enviar_documentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvioDeDocumentosWhiteLabelApi->enviar_documentos: %s\n" % e)
```

### Parameters

| Name              | Type                                                                                                  | Description                               | Notes      |
| ----------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------- | ---------- |
| **id**            | **str**                                                                                               | Identificador único do documento no Asaas |
| **document_file** | **bytes**                                                                                             | Arquivo                                   | [optional] |
| **type**          | [**AccountDocumentSaveRequestAccountDocumentType**](AccountDocumentSaveRequestAccountDocumentType.md) |                                           | [optional] |

### Return type

[**AccountDocumentGetResponseDTO**](AccountDocumentGetResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **remover_documento_enviado**

> AccountDocumentDeleteResponseDTO remover_documento_enviado(id)

Remover documento enviado

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_document_delete_response_dto import AccountDocumentDeleteResponseDTO
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
    api_instance = asaas.EnvioDeDocumentosWhiteLabelApi(api_client)
    id = '8d257732-2220-11ec-b695-b6af4a64184d' # str | Identificador único do documento no Asaas

    try:
        # Remover documento enviado
        api_response = api_instance.remover_documento_enviado(id)
        print("The response of EnvioDeDocumentosWhiteLabelApi->remover_documento_enviado:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvioDeDocumentosWhiteLabelApi->remover_documento_enviado: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                               | Notes |
| ------ | ------- | ----------------------------------------- | ----- |
| **id** | **str** | Identificador único do documento no Asaas |

### Return type

[**AccountDocumentDeleteResponseDTO**](AccountDocumentDeleteResponseDTO.md)

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

# **verificar_documentos_pendentes**

> AccountDocumentShowResponseDTO verificar_documentos_pendentes()

Verificar documentos pendentes

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_document_show_response_dto import AccountDocumentShowResponseDTO
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
    api_instance = asaas.EnvioDeDocumentosWhiteLabelApi(api_client)

    try:
        # Verificar documentos pendentes
        api_response = api_instance.verificar_documentos_pendentes()
        print("The response of EnvioDeDocumentosWhiteLabelApi->verificar_documentos_pendentes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvioDeDocumentosWhiteLabelApi->verificar_documentos_pendentes: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountDocumentShowResponseDTO**](AccountDocumentShowResponseDTO.md)

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

# **visualizar_documento_enviado**

> AccountDocumentGetResponseDTO visualizar_documento_enviado(id)

Visualizar documento enviado

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_document_get_response_dto import AccountDocumentGetResponseDTO
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
    api_instance = asaas.EnvioDeDocumentosWhiteLabelApi(api_client)
    id = '8d257732-2220-11ec-b695-b6af4a64184d' # str | Identificador único do documento no Asaas

    try:
        # Visualizar documento enviado
        api_response = api_instance.visualizar_documento_enviado(id)
        print("The response of EnvioDeDocumentosWhiteLabelApi->visualizar_documento_enviado:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvioDeDocumentosWhiteLabelApi->visualizar_documento_enviado: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                               | Notes |
| ------ | ------- | ----------------------------------------- | ----- |
| **id** | **str** | Identificador único do documento no Asaas |

### Return type

[**AccountDocumentGetResponseDTO**](AccountDocumentGetResponseDTO.md)

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
