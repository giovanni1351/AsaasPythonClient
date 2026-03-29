# asaas.DocumentosDeCobranasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                              | HTTP request                                        | Description                                      |
| ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------ |
| [**atualizar_definicoes_de_um_documento_da_cobranca**](DocumentosDeCobranasApi.md#atualizar_definicoes_de_um_documento_da_cobranca) | **PUT** /v3/payments/{id}/documents/{documentId}    | Atualizar definições de um documento da cobrança |
| [**excluir_documento_de_uma_cobranca**](DocumentosDeCobranasApi.md#excluir_documento_de_uma_cobranca)                               | **DELETE** /v3/payments/{id}/documents/{documentId} | Excluir documento de uma cobrança                |
| [**fazer_upload_de_documentos_da_cobranca**](DocumentosDeCobranasApi.md#fazer_upload_de_documentos_da_cobranca)                     | **POST** /v3/payments/{id}/documents                | Fazer upload de documentos da cobrança           |
| [**listar_documentos_de_uma_cobranca**](DocumentosDeCobranasApi.md#listar_documentos_de_uma_cobranca)                               | **GET** /v3/payments/{id}/documents                 | Listar documentos de uma cobrança                |
| [**recuperar_um_unico_documento_da_cobranca**](DocumentosDeCobranasApi.md#recuperar_um_unico_documento_da_cobranca)                 | **GET** /v3/payments/{id}/documents/{documentId}    | Recuperar um único documento da cobrança         |

# **atualizar_definicoes_de_um_documento_da_cobranca**

> PaymentDocumentGetResponseDTO atualizar_definicoes_de_um_documento_da_cobranca(id, document_id, payment_document_update_request_dto=payment_document_update_request_dto)

Atualizar definições de um documento da cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_document_get_response_dto import PaymentDocumentGetResponseDTO
from asaas.models.payment_document_update_request_dto import PaymentDocumentUpdateRequestDTO
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
    api_instance = asaas.DocumentosDeCobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    document_id = 'document_id_example' # str | Identificador único do documento
    payment_document_update_request_dto = asaas.PaymentDocumentUpdateRequestDTO() # PaymentDocumentUpdateRequestDTO |  (optional)

    try:
        # Atualizar definições de um documento da cobrança
        api_response = api_instance.atualizar_definicoes_de_um_documento_da_cobranca(id, document_id, payment_document_update_request_dto=payment_document_update_request_dto)
        print("The response of DocumentosDeCobranasApi->atualizar_definicoes_de_um_documento_da_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentosDeCobranasApi->atualizar_definicoes_de_um_documento_da_cobranca: %s\n" % e)
```

### Parameters

| Name                                    | Type                                                                      | Description                              | Notes      |
| --------------------------------------- | ------------------------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                                  | **str**                                                                   | Identificador único da cobrança no Asaas |
| **document_id**                         | **str**                                                                   | Identificador único do documento         |
| **payment_document_update_request_dto** | [**PaymentDocumentUpdateRequestDTO**](PaymentDocumentUpdateRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentDocumentGetResponseDTO**](PaymentDocumentGetResponseDTO.md)

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

# **excluir_documento_de_uma_cobranca**

> PaymentDocumentDeleteResponseDTO excluir_documento_de_uma_cobranca(id, document_id)

Excluir documento de uma cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_document_delete_response_dto import PaymentDocumentDeleteResponseDTO
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
    api_instance = asaas.DocumentosDeCobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    document_id = 'document_id_example' # str | Identificador único do documento

    try:
        # Excluir documento de uma cobrança
        api_response = api_instance.excluir_documento_de_uma_cobranca(id, document_id)
        print("The response of DocumentosDeCobranasApi->excluir_documento_de_uma_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentosDeCobranasApi->excluir_documento_de_uma_cobranca: %s\n" % e)
```

### Parameters

| Name            | Type    | Description                              | Notes |
| --------------- | ------- | ---------------------------------------- | ----- |
| **id**          | **str** | Identificador único da cobrança no Asaas |
| **document_id** | **str** | Identificador único do documento         |

### Return type

[**PaymentDocumentDeleteResponseDTO**](PaymentDocumentDeleteResponseDTO.md)

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

# **fazer_upload_de_documentos_da_cobranca**

> PaymentDocumentGetResponseDTO fazer_upload_de_documentos_da_cobranca(id, available_after_payment, type, file)

Fazer upload de documentos da cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_document_get_response_dto import PaymentDocumentGetResponseDTO
from asaas.models.payment_document_save_request_payment_document_type import PaymentDocumentSaveRequestPaymentDocumentType
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
    api_instance = asaas.DocumentosDeCobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    available_after_payment = True # bool | true para disponibilizar o documento apenas após o pagamento
    type = asaas.PaymentDocumentSaveRequestPaymentDocumentType() # PaymentDocumentSaveRequestPaymentDocumentType |
    file = None # bytes | Arquivo

    try:
        # Fazer upload de documentos da cobrança
        api_response = api_instance.fazer_upload_de_documentos_da_cobranca(id, available_after_payment, type, file)
        print("The response of DocumentosDeCobranasApi->fazer_upload_de_documentos_da_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentosDeCobranasApi->fazer_upload_de_documentos_da_cobranca: %s\n" % e)
```

### Parameters

| Name                        | Type                                                                                                  | Description                                                  | Notes |
| --------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| **id**                      | **str**                                                                                               | Identificador único da cobrança no Asaas                     |
| **available_after_payment** | **bool**                                                                                              | true para disponibilizar o documento apenas após o pagamento |
| **type**                    | [**PaymentDocumentSaveRequestPaymentDocumentType**](PaymentDocumentSaveRequestPaymentDocumentType.md) |                                                              |
| **file**                    | **bytes**                                                                                             | Arquivo                                                      |

### Return type

[**PaymentDocumentGetResponseDTO**](PaymentDocumentGetResponseDTO.md)

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

# **listar_documentos_de_uma_cobranca**

> PaymentDocumentListResponseDTO listar_documentos_de_uma_cobranca(id)

Listar documentos de uma cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_document_list_response_dto import PaymentDocumentListResponseDTO
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
    api_instance = asaas.DocumentosDeCobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Listar documentos de uma cobrança
        api_response = api_instance.listar_documentos_de_uma_cobranca(id)
        print("The response of DocumentosDeCobranasApi->listar_documentos_de_uma_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentosDeCobranasApi->listar_documentos_de_uma_cobranca: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentDocumentListResponseDTO**](PaymentDocumentListResponseDTO.md)

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

# **recuperar_um_unico_documento_da_cobranca**

> PaymentDocumentGetResponseDTO recuperar_um_unico_documento_da_cobranca(id, document_id)

Recuperar um único documento da cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_document_get_response_dto import PaymentDocumentGetResponseDTO
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
    api_instance = asaas.DocumentosDeCobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    document_id = 'document_id_example' # str | Identificador único do documento

    try:
        # Recuperar um único documento da cobrança
        api_response = api_instance.recuperar_um_unico_documento_da_cobranca(id, document_id)
        print("The response of DocumentosDeCobranasApi->recuperar_um_unico_documento_da_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentosDeCobranasApi->recuperar_um_unico_documento_da_cobranca: %s\n" % e)
```

### Parameters

| Name            | Type    | Description                              | Notes |
| --------------- | ------- | ---------------------------------------- | ----- |
| **id**          | **str** | Identificador único da cobrança no Asaas |
| **document_id** | **str** | Identificador único do documento         |

### Return type

[**PaymentDocumentGetResponseDTO**](PaymentDocumentGetResponseDTO.md)

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
