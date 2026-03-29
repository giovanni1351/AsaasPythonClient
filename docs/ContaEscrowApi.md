# asaas.ContaEscrowApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas**](ContaEscrowApi.md#criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas) | **POST** /v3/accounts/escrow | Criar configuração padrão da Conta Escrow para todas as subcontas
[**encerrar_garantia_da_cobranca_na_conta_escrow**](ContaEscrowApi.md#encerrar_garantia_da_cobranca_na_conta_escrow) | **POST** /v3/escrow/{id}/finish | Encerrar garantia da cobrança na Conta Escrow
[**recuperar_configuracao_da_conta_escrow_para_a_subconta**](ContaEscrowApi.md#recuperar_configuracao_da_conta_escrow_para_a_subconta) | **GET** /v3/accounts/{id}/escrow | Recuperar configuração da Conta Escrow para a subconta
[**recuperar_configuracao_padrao_da_conta_escrow**](ContaEscrowApi.md#recuperar_configuracao_padrao_da_conta_escrow) | **GET** /v3/accounts/escrow | Recuperar configuração padrão da Conta Escrow
[**recuperar_garantia_da_cobranca_na_conta_escrow**](ContaEscrowApi.md#recuperar_garantia_da_cobranca_na_conta_escrow) | **GET** /v3/payments/{id}/escrow | Recuperar garantia da cobrança na Conta Escrow
[**salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta**](ContaEscrowApi.md#salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta) | **POST** /v3/accounts/{id}/escrow | Salvar ou atualizar configuração da Conta Escrow para a subconta


# **criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas**
> AccountPaymentEscrowConfigDTO criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas(account_payment_escrow_config_dto=account_payment_escrow_config_dto)

Criar configuração padrão da Conta Escrow para todas as subcontas



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_payment_escrow_config_dto import AccountPaymentEscrowConfigDTO
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
    api_instance = asaas.ContaEscrowApi(api_client)
    account_payment_escrow_config_dto = asaas.AccountPaymentEscrowConfigDTO() # AccountPaymentEscrowConfigDTO |  (optional)

    try:
        # Criar configuração padrão da Conta Escrow para todas as subcontas
        api_response = api_instance.criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas(account_payment_escrow_config_dto=account_payment_escrow_config_dto)
        print("The response of ContaEscrowApi->criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContaEscrowApi->criar_configuracao_padrao_da_conta_escrow_para_todas_as_subcontas: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_payment_escrow_config_dto** | [**AccountPaymentEscrowConfigDTO**](AccountPaymentEscrowConfigDTO.md)|  | [optional] 

### Return type

[**AccountPaymentEscrowConfigDTO**](AccountPaymentEscrowConfigDTO.md)

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

# **encerrar_garantia_da_cobranca_na_conta_escrow**
> PaymentGetResponseDTO encerrar_garantia_da_cobranca_na_conta_escrow(id, body=body)

Encerrar garantia da cobrança na Conta Escrow



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
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
    api_instance = asaas.ContaEscrowApi(api_client)
    id = '4f468235-cec3-482f-b3d0-348af4c7194' # str | Identificador único da garantia da cobrança na Conta Escrow do Asaas
    body = None # object |  (optional)

    try:
        # Encerrar garantia da cobrança na Conta Escrow
        api_response = api_instance.encerrar_garantia_da_cobranca_na_conta_escrow(id, body=body)
        print("The response of ContaEscrowApi->encerrar_garantia_da_cobranca_na_conta_escrow:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContaEscrowApi->encerrar_garantia_da_cobranca_na_conta_escrow: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da garantia da cobrança na Conta Escrow do Asaas | 
 **body** | **object**|  | [optional] 

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **recuperar_configuracao_da_conta_escrow_para_a_subconta**
> AccountPaymentEscrowConfigDTO recuperar_configuracao_da_conta_escrow_para_a_subconta(id)

Recuperar configuração da Conta Escrow para a subconta



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_payment_escrow_config_dto import AccountPaymentEscrowConfigDTO
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
    api_instance = asaas.ContaEscrowApi(api_client)
    id = '4f468235-cec3-482f-b3d0-348af4c7194' # str | Identificador único da subconta no Asaas

    try:
        # Recuperar configuração da Conta Escrow para a subconta
        api_response = api_instance.recuperar_configuracao_da_conta_escrow_para_a_subconta(id)
        print("The response of ContaEscrowApi->recuperar_configuracao_da_conta_escrow_para_a_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContaEscrowApi->recuperar_configuracao_da_conta_escrow_para_a_subconta: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da subconta no Asaas | 

### Return type

[**AccountPaymentEscrowConfigDTO**](AccountPaymentEscrowConfigDTO.md)

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

# **recuperar_configuracao_padrao_da_conta_escrow**
> AccountPaymentEscrowConfigDTO recuperar_configuracao_padrao_da_conta_escrow()

Recuperar configuração padrão da Conta Escrow



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_payment_escrow_config_dto import AccountPaymentEscrowConfigDTO
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
    api_instance = asaas.ContaEscrowApi(api_client)

    try:
        # Recuperar configuração padrão da Conta Escrow
        api_response = api_instance.recuperar_configuracao_padrao_da_conta_escrow()
        print("The response of ContaEscrowApi->recuperar_configuracao_padrao_da_conta_escrow:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContaEscrowApi->recuperar_configuracao_padrao_da_conta_escrow: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountPaymentEscrowConfigDTO**](AccountPaymentEscrowConfigDTO.md)

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

# **recuperar_garantia_da_cobranca_na_conta_escrow**
> PaymentEscrowGetResponseDTO recuperar_garantia_da_cobranca_na_conta_escrow(id)

Recuperar garantia da cobrança na Conta Escrow



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_escrow_get_response_dto import PaymentEscrowGetResponseDTO
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
    api_instance = asaas.ContaEscrowApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Recuperar garantia da cobrança na Conta Escrow
        api_response = api_instance.recuperar_garantia_da_cobranca_na_conta_escrow(id)
        print("The response of ContaEscrowApi->recuperar_garantia_da_cobranca_na_conta_escrow:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContaEscrowApi->recuperar_garantia_da_cobranca_na_conta_escrow: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da cobrança no Asaas | 

### Return type

[**PaymentEscrowGetResponseDTO**](PaymentEscrowGetResponseDTO.md)

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

# **salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta**
> AccountPaymentEscrowConfigDTO salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta(id, account_save_or_update_payment_escrow_config_request_dto=account_save_or_update_payment_escrow_config_request_dto)

Salvar ou atualizar configuração da Conta Escrow para a subconta



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_payment_escrow_config_dto import AccountPaymentEscrowConfigDTO
from asaas.models.account_save_or_update_payment_escrow_config_request_dto import AccountSaveOrUpdatePaymentEscrowConfigRequestDTO
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
    api_instance = asaas.ContaEscrowApi(api_client)
    id = '4f468235-cec3-482f-b3d0-348af4c7194' # str | Identificador único da subconta no Asaas
    account_save_or_update_payment_escrow_config_request_dto = asaas.AccountSaveOrUpdatePaymentEscrowConfigRequestDTO() # AccountSaveOrUpdatePaymentEscrowConfigRequestDTO |  (optional)

    try:
        # Salvar ou atualizar configuração da Conta Escrow para a subconta
        api_response = api_instance.salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta(id, account_save_or_update_payment_escrow_config_request_dto=account_save_or_update_payment_escrow_config_request_dto)
        print("The response of ContaEscrowApi->salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContaEscrowApi->salvar_ou_atualizar_configuracao_da_conta_escrow_para_a_subconta: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da subconta no Asaas | 
 **account_save_or_update_payment_escrow_config_request_dto** | [**AccountSaveOrUpdatePaymentEscrowConfigRequestDTO**](AccountSaveOrUpdatePaymentEscrowConfigRequestDTO.md)|  | [optional] 

### Return type

[**AccountPaymentEscrowConfigDTO**](AccountPaymentEscrowConfigDTO.md)

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

