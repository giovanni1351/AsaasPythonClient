# asaas.RecargasDeCelularApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga**](RecargasDeCelularApi.md#buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga) | **GET** /v3/mobilePhoneRecharges/{phoneNumber}/provider | Buscar qual provedor o número pertence e os valores disponíveis para recarga
[**cancelar_uma_recarga_de_celular**](RecargasDeCelularApi.md#cancelar_uma_recarga_de_celular) | **POST** /v3/mobilePhoneRecharges/{id}/cancel | Cancelar uma recarga de celular
[**listar_recargas_de_celular**](RecargasDeCelularApi.md#listar_recargas_de_celular) | **GET** /v3/mobilePhoneRecharges | Listar recargas de celular
[**recuperar_uma_unica_recarga_de_celular**](RecargasDeCelularApi.md#recuperar_uma_unica_recarga_de_celular) | **GET** /v3/mobilePhoneRecharges/{id} | Recuperar uma única recarga de celular
[**solicitar_recarga**](RecargasDeCelularApi.md#solicitar_recarga) | **POST** /v3/mobilePhoneRecharges | Solicitar recarga


# **buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga**
> MobilePhoneRechargeFindProviderResponseDTO buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga(phone_number)

Buscar qual provedor o número pertence e os valores disponíveis para recarga



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.mobile_phone_recharge_find_provider_response_dto import MobilePhoneRechargeFindProviderResponseDTO
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
    api_instance = asaas.RecargasDeCelularApi(api_client)
    phone_number = '63997365512' # str | Número do celular que será consultado.

    try:
        # Buscar qual provedor o número pertence e os valores disponíveis para recarga
        api_response = api_instance.buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga(phone_number)
        print("The response of RecargasDeCelularApi->buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecargasDeCelularApi->buscar_qual_provedor_o_numero_pertence_eos_valores_disponiveis_para_recarga: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **phone_number** | **str**| Número do celular que será consultado. | 

### Return type

[**MobilePhoneRechargeFindProviderResponseDTO**](MobilePhoneRechargeFindProviderResponseDTO.md)

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

# **cancelar_uma_recarga_de_celular**
> MobilePhoneRechargeGetResponseDTO cancelar_uma_recarga_de_celular(id, body=body)

Cancelar uma recarga de celular

Permite o cancelamento da recarga de celular. Utilize a propriedade `canBeCancelled` para verificar se a recarga pode ser cancelada. Ao ser cancelado a recarga não será realizada.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.mobile_phone_recharge_get_response_dto import MobilePhoneRechargeGetResponseDTO
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
    api_instance = asaas.RecargasDeCelularApi(api_client)
    id = '37c22147-4194-11ec-8061-0242ac120002' # str | Identificador único da recarga de celular no Asaas
    body = None # object |  (optional)

    try:
        # Cancelar uma recarga de celular
        api_response = api_instance.cancelar_uma_recarga_de_celular(id, body=body)
        print("The response of RecargasDeCelularApi->cancelar_uma_recarga_de_celular:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecargasDeCelularApi->cancelar_uma_recarga_de_celular: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da recarga de celular no Asaas | 
 **body** | **object**|  | [optional] 

### Return type

[**MobilePhoneRechargeGetResponseDTO**](MobilePhoneRechargeGetResponseDTO.md)

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

# **listar_recargas_de_celular**
> MobilePhoneRechargeListResponseDTO listar_recargas_de_celular(offset=offset, limit=limit)

Listar recargas de celular



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.mobile_phone_recharge_list_response_dto import MobilePhoneRechargeListResponseDTO
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
    api_instance = asaas.RecargasDeCelularApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)

    try:
        # Listar recargas de celular
        api_response = api_instance.listar_recargas_de_celular(offset=offset, limit=limit)
        print("The response of RecargasDeCelularApi->listar_recargas_de_celular:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecargasDeCelularApi->listar_recargas_de_celular: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 

### Return type

[**MobilePhoneRechargeListResponseDTO**](MobilePhoneRechargeListResponseDTO.md)

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

# **recuperar_uma_unica_recarga_de_celular**
> MobilePhoneRechargeGetResponseDTO recuperar_uma_unica_recarga_de_celular(id)

Recuperar uma única recarga de celular



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.mobile_phone_recharge_get_response_dto import MobilePhoneRechargeGetResponseDTO
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
    api_instance = asaas.RecargasDeCelularApi(api_client)
    id = '37c22147-4194-11ec-8061-0242ac120002' # str | Identificador único da recarga de celular no Asaas

    try:
        # Recuperar uma única recarga de celular
        api_response = api_instance.recuperar_uma_unica_recarga_de_celular(id)
        print("The response of RecargasDeCelularApi->recuperar_uma_unica_recarga_de_celular:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecargasDeCelularApi->recuperar_uma_unica_recarga_de_celular: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da recarga de celular no Asaas | 

### Return type

[**MobilePhoneRechargeGetResponseDTO**](MobilePhoneRechargeGetResponseDTO.md)

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

# **solicitar_recarga**
> MobilePhoneRechargeGetResponseDTO solicitar_recarga(mobile_phone_recharge_save_request_dto=mobile_phone_recharge_save_request_dto)

Solicitar recarga



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.mobile_phone_recharge_get_response_dto import MobilePhoneRechargeGetResponseDTO
from asaas.models.mobile_phone_recharge_save_request_dto import MobilePhoneRechargeSaveRequestDTO
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
    api_instance = asaas.RecargasDeCelularApi(api_client)
    mobile_phone_recharge_save_request_dto = asaas.MobilePhoneRechargeSaveRequestDTO() # MobilePhoneRechargeSaveRequestDTO |  (optional)

    try:
        # Solicitar recarga
        api_response = api_instance.solicitar_recarga(mobile_phone_recharge_save_request_dto=mobile_phone_recharge_save_request_dto)
        print("The response of RecargasDeCelularApi->solicitar_recarga:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecargasDeCelularApi->solicitar_recarga: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **mobile_phone_recharge_save_request_dto** | [**MobilePhoneRechargeSaveRequestDTO**](MobilePhoneRechargeSaveRequestDTO.md)|  | [optional] 

### Return type

[**MobilePhoneRechargeGetResponseDTO**](MobilePhoneRechargeGetResponseDTO.md)

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

