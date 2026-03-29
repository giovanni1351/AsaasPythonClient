# asaas.SplitsApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listar_splits_pagos**](SplitsApi.md#listar_splits_pagos) | **GET** /v3/payments/splits/paid | Listar splits pagos
[**listar_splits_recebidos**](SplitsApi.md#listar_splits_recebidos) | **GET** /v3/payments/splits/received | Listar splits recebidos
[**recuperar_um_unico_split_pago**](SplitsApi.md#recuperar_um_unico_split_pago) | **GET** /v3/payments/splits/paid/{id} | Recuperar um único split pago
[**recuperar_um_unico_split_recebido**](SplitsApi.md#recuperar_um_unico_split_recebido) | **GET** /v3/payments/splits/received/{id} | Recuperar um único split recebido


# **listar_splits_pagos**
> PaymentSplitListResponseDTO listar_splits_pagos(offset=offset, limit=limit, payment_id=payment_id, status=status, payment_confirmed_date_ge=payment_confirmed_date_ge, payment_confirmed_date_le=payment_confirmed_date_le, credit_date_ge=credit_date_ge, credit_date_le=credit_date_le)

Listar splits pagos



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_split_list_paid_request_payment_split_status import PaymentSplitListPaidRequestPaymentSplitStatus
from asaas.models.payment_split_list_response_dto import PaymentSplitListResponseDTO
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
    api_instance = asaas.SplitsApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    payment_id = 'payment_id_example' # str | Filtrar pelo ID da cobrança (optional)
    status = asaas.PaymentSplitListPaidRequestPaymentSplitStatus() # PaymentSplitListPaidRequestPaymentSplitStatus | Filtrar por status (optional)
    payment_confirmed_date_ge = 'payment_confirmed_date_ge_example' # str | Filtrar a partir da data de confirmação da cobrança inicial (optional)
    payment_confirmed_date_le = 'payment_confirmed_date_le_example' # str | Filtrar a partir da data de confirmação da cobrança final (optional)
    credit_date_ge = 'credit_date_ge_example' # str | Filtrar a partir da data de envio do split inicial (optional)
    credit_date_le = 'credit_date_le_example' # str | Filtrar a partir da data de envio do split final (optional)

    try:
        # Listar splits pagos
        api_response = api_instance.listar_splits_pagos(offset=offset, limit=limit, payment_id=payment_id, status=status, payment_confirmed_date_ge=payment_confirmed_date_ge, payment_confirmed_date_le=payment_confirmed_date_le, credit_date_ge=credit_date_ge, credit_date_le=credit_date_le)
        print("The response of SplitsApi->listar_splits_pagos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SplitsApi->listar_splits_pagos: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **payment_id** | **str**| Filtrar pelo ID da cobrança | [optional] 
 **status** | [**PaymentSplitListPaidRequestPaymentSplitStatus**](.md)| Filtrar por status | [optional] 
 **payment_confirmed_date_ge** | **str**| Filtrar a partir da data de confirmação da cobrança inicial | [optional] 
 **payment_confirmed_date_le** | **str**| Filtrar a partir da data de confirmação da cobrança final | [optional] 
 **credit_date_ge** | **str**| Filtrar a partir da data de envio do split inicial | [optional] 
 **credit_date_le** | **str**| Filtrar a partir da data de envio do split final | [optional] 

### Return type

[**PaymentSplitListResponseDTO**](PaymentSplitListResponseDTO.md)

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

# **listar_splits_recebidos**
> PaymentSplitListResponseDTO listar_splits_recebidos(offset=offset, limit=limit, payment_id=payment_id, status=status, payment_confirmed_date_ge=payment_confirmed_date_ge, payment_confirmed_date_le=payment_confirmed_date_le, credit_date_ge=credit_date_ge, credit_date_le=credit_date_le)

Listar splits recebidos



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_split_list_received_request_payment_split_status import PaymentSplitListReceivedRequestPaymentSplitStatus
from asaas.models.payment_split_list_response_dto import PaymentSplitListResponseDTO
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
    api_instance = asaas.SplitsApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    payment_id = 'payment_id_example' # str | Filtrar pelo ID da cobrança (optional)
    status = asaas.PaymentSplitListReceivedRequestPaymentSplitStatus() # PaymentSplitListReceivedRequestPaymentSplitStatus | Filtrar por status (optional)
    payment_confirmed_date_ge = 'payment_confirmed_date_ge_example' # str | Filtrar a partir da data de confirmação da cobrança inicial (optional)
    payment_confirmed_date_le = 'payment_confirmed_date_le_example' # str | Filtrar a partir da data de confirmação da cobrança final (optional)
    credit_date_ge = 'credit_date_ge_example' # str | Filtrar a partir da data de recebimento do split inicial (optional)
    credit_date_le = 'credit_date_le_example' # str | Filtrar a partir da data de recebimento do split final (optional)

    try:
        # Listar splits recebidos
        api_response = api_instance.listar_splits_recebidos(offset=offset, limit=limit, payment_id=payment_id, status=status, payment_confirmed_date_ge=payment_confirmed_date_ge, payment_confirmed_date_le=payment_confirmed_date_le, credit_date_ge=credit_date_ge, credit_date_le=credit_date_le)
        print("The response of SplitsApi->listar_splits_recebidos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SplitsApi->listar_splits_recebidos: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **payment_id** | **str**| Filtrar pelo ID da cobrança | [optional] 
 **status** | [**PaymentSplitListReceivedRequestPaymentSplitStatus**](.md)| Filtrar por status | [optional] 
 **payment_confirmed_date_ge** | **str**| Filtrar a partir da data de confirmação da cobrança inicial | [optional] 
 **payment_confirmed_date_le** | **str**| Filtrar a partir da data de confirmação da cobrança final | [optional] 
 **credit_date_ge** | **str**| Filtrar a partir da data de recebimento do split inicial | [optional] 
 **credit_date_le** | **str**| Filtrar a partir da data de recebimento do split final | [optional] 

### Return type

[**PaymentSplitListResponseDTO**](PaymentSplitListResponseDTO.md)

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

# **recuperar_um_unico_split_pago**
> PaymentSplitGetFullResponseDTO recuperar_um_unico_split_pago(id)

Recuperar um único split pago



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_split_get_full_response_dto import PaymentSplitGetFullResponseDTO
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
    api_instance = asaas.SplitsApi(api_client)
    id = 'id_example' # str | Identificador único do split pago no Asaas

    try:
        # Recuperar um único split pago
        api_response = api_instance.recuperar_um_unico_split_pago(id)
        print("The response of SplitsApi->recuperar_um_unico_split_pago:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SplitsApi->recuperar_um_unico_split_pago: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único do split pago no Asaas | 

### Return type

[**PaymentSplitGetFullResponseDTO**](PaymentSplitGetFullResponseDTO.md)

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

# **recuperar_um_unico_split_recebido**
> PaymentSplitGetFullResponseDTO recuperar_um_unico_split_recebido(id)

Recuperar um único split recebido



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_split_get_full_response_dto import PaymentSplitGetFullResponseDTO
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
    api_instance = asaas.SplitsApi(api_client)
    id = 'id_example' # str | Identificador único do split pago no Asaas

    try:
        # Recuperar um único split recebido
        api_response = api_instance.recuperar_um_unico_split_recebido(id)
        print("The response of SplitsApi->recuperar_um_unico_split_recebido:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SplitsApi->recuperar_um_unico_split_recebido: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único do split pago no Asaas | 

### Return type

[**PaymentSplitGetFullResponseDTO**](PaymentSplitGetFullResponseDTO.md)

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

