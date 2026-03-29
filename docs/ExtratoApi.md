# asaas.ExtratoApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**recuperar_extrato**](ExtratoApi.md#recuperar_extrato) | **GET** /v3/financialTransactions | Recuperar extrato


# **recuperar_extrato**
> FinancialTransactionListResponseDTO recuperar_extrato(offset=offset, limit=limit, start_date=start_date, finish_date=finish_date, order=order)

Recuperar extrato



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.financial_transaction_list_response_dto import FinancialTransactionListResponseDTO
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
    api_instance = asaas.ExtratoApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    start_date = '2023-03-01' # str | Data inicial da lista (optional)
    finish_date = '2023-03-31' # str | Data final da lista (optional)
    order = 'asc' # str | Ordenação do resultado (optional)

    try:
        # Recuperar extrato
        api_response = api_instance.recuperar_extrato(offset=offset, limit=limit, start_date=start_date, finish_date=finish_date, order=order)
        print("The response of ExtratoApi->recuperar_extrato:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ExtratoApi->recuperar_extrato: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **start_date** | **str**| Data inicial da lista | [optional] 
 **finish_date** | **str**| Data final da lista | [optional] 
 **order** | **str**| Ordenação do resultado | [optional] 

### Return type

[**FinancialTransactionListResponseDTO**](FinancialTransactionListResponseDTO.md)

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

