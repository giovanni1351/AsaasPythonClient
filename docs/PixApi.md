# asaas.PixApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**consulta_de_fichas_disponiveis_no_balde**](PixApi.md#consulta_de_fichas_disponiveis_no_balde) | **GET** /v3/pix/tokenBucket/addressKey | Consulta de fichas disponíveis no balde
[**criar_qrcode_estatico**](PixApi.md#criar_qrcode_estatico) | **POST** /v3/pix/qrCodes/static | Criar QR Code estático
[**criar_uma_chave**](PixApi.md#criar_uma_chave) | **POST** /v3/pix/addressKeys | Criar uma chave
[**deletar_qrcode_estatico**](PixApi.md#deletar_qrcode_estatico) | **DELETE** /v3/pix/qrCodes/static/{id} | Deletar QR Code estático
[**listar_chaves**](PixApi.md#listar_chaves) | **GET** /v3/pix/addressKeys | Listar chaves
[**recuperar_uma_unica_chave**](PixApi.md#recuperar_uma_unica_chave) | **GET** /v3/pix/addressKeys/{id} | Recuperar uma única chave
[**remover_chave**](PixApi.md#remover_chave) | **DELETE** /v3/pix/addressKeys/{id} | Remover chave


# **consulta_de_fichas_disponiveis_no_balde**
> PixTokenBucketGetAddressKeyResponseDTO consulta_de_fichas_disponiveis_no_balde()

Consulta de fichas disponíveis no balde



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_token_bucket_get_address_key_response_dto import PixTokenBucketGetAddressKeyResponseDTO
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
    api_instance = asaas.PixApi(api_client)

    try:
        # Consulta de fichas disponíveis no balde
        api_response = api_instance.consulta_de_fichas_disponiveis_no_balde()
        print("The response of PixApi->consulta_de_fichas_disponiveis_no_balde:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->consulta_de_fichas_disponiveis_no_balde: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**PixTokenBucketGetAddressKeyResponseDTO**](PixTokenBucketGetAddressKeyResponseDTO.md)

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

# **criar_qrcode_estatico**
> PixQrCodeSaveResponseDTO criar_qrcode_estatico(pix_qr_code_save_request_dto=pix_qr_code_save_request_dto)

Criar QR Code estático



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_qr_code_save_request_dto import PixQrCodeSaveRequestDTO
from asaas.models.pix_qr_code_save_response_dto import PixQrCodeSaveResponseDTO
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
    api_instance = asaas.PixApi(api_client)
    pix_qr_code_save_request_dto = asaas.PixQrCodeSaveRequestDTO() # PixQrCodeSaveRequestDTO |  (optional)

    try:
        # Criar QR Code estático
        api_response = api_instance.criar_qrcode_estatico(pix_qr_code_save_request_dto=pix_qr_code_save_request_dto)
        print("The response of PixApi->criar_qrcode_estatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->criar_qrcode_estatico: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pix_qr_code_save_request_dto** | [**PixQrCodeSaveRequestDTO**](PixQrCodeSaveRequestDTO.md)|  | [optional] 

### Return type

[**PixQrCodeSaveResponseDTO**](PixQrCodeSaveResponseDTO.md)

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

# **criar_uma_chave**
> PixAddressKeyGetResponseDTO criar_uma_chave(pix_address_key_save_request_dto=pix_address_key_save_request_dto)

Criar uma chave



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_address_key_get_response_dto import PixAddressKeyGetResponseDTO
from asaas.models.pix_address_key_save_request_dto import PixAddressKeySaveRequestDTO
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
    api_instance = asaas.PixApi(api_client)
    pix_address_key_save_request_dto = asaas.PixAddressKeySaveRequestDTO() # PixAddressKeySaveRequestDTO |  (optional)

    try:
        # Criar uma chave
        api_response = api_instance.criar_uma_chave(pix_address_key_save_request_dto=pix_address_key_save_request_dto)
        print("The response of PixApi->criar_uma_chave:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->criar_uma_chave: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pix_address_key_save_request_dto** | [**PixAddressKeySaveRequestDTO**](PixAddressKeySaveRequestDTO.md)|  | [optional] 

### Return type

[**PixAddressKeyGetResponseDTO**](PixAddressKeyGetResponseDTO.md)

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

# **deletar_qrcode_estatico**
> PixQrCodeDeleteResponseDTO deletar_qrcode_estatico(id)

Deletar QR Code estático



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_qr_code_delete_response_dto import PixQrCodeDeleteResponseDTO
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
    api_instance = asaas.PixApi(api_client)
    id = 'ASAAS00000000000000383ASA' # str | Identificador do QR Code que será removido.

    try:
        # Deletar QR Code estático
        api_response = api_instance.deletar_qrcode_estatico(id)
        print("The response of PixApi->deletar_qrcode_estatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->deletar_qrcode_estatico: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador do QR Code que será removido. | 

### Return type

[**PixQrCodeDeleteResponseDTO**](PixQrCodeDeleteResponseDTO.md)

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

# **listar_chaves**
> PixAddressKeyListResponseDTO listar_chaves(offset=offset, limit=limit, status=status, status_list=status_list)

Listar chaves



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_address_key_list_request_pix_address_key_status import PixAddressKeyListRequestPixAddressKeyStatus
from asaas.models.pix_address_key_list_response_dto import PixAddressKeyListResponseDTO
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
    api_instance = asaas.PixApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    status = asaas.PixAddressKeyListRequestPixAddressKeyStatus() # PixAddressKeyListRequestPixAddressKeyStatus | Filtrar pelo status atual da chave (optional)
    status_list = 'status_list_example' # str | Filtrar por um ou mais status das chaves (optional)

    try:
        # Listar chaves
        api_response = api_instance.listar_chaves(offset=offset, limit=limit, status=status, status_list=status_list)
        print("The response of PixApi->listar_chaves:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->listar_chaves: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **status** | [**PixAddressKeyListRequestPixAddressKeyStatus**](.md)| Filtrar pelo status atual da chave | [optional] 
 **status_list** | **str**| Filtrar por um ou mais status das chaves | [optional] 

### Return type

[**PixAddressKeyListResponseDTO**](PixAddressKeyListResponseDTO.md)

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

# **recuperar_uma_unica_chave**
> PixAddressKeyGetResponseDTO recuperar_uma_unica_chave(id)

Recuperar uma única chave



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_address_key_get_response_dto import PixAddressKeyGetResponseDTO
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
    api_instance = asaas.PixApi(api_client)
    id = 'a33047b1-fb19-4b68-9373-a7ba8a8162aa' # str | Identificador único da chave Pix no Asaas

    try:
        # Recuperar uma única chave
        api_response = api_instance.recuperar_uma_unica_chave(id)
        print("The response of PixApi->recuperar_uma_unica_chave:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->recuperar_uma_unica_chave: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da chave Pix no Asaas | 

### Return type

[**PixAddressKeyGetResponseDTO**](PixAddressKeyGetResponseDTO.md)

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

# **remover_chave**
> PixAddressKeyGetResponseDTO remover_chave(id)

Remover chave



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_address_key_get_response_dto import PixAddressKeyGetResponseDTO
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
    api_instance = asaas.PixApi(api_client)
    id = 'a33047b1-fb19-4b68-9373-a7ba8a8162aa' # str | Identificador único da chave Pix no Asaas

    try:
        # Remover chave
        api_response = api_instance.remover_chave(id)
        print("The response of PixApi->remover_chave:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixApi->remover_chave: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da chave Pix no Asaas | 

### Return type

[**PixAddressKeyGetResponseDTO**](PixAddressKeyGetResponseDTO.md)

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

