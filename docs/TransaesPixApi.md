# asaas.TransaesPixApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelar_uma_transacao_agendada**](TransaesPixApi.md#cancelar_uma_transacao_agendada) | **POST** /v3/pix/transactions/{id}/cancel | Cancelar uma transação agendada
[**decodificar_um_qrcode_para_pagamento**](TransaesPixApi.md#decodificar_um_qrcode_para_pagamento) | **POST** /v3/pix/qrCodes/decode | Decodificar um QRCode para pagamento
[**listar_transacoes**](TransaesPixApi.md#listar_transacoes) | **GET** /v3/pix/transactions | Listar transações
[**pagar_um_qrcode**](TransaesPixApi.md#pagar_um_qrcode) | **POST** /v3/pix/qrCodes/pay | Pagar um QRCode
[**recuperar_uma_unica_transacao**](TransaesPixApi.md#recuperar_uma_unica_transacao) | **GET** /v3/pix/transactions/{id} | Recuperar uma única transação


# **cancelar_uma_transacao_agendada**
> PixTransactionGetResponseDTO cancelar_uma_transacao_agendada(id, body=body)

Cancelar uma transação agendada



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_transaction_get_response_dto import PixTransactionGetResponseDTO
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
    api_instance = asaas.TransaesPixApi(api_client)
    id = 'id_example' # str | Identificador único da transação Pix agendada a ser cancelada.
    body = None # object |  (optional)

    try:
        # Cancelar uma transação agendada
        api_response = api_instance.cancelar_uma_transacao_agendada(id, body=body)
        print("The response of TransaesPixApi->cancelar_uma_transacao_agendada:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransaesPixApi->cancelar_uma_transacao_agendada: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da transação Pix agendada a ser cancelada. | 
 **body** | **object**|  | [optional] 

### Return type

[**PixTransactionGetResponseDTO**](PixTransactionGetResponseDTO.md)

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

# **decodificar_um_qrcode_para_pagamento**
> PixQrCodeDecodeResponseDTO decodificar_um_qrcode_para_pagamento(pix_qr_code_decode_request_dto=pix_qr_code_decode_request_dto)

Decodificar um QRCode para pagamento



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_qr_code_decode_request_dto import PixQrCodeDecodeRequestDTO
from asaas.models.pix_qr_code_decode_response_dto import PixQrCodeDecodeResponseDTO
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
    api_instance = asaas.TransaesPixApi(api_client)
    pix_qr_code_decode_request_dto = asaas.PixQrCodeDecodeRequestDTO() # PixQrCodeDecodeRequestDTO |  (optional)

    try:
        # Decodificar um QRCode para pagamento
        api_response = api_instance.decodificar_um_qrcode_para_pagamento(pix_qr_code_decode_request_dto=pix_qr_code_decode_request_dto)
        print("The response of TransaesPixApi->decodificar_um_qrcode_para_pagamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransaesPixApi->decodificar_um_qrcode_para_pagamento: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pix_qr_code_decode_request_dto** | [**PixQrCodeDecodeRequestDTO**](PixQrCodeDecodeRequestDTO.md)|  | [optional] 

### Return type

[**PixQrCodeDecodeResponseDTO**](PixQrCodeDecodeResponseDTO.md)

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

# **listar_transacoes**
> PixTransactionListResponseDTO listar_transacoes(offset=offset, limit=limit, status=status, type=type, end_to_end_identifier=end_to_end_identifier)

Listar transações



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_transaction_list_request_pix_transaction_status import PixTransactionListRequestPixTransactionStatus
from asaas.models.pix_transaction_list_request_pix_transaction_type import PixTransactionListRequestPixTransactionType
from asaas.models.pix_transaction_list_response_dto import PixTransactionListResponseDTO
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
    api_instance = asaas.TransaesPixApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    status = asaas.PixTransactionListRequestPixTransactionStatus() # PixTransactionListRequestPixTransactionStatus | Filtrar por status da transação (optional)
    type = asaas.PixTransactionListRequestPixTransactionType() # PixTransactionListRequestPixTransactionType | Filtrar por tipo da transação (optional)
    end_to_end_identifier = 'end_to_end_identifier_example' # str | Filtrar pelo identificador da transação Pix no Banco Central (optional)

    try:
        # Listar transações
        api_response = api_instance.listar_transacoes(offset=offset, limit=limit, status=status, type=type, end_to_end_identifier=end_to_end_identifier)
        print("The response of TransaesPixApi->listar_transacoes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransaesPixApi->listar_transacoes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **status** | [**PixTransactionListRequestPixTransactionStatus**](.md)| Filtrar por status da transação | [optional] 
 **type** | [**PixTransactionListRequestPixTransactionType**](.md)| Filtrar por tipo da transação | [optional] 
 **end_to_end_identifier** | **str**| Filtrar pelo identificador da transação Pix no Banco Central | [optional] 

### Return type

[**PixTransactionListResponseDTO**](PixTransactionListResponseDTO.md)

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

# **pagar_um_qrcode**
> PixTransactionGetResponseDTO pagar_um_qrcode(pix_transaction_save_request_dto=pix_transaction_save_request_dto)

Pagar um QRCode



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_transaction_get_response_dto import PixTransactionGetResponseDTO
from asaas.models.pix_transaction_save_request_dto import PixTransactionSaveRequestDTO
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
    api_instance = asaas.TransaesPixApi(api_client)
    pix_transaction_save_request_dto = asaas.PixTransactionSaveRequestDTO() # PixTransactionSaveRequestDTO |  (optional)

    try:
        # Pagar um QRCode
        api_response = api_instance.pagar_um_qrcode(pix_transaction_save_request_dto=pix_transaction_save_request_dto)
        print("The response of TransaesPixApi->pagar_um_qrcode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransaesPixApi->pagar_um_qrcode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pix_transaction_save_request_dto** | [**PixTransactionSaveRequestDTO**](PixTransactionSaveRequestDTO.md)|  | [optional] 

### Return type

[**PixTransactionGetResponseDTO**](PixTransactionGetResponseDTO.md)

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

# **recuperar_uma_unica_transacao**
> PixTransactionGetResponseDTO recuperar_uma_unica_transacao(id)

Recuperar uma única transação



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_transaction_get_response_dto import PixTransactionGetResponseDTO
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
    api_instance = asaas.TransaesPixApi(api_client)
    id = '35363f6e-93e2-11ec-b9d9-96f4053b1bd4' # str | Identificador único da transação Pix no Asaas

    try:
        # Recuperar uma única transação
        api_response = api_instance.recuperar_uma_unica_transacao(id)
        print("The response of TransaesPixApi->recuperar_uma_unica_transacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransaesPixApi->recuperar_uma_unica_transacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da transação Pix no Asaas | 

### Return type

[**PixTransactionGetResponseDTO**](PixTransactionGetResponseDTO.md)

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

