# asaas.EstornosApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**estornar_boleto**](EstornosApi.md#estornar_boleto) | **POST** /v3/payments/{id}/bankSlip/refund | Estornar boleto
[**listar_estornos_de_uma_cobranca**](EstornosApi.md#listar_estornos_de_uma_cobranca) | **GET** /v3/payments/{id}/refunds | Listar estornos de uma cobrança


# **estornar_boleto**
> PaymentBankSlipRefundResponseDTO estornar_boleto(id, body=body)

Estornar boleto



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_bank_slip_refund_response_dto import PaymentBankSlipRefundResponseDTO
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
    api_instance = asaas.EstornosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Estornar boleto
        api_response = api_instance.estornar_boleto(id, body=body)
        print("The response of EstornosApi->estornar_boleto:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EstornosApi->estornar_boleto: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da cobrança no Asaas | 
 **body** | **object**|  | [optional] 

### Return type

[**PaymentBankSlipRefundResponseDTO**](PaymentBankSlipRefundResponseDTO.md)

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

# **listar_estornos_de_uma_cobranca**
> PaymentRefundListResponseDTO listar_estornos_de_uma_cobranca(id)

Listar estornos de uma cobrança



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_refund_list_response_dto import PaymentRefundListResponseDTO
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
    api_instance = asaas.EstornosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Listar estornos de uma cobrança
        api_response = api_instance.listar_estornos_de_uma_cobranca(id)
        print("The response of EstornosApi->listar_estornos_de_uma_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EstornosApi->listar_estornos_de_uma_cobranca: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da cobrança no Asaas | 

### Return type

[**PaymentRefundListResponseDTO**](PaymentRefundListResponseDTO.md)

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

