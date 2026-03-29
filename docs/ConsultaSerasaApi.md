# asaas.ConsultaSerasaApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**listar_consultas**](ConsultaSerasaApi.md#listar_consultas) | **GET** /v3/creditBureauReport | Listar consultas
[**realizar_consulta**](ConsultaSerasaApi.md#realizar_consulta) | **POST** /v3/creditBureauReport | Realizar consulta
[**recuperar_uma_consulta**](ConsultaSerasaApi.md#recuperar_uma_consulta) | **GET** /v3/creditBureauReport/{id} | Recuperar uma consulta


# **listar_consultas**
> CreditBureauReportListResponseDTO listar_consultas(offset=offset, limit=limit, start_date=start_date, end_date=end_date)

Listar consultas



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.credit_bureau_report_list_response_dto import CreditBureauReportListResponseDTO
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
    api_instance = asaas.ConsultaSerasaApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    start_date = 'start_date_example' # str | Filtrar a partir da data de criação (optional)
    end_date = 'end_date_example' # str | Filtrar até uma data de criação (optional)

    try:
        # Listar consultas
        api_response = api_instance.listar_consultas(offset=offset, limit=limit, start_date=start_date, end_date=end_date)
        print("The response of ConsultaSerasaApi->listar_consultas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConsultaSerasaApi->listar_consultas: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **start_date** | **str**| Filtrar a partir da data de criação | [optional] 
 **end_date** | **str**| Filtrar até uma data de criação | [optional] 

### Return type

[**CreditBureauReportListResponseDTO**](CreditBureauReportListResponseDTO.md)

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

# **realizar_consulta**
> CreditBureauReportGetResponseDTO realizar_consulta(credit_bureau_report_save_request_dto=credit_bureau_report_save_request_dto)

Realizar consulta



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.credit_bureau_report_get_response_dto import CreditBureauReportGetResponseDTO
from asaas.models.credit_bureau_report_save_request_dto import CreditBureauReportSaveRequestDTO
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
    api_instance = asaas.ConsultaSerasaApi(api_client)
    credit_bureau_report_save_request_dto = asaas.CreditBureauReportSaveRequestDTO() # CreditBureauReportSaveRequestDTO |  (optional)

    try:
        # Realizar consulta
        api_response = api_instance.realizar_consulta(credit_bureau_report_save_request_dto=credit_bureau_report_save_request_dto)
        print("The response of ConsultaSerasaApi->realizar_consulta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConsultaSerasaApi->realizar_consulta: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **credit_bureau_report_save_request_dto** | [**CreditBureauReportSaveRequestDTO**](CreditBureauReportSaveRequestDTO.md)|  | [optional] 

### Return type

[**CreditBureauReportGetResponseDTO**](CreditBureauReportGetResponseDTO.md)

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

# **recuperar_uma_consulta**
> CreditBureauReportGetResponseDTO recuperar_uma_consulta(id)

Recuperar uma consulta



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.credit_bureau_report_get_response_dto import CreditBureauReportGetResponseDTO
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
    api_instance = asaas.ConsultaSerasaApi(api_client)
    id = '6c5e73fa-9efd-4a75-b60c-1cafb8d1c7ed' # str | Identificador único da consulta no Asaas

    try:
        # Recuperar uma consulta
        api_response = api_instance.recuperar_uma_consulta(id)
        print("The response of ConsultaSerasaApi->recuperar_uma_consulta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ConsultaSerasaApi->recuperar_uma_consulta: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da consulta no Asaas | 

### Return type

[**CreditBureauReportGetResponseDTO**](CreditBureauReportGetResponseDTO.md)

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

