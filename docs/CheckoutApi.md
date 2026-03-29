# asaas.CheckoutApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelar_um_checkout**](CheckoutApi.md#cancelar_um_checkout) | **POST** /v3/checkouts/{id}/cancel | Cancelar um checkout
[**criar_novo_checkout**](CheckoutApi.md#criar_novo_checkout) | **POST** /v3/checkouts | Criar novo checkout


# **cancelar_um_checkout**
> CheckoutSessionResponseDTO cancelar_um_checkout(id, body=body)

Cancelar um checkout



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.checkout_session_response_dto import CheckoutSessionResponseDTO
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
    api_instance = asaas.CheckoutApi(api_client)
    id = '131ca662-56c8-4479-b5b3-fd61a413fce7' # str | Identificador único do checkout no Asaas
    body = None # object |  (optional)

    try:
        # Cancelar um checkout
        api_response = api_instance.cancelar_um_checkout(id, body=body)
        print("The response of CheckoutApi->cancelar_um_checkout:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CheckoutApi->cancelar_um_checkout: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único do checkout no Asaas | 
 **body** | **object**|  | [optional] 

### Return type

[**CheckoutSessionResponseDTO**](CheckoutSessionResponseDTO.md)

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

# **criar_novo_checkout**
> CheckoutSessionResponseDTO criar_novo_checkout(checkout_session_save_request_dto=checkout_session_save_request_dto)

Criar novo checkout



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.checkout_session_response_dto import CheckoutSessionResponseDTO
from asaas.models.checkout_session_save_request_dto import CheckoutSessionSaveRequestDTO
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
    api_instance = asaas.CheckoutApi(api_client)
    checkout_session_save_request_dto = asaas.CheckoutSessionSaveRequestDTO() # CheckoutSessionSaveRequestDTO |  (optional)

    try:
        # Criar novo checkout
        api_response = api_instance.criar_novo_checkout(checkout_session_save_request_dto=checkout_session_save_request_dto)
        print("The response of CheckoutApi->criar_novo_checkout:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CheckoutApi->criar_novo_checkout: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **checkout_session_save_request_dto** | [**CheckoutSessionSaveRequestDTO**](CheckoutSessionSaveRequestDTO.md)|  | [optional] 

### Return type

[**CheckoutSessionResponseDTO**](CheckoutSessionResponseDTO.md)

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

