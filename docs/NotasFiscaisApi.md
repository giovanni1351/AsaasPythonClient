# asaas.NotasFiscaisApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**agendar_nota_fiscal**](NotasFiscaisApi.md#agendar_nota_fiscal) | **POST** /v3/invoices | Agendar nota fiscal
[**atualizar_nota_fiscal**](NotasFiscaisApi.md#atualizar_nota_fiscal) | **PUT** /v3/invoices/{id} | Atualizar nota fiscal
[**cancelar_uma_nota_fiscal**](NotasFiscaisApi.md#cancelar_uma_nota_fiscal) | **POST** /v3/invoices/{id}/cancel | Cancelar uma nota fiscal
[**emitir_uma_nota_fiscal**](NotasFiscaisApi.md#emitir_uma_nota_fiscal) | **POST** /v3/invoices/{id}/authorize | Emitir uma nota fiscal
[**listar_notas_fiscais**](NotasFiscaisApi.md#listar_notas_fiscais) | **GET** /v3/invoices | Listar notas fiscais
[**recuperar_uma_nota_fiscal**](NotasFiscaisApi.md#recuperar_uma_nota_fiscal) | **GET** /v3/invoices/{id} | Recuperar uma única nota fiscal


# **agendar_nota_fiscal**
> InvoiceGetResponseDTO agendar_nota_fiscal(invoice_save_request_dto=invoice_save_request_dto)

Agendar nota fiscal



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_get_response_dto import InvoiceGetResponseDTO
from asaas.models.invoice_save_request_dto import InvoiceSaveRequestDTO
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
    api_instance = asaas.NotasFiscaisApi(api_client)
    invoice_save_request_dto = asaas.InvoiceSaveRequestDTO() # InvoiceSaveRequestDTO |  (optional)

    try:
        # Agendar nota fiscal
        api_response = api_instance.agendar_nota_fiscal(invoice_save_request_dto=invoice_save_request_dto)
        print("The response of NotasFiscaisApi->agendar_nota_fiscal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotasFiscaisApi->agendar_nota_fiscal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invoice_save_request_dto** | [**InvoiceSaveRequestDTO**](InvoiceSaveRequestDTO.md)|  | [optional] 

### Return type

[**InvoiceGetResponseDTO**](InvoiceGetResponseDTO.md)

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

# **atualizar_nota_fiscal**
> InvoiceGetResponseDTO atualizar_nota_fiscal(id, invoice_update_request_dto=invoice_update_request_dto)

Atualizar nota fiscal



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_get_response_dto import InvoiceGetResponseDTO
from asaas.models.invoice_update_request_dto import InvoiceUpdateRequestDTO
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
    api_instance = asaas.NotasFiscaisApi(api_client)
    id = 'inv_000000000232' # str | Identificador único da nota fiscal no Asaas
    invoice_update_request_dto = asaas.InvoiceUpdateRequestDTO() # InvoiceUpdateRequestDTO |  (optional)

    try:
        # Atualizar nota fiscal
        api_response = api_instance.atualizar_nota_fiscal(id, invoice_update_request_dto=invoice_update_request_dto)
        print("The response of NotasFiscaisApi->atualizar_nota_fiscal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotasFiscaisApi->atualizar_nota_fiscal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da nota fiscal no Asaas | 
 **invoice_update_request_dto** | [**InvoiceUpdateRequestDTO**](InvoiceUpdateRequestDTO.md)|  | [optional] 

### Return type

[**InvoiceGetResponseDTO**](InvoiceGetResponseDTO.md)

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

# **cancelar_uma_nota_fiscal**
> InvoiceGetResponseDTO cancelar_uma_nota_fiscal(id, invoice_cancel_request_dto=invoice_cancel_request_dto)

Cancelar uma nota fiscal



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_cancel_request_dto import InvoiceCancelRequestDTO
from asaas.models.invoice_get_response_dto import InvoiceGetResponseDTO
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
    api_instance = asaas.NotasFiscaisApi(api_client)
    id = 'inv_000000000232' # str | Identificador único da nota fiscal no Asaas
    invoice_cancel_request_dto = asaas.InvoiceCancelRequestDTO() # InvoiceCancelRequestDTO |  (optional)

    try:
        # Cancelar uma nota fiscal
        api_response = api_instance.cancelar_uma_nota_fiscal(id, invoice_cancel_request_dto=invoice_cancel_request_dto)
        print("The response of NotasFiscaisApi->cancelar_uma_nota_fiscal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotasFiscaisApi->cancelar_uma_nota_fiscal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da nota fiscal no Asaas | 
 **invoice_cancel_request_dto** | [**InvoiceCancelRequestDTO**](InvoiceCancelRequestDTO.md)|  | [optional] 

### Return type

[**InvoiceGetResponseDTO**](InvoiceGetResponseDTO.md)

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

# **emitir_uma_nota_fiscal**
> InvoiceGetResponseDTO emitir_uma_nota_fiscal(id, body=body)

Emitir uma nota fiscal



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_get_response_dto import InvoiceGetResponseDTO
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
    api_instance = asaas.NotasFiscaisApi(api_client)
    id = 'inv_000000000232' # str | Identificador único da nota fiscal no Asaas
    body = None # object |  (optional)

    try:
        # Emitir uma nota fiscal
        api_response = api_instance.emitir_uma_nota_fiscal(id, body=body)
        print("The response of NotasFiscaisApi->emitir_uma_nota_fiscal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotasFiscaisApi->emitir_uma_nota_fiscal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da nota fiscal no Asaas | 
 **body** | **object**|  | [optional] 

### Return type

[**InvoiceGetResponseDTO**](InvoiceGetResponseDTO.md)

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

# **listar_notas_fiscais**
> InvoiceListResponseDTO listar_notas_fiscais(offset=offset, limit=limit, effective_date_ge=effective_date_ge, effective_date_le=effective_date_le, payment=payment, installment=installment, external_reference=external_reference, status=status, customer=customer)

Listar notas fiscais



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_list_request_invoice_status import InvoiceListRequestInvoiceStatus
from asaas.models.invoice_list_response_dto import InvoiceListResponseDTO
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
    api_instance = asaas.NotasFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    effective_date_ge = '2024-08-03' # str | Filtrar a partir de uma data de emissão (optional)
    effective_date_le = '2024-09-03' # str | Filtrar até uma data de emissão (optional)
    payment = 'payment_example' # str | Filtrar pelo identificador único da cobrança (optional)
    installment = 'installment_example' # str | Filtrar pelo identificador único do parcelamento (optional)
    external_reference = 'external_reference_example' # str | Filtrar pelo identificador da nota fiscal no seu sistema (optional)
    status = asaas.InvoiceListRequestInvoiceStatus() # InvoiceListRequestInvoiceStatus | Filtrar por situação (optional)
    customer = 'customer_example' # str | Filtrar pelo identificador único do cliente (optional)

    try:
        # Listar notas fiscais
        api_response = api_instance.listar_notas_fiscais(offset=offset, limit=limit, effective_date_ge=effective_date_ge, effective_date_le=effective_date_le, payment=payment, installment=installment, external_reference=external_reference, status=status, customer=customer)
        print("The response of NotasFiscaisApi->listar_notas_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotasFiscaisApi->listar_notas_fiscais: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **effective_date_ge** | **str**| Filtrar a partir de uma data de emissão | [optional] 
 **effective_date_le** | **str**| Filtrar até uma data de emissão | [optional] 
 **payment** | **str**| Filtrar pelo identificador único da cobrança | [optional] 
 **installment** | **str**| Filtrar pelo identificador único do parcelamento | [optional] 
 **external_reference** | **str**| Filtrar pelo identificador da nota fiscal no seu sistema | [optional] 
 **status** | [**InvoiceListRequestInvoiceStatus**](.md)| Filtrar por situação | [optional] 
 **customer** | **str**| Filtrar pelo identificador único do cliente | [optional] 

### Return type

[**InvoiceListResponseDTO**](InvoiceListResponseDTO.md)

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

# **recuperar_uma_nota_fiscal**
> InvoiceGetResponseDTO recuperar_uma_nota_fiscal(id)

Recuperar uma única nota fiscal



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_get_response_dto import InvoiceGetResponseDTO
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
    api_instance = asaas.NotasFiscaisApi(api_client)
    id = 'inv_000000000232' # str | Identificador único da nota fiscal no Asaas

    try:
        # Recuperar uma única nota fiscal
        api_response = api_instance.recuperar_uma_nota_fiscal(id)
        print("The response of NotasFiscaisApi->recuperar_uma_nota_fiscal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NotasFiscaisApi->recuperar_uma_nota_fiscal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da nota fiscal no Asaas | 

### Return type

[**InvoiceGetResponseDTO**](InvoiceGetResponseDTO.md)

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

