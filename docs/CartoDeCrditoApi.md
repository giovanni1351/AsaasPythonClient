# asaas.CartoDeCrditoApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**recuperar_configuracao_de_pre_autorizacao**](CartoDeCrditoApi.md#recuperar_configuracao_de_pre_autorizacao) | **GET** /v3/creditCard/preAuthorization/config | Recuperar configuração da pré-autorização
[**salvar_ou_atualizar_configuracao_de_pre_autorizacao**](CartoDeCrditoApi.md#salvar_ou_atualizar_configuracao_de_pre_autorizacao) | **POST** /v3/creditCard/preAuthorization/config | Salvar ou atualizar configuração da pré-autorização
[**tokenizacao_de_cartao_de_credito**](CartoDeCrditoApi.md#tokenizacao_de_cartao_de_credito) | **POST** /v3/creditCard/tokenizeCreditCard | Tokenização de cartão de crédito


# **recuperar_configuracao_de_pre_autorizacao**
> CreditCardPreAuthorizationConfigResponseDTO recuperar_configuracao_de_pre_autorizacao()

Recuperar configuração da pré-autorização



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.credit_card_pre_authorization_config_response_dto import CreditCardPreAuthorizationConfigResponseDTO
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
    api_instance = asaas.CartoDeCrditoApi(api_client)

    try:
        # Recuperar configuração da pré-autorização
        api_response = api_instance.recuperar_configuracao_de_pre_autorizacao()
        print("The response of CartoDeCrditoApi->recuperar_configuracao_de_pre_autorizacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CartoDeCrditoApi->recuperar_configuracao_de_pre_autorizacao: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**CreditCardPreAuthorizationConfigResponseDTO**](CreditCardPreAuthorizationConfigResponseDTO.md)

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

# **salvar_ou_atualizar_configuracao_de_pre_autorizacao**
> CreditCardPreAuthorizationConfigResponseDTO salvar_ou_atualizar_configuracao_de_pre_autorizacao(credit_card_pre_authorization_config_request_dto=credit_card_pre_authorization_config_request_dto)

Salvar ou atualizar configuração da pré-autorização



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.credit_card_pre_authorization_config_request_dto import CreditCardPreAuthorizationConfigRequestDTO
from asaas.models.credit_card_pre_authorization_config_response_dto import CreditCardPreAuthorizationConfigResponseDTO
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
    api_instance = asaas.CartoDeCrditoApi(api_client)
    credit_card_pre_authorization_config_request_dto = asaas.CreditCardPreAuthorizationConfigRequestDTO() # CreditCardPreAuthorizationConfigRequestDTO |  (optional)

    try:
        # Salvar ou atualizar configuração da pré-autorização
        api_response = api_instance.salvar_ou_atualizar_configuracao_de_pre_autorizacao(credit_card_pre_authorization_config_request_dto=credit_card_pre_authorization_config_request_dto)
        print("The response of CartoDeCrditoApi->salvar_ou_atualizar_configuracao_de_pre_autorizacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CartoDeCrditoApi->salvar_ou_atualizar_configuracao_de_pre_autorizacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **credit_card_pre_authorization_config_request_dto** | [**CreditCardPreAuthorizationConfigRequestDTO**](CreditCardPreAuthorizationConfigRequestDTO.md)|  | [optional] 

### Return type

[**CreditCardPreAuthorizationConfigResponseDTO**](CreditCardPreAuthorizationConfigResponseDTO.md)

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

# **tokenizacao_de_cartao_de_credito**
> CreditCardTokenizeResponseDTO tokenizacao_de_cartao_de_credito(credit_card_tokenize_request_dto=credit_card_tokenize_request_dto)

Tokenização de cartão de crédito



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.credit_card_tokenize_request_dto import CreditCardTokenizeRequestDTO
from asaas.models.credit_card_tokenize_response_dto import CreditCardTokenizeResponseDTO
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
    api_instance = asaas.CartoDeCrditoApi(api_client)
    credit_card_tokenize_request_dto = asaas.CreditCardTokenizeRequestDTO() # CreditCardTokenizeRequestDTO |  (optional)

    try:
        # Tokenização de cartão de crédito
        api_response = api_instance.tokenizacao_de_cartao_de_credito(credit_card_tokenize_request_dto=credit_card_tokenize_request_dto)
        print("The response of CartoDeCrditoApi->tokenizacao_de_cartao_de_credito:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CartoDeCrditoApi->tokenizacao_de_cartao_de_credito: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **credit_card_tokenize_request_dto** | [**CreditCardTokenizeRequestDTO**](CreditCardTokenizeRequestDTO.md)|  | [optional] 

### Return type

[**CreditCardTokenizeResponseDTO**](CreditCardTokenizeResponseDTO.md)

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

