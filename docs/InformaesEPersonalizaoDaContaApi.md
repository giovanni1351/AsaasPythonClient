# asaas.InformaesEPersonalizaoDaContaApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                         | HTTP request                                  | Description                               |
| ------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------- | ----------------------------------------- |
| [**aprovar_conta**](InformaesEPersonalizaoDaContaApi.md#aprovar_conta)                                                         | **POST** /v3/sandbox/myAccount/approve        | (Apenas Sandbox) Aprovar conta            |
| [**atualizar_dados_comerciais**](InformaesEPersonalizaoDaContaApi.md#atualizar_dados_comerciais)                               | **POST** /v3/myAccount/commercialInfo/        | Atualizar dados comerciais                |
| [**consultar_situacao_cadastral_da_conta**](InformaesEPersonalizaoDaContaApi.md#consultar_situacao_cadastral_da_conta)         | **GET** /v3/myAccount/status/                 | Consultar situação cadastral da conta     |
| [**excluir_subconta_white_label**](InformaesEPersonalizaoDaContaApi.md#excluir_subconta_white_label)                           | **DELETE** /v3/myAccount/                     | Excluir subconta White Label              |
| [**recuperar_configuracoes_de_personalizacao**](InformaesEPersonalizaoDaContaApi.md#recuperar_configuracoes_de_personalizacao) | **GET** /v3/myAccount/paymentCheckoutConfig/  | Recuperar configurações de personalização |
| [**recuperar_dados_comerciais**](InformaesEPersonalizaoDaContaApi.md#recuperar_dados_comerciais)                               | **GET** /v3/myAccount/commercialInfo/         | Recuperar dados comerciais                |
| [**recuperar_numero_de_conta_no_asaas**](InformaesEPersonalizaoDaContaApi.md#recuperar_numero_de_conta_no_asaas)               | **GET** /v3/myAccount/accountNumber           | Recuperar número de conta no Asaas        |
| [**recuperar_taxas_da_conta**](InformaesEPersonalizaoDaContaApi.md#recuperar_taxas_da_conta)                                   | **GET** /v3/myAccount/fees/                   | Recuperar taxas da conta                  |
| [**recuperar_walletid**](InformaesEPersonalizaoDaContaApi.md#recuperar_walletid)                                               | **GET** /v3/wallets/                          | Recuperar WalletId                        |
| [**salvar_personalizacao_da_fatura**](InformaesEPersonalizaoDaContaApi.md#salvar_personalizacao_da_fatura)                     | **POST** /v3/myAccount/paymentCheckoutConfig/ | Salvar personalização da fatura           |

# **aprovar_conta**

> MyAccountGetStatusResponseDTO aprovar_conta(body=body)

(Apenas Sandbox) Aprovar conta

Este endpoint aprova a sua conta no ambiente sandbox.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.my_account_get_status_response_dto import MyAccountGetStatusResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)
    body = None # object |  (optional)

    try:
        # (Apenas Sandbox) Aprovar conta
        api_response = api_instance.aprovar_conta(body=body)
        print("The response of InformaesEPersonalizaoDaContaApi->aprovar_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->aprovar_conta: %s\n" % e)
```

### Parameters

| Name     | Type       | Description | Notes      |
| -------- | ---------- | ----------- | ---------- |
| **body** | **object** |             | [optional] |

### Return type

[**MyAccountGetStatusResponseDTO**](MyAccountGetStatusResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **atualizar_dados_comerciais**

> AccountInfoGetResponseDTO atualizar_dados_comerciais(account_info_save_request_dto=account_info_save_request_dto)

Atualizar dados comerciais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_info_get_response_dto import AccountInfoGetResponseDTO
from asaas.models.account_info_save_request_dto import AccountInfoSaveRequestDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)
    account_info_save_request_dto = asaas.AccountInfoSaveRequestDTO() # AccountInfoSaveRequestDTO |  (optional)

    try:
        # Atualizar dados comerciais
        api_response = api_instance.atualizar_dados_comerciais(account_info_save_request_dto=account_info_save_request_dto)
        print("The response of InformaesEPersonalizaoDaContaApi->atualizar_dados_comerciais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->atualizar_dados_comerciais: %s\n" % e)
```

### Parameters

| Name                              | Type                                                          | Description | Notes      |
| --------------------------------- | ------------------------------------------------------------- | ----------- | ---------- |
| **account_info_save_request_dto** | [**AccountInfoSaveRequestDTO**](AccountInfoSaveRequestDTO.md) |             | [optional] |

### Return type

[**AccountInfoGetResponseDTO**](AccountInfoGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **consultar_situacao_cadastral_da_conta**

> MyAccountGetStatusResponseDTO consultar_situacao_cadastral_da_conta()

Consultar situação cadastral da conta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.my_account_get_status_response_dto import MyAccountGetStatusResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)

    try:
        # Consultar situação cadastral da conta
        api_response = api_instance.consultar_situacao_cadastral_da_conta()
        print("The response of InformaesEPersonalizaoDaContaApi->consultar_situacao_cadastral_da_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->consultar_situacao_cadastral_da_conta: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**MyAccountGetStatusResponseDTO**](MyAccountGetStatusResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **excluir_subconta_white_label**

> MyAccountDisableAccountResponseDTO excluir_subconta_white_label(remove_reason=remove_reason)

Excluir subconta White Label

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.my_account_disable_account_response_dto import MyAccountDisableAccountResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)
    remove_reason = 'Liberar dados' # str | Motivo da remoção (optional)

    try:
        # Excluir subconta White Label
        api_response = api_instance.excluir_subconta_white_label(remove_reason=remove_reason)
        print("The response of InformaesEPersonalizaoDaContaApi->excluir_subconta_white_label:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->excluir_subconta_white_label: %s\n" % e)
```

### Parameters

| Name              | Type    | Description       | Notes      |
| ----------------- | ------- | ----------------- | ---------- |
| **remove_reason** | **str** | Motivo da remoção | [optional] |

### Return type

[**MyAccountDisableAccountResponseDTO**](MyAccountDisableAccountResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_configuracoes_de_personalizacao**

> PaymentCheckoutConfigGetResponseDTO recuperar_configuracoes_de_personalizacao()

Recuperar configurações de personalização

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_checkout_config_get_response_dto import PaymentCheckoutConfigGetResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)

    try:
        # Recuperar configurações de personalização
        api_response = api_instance.recuperar_configuracoes_de_personalizacao()
        print("The response of InformaesEPersonalizaoDaContaApi->recuperar_configuracoes_de_personalizacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->recuperar_configuracoes_de_personalizacao: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PaymentCheckoutConfigGetResponseDTO**](PaymentCheckoutConfigGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_dados_comerciais**

> AccountInfoGetResponseDTO recuperar_dados_comerciais()

Recuperar dados comerciais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.account_info_get_response_dto import AccountInfoGetResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)

    try:
        # Recuperar dados comerciais
        api_response = api_instance.recuperar_dados_comerciais()
        print("The response of InformaesEPersonalizaoDaContaApi->recuperar_dados_comerciais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->recuperar_dados_comerciais: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountInfoGetResponseDTO**](AccountInfoGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_numero_de_conta_no_asaas**

> MyAccountGetAccountNumberResponseDTO recuperar_numero_de_conta_no_asaas()

Recuperar número de conta no Asaas

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.my_account_get_account_number_response_dto import MyAccountGetAccountNumberResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)

    try:
        # Recuperar número de conta no Asaas
        api_response = api_instance.recuperar_numero_de_conta_no_asaas()
        print("The response of InformaesEPersonalizaoDaContaApi->recuperar_numero_de_conta_no_asaas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->recuperar_numero_de_conta_no_asaas: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**MyAccountGetAccountNumberResponseDTO**](MyAccountGetAccountNumberResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_taxas_da_conta**

> MyAccountGetAccountFeesResponseDTO recuperar_taxas_da_conta()

Recuperar taxas da conta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.my_account_get_account_fees_response_dto import MyAccountGetAccountFeesResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)

    try:
        # Recuperar taxas da conta
        api_response = api_instance.recuperar_taxas_da_conta()
        print("The response of InformaesEPersonalizaoDaContaApi->recuperar_taxas_da_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->recuperar_taxas_da_conta: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**MyAccountGetAccountFeesResponseDTO**](MyAccountGetAccountFeesResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_walletid**

> WalletShowResponseDTO recuperar_walletid()

Recuperar WalletId

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.wallet_show_response_dto import WalletShowResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)

    try:
        # Recuperar WalletId
        api_response = api_instance.recuperar_walletid()
        print("The response of InformaesEPersonalizaoDaContaApi->recuperar_walletid:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->recuperar_walletid: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**WalletShowResponseDTO**](WalletShowResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **salvar_personalizacao_da_fatura**

> PaymentCheckoutConfigGetResponseDTO salvar_personalizacao_da_fatura(logo_background_color, info_background_color, font_color, enabled=enabled, logo_file=logo_file)

Salvar personalização da fatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_checkout_config_get_response_dto import PaymentCheckoutConfigGetResponseDTO
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
    api_instance = asaas.InformaesEPersonalizaoDaContaApi(api_client)
    logo_background_color = 'logo_background_color_example' # str | Cor de fundo do logo
    info_background_color = 'info_background_color_example' # str | Cor de fundo das suas informações
    font_color = 'font_color_example' # str | Cor da fonte das suas informações
    enabled = True # bool | Indica se a personalização está habilitada (optional)
    logo_file = None # bytes | Arquivo (optional)

    try:
        # Salvar personalização da fatura
        api_response = api_instance.salvar_personalizacao_da_fatura(logo_background_color, info_background_color, font_color, enabled=enabled, logo_file=logo_file)
        print("The response of InformaesEPersonalizaoDaContaApi->salvar_personalizacao_da_fatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesEPersonalizaoDaContaApi->salvar_personalizacao_da_fatura: %s\n" % e)
```

### Parameters

| Name                      | Type      | Description                                | Notes      |
| ------------------------- | --------- | ------------------------------------------ | ---------- |
| **logo_background_color** | **str**   | Cor de fundo do logo                       |
| **info_background_color** | **str**   | Cor de fundo das suas informações          |
| **font_color**            | **str**   | Cor da fonte das suas informações          |
| **enabled**               | **bool**  | Indica se a personalização está habilitada | [optional] |
| **logo_file**             | **bytes** | Arquivo                                    | [optional] |

### Return type

[**PaymentCheckoutConfigGetResponseDTO**](PaymentCheckoutConfigGetResponseDTO.md)

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

### HTTP response details

| Status code | Description  | Response headers |
| ----------- | ------------ | ---------------- |
| **200**     | Ok           | -                |
| **401**     | Unauthorized | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)
