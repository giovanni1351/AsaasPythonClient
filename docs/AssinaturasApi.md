# asaas.AssinaturasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                             | HTTP request                                      | Description                                          |
| ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ---------------------------------------------------- |
| [**atualizar_assinatura_existente**](AssinaturasApi.md#atualizar_assinatura_existente)                                             | **PUT** /v3/subscriptions/{id}                    | Atualizar assinatura existente                       |
| [**atualizar_cartao_de_credito_assinatura**](AssinaturasApi.md#atualizar_cartao_de_credito_assinatura)                             | **PUT** /v3/subscriptions/{id}/creditCard         | Atualiza o cartão de crédito sem efetuar cobrança    |
| [**atualizar_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#atualizar_configuracao_para_emissao_de_notas_fiscais) | **PUT** /v3/subscriptions/{id}/invoiceSettings    | Atualizar configuração para emissão de Notas Fiscais |
| [**criar_assinatura_com_cartao_de_credito**](AssinaturasApi.md#criar_assinatura_com_cartao_de_credito)                             | **POST** /v3/subscriptions/                       | Criar assinatura com cartão de crédito               |
| [**criar_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#criar_configuracao_para_emissao_de_notas_fiscais)         | **POST** /v3/subscriptions/{id}/invoiceSettings   | Criar configuração para emissão de Notas Fiscais     |
| [**criar_nova_assinatura**](AssinaturasApi.md#criar_nova_assinatura)                                                               | **POST** /v3/subscriptions                        | Criar nova assinatura                                |
| [**gerar_carne_de_assinatura**](AssinaturasApi.md#gerar_carne_de_assinatura)                                                       | **GET** /v3/subscriptions/{id}/paymentBook        | Gerar carnê de assinatura                            |
| [**listar_assinaturas**](AssinaturasApi.md#listar_assinaturas)                                                                     | **GET** /v3/subscriptions                         | Listar assinaturas                                   |
| [**listar_cobrancas_de_uma_assinatura**](AssinaturasApi.md#listar_cobrancas_de_uma_assinatura)                                     | **GET** /v3/subscriptions/{id}/payments           | Listar cobranças de uma assinatura                   |
| [**listar_notas_fiscais_das_cobrancas_de_uma_assinatura**](AssinaturasApi.md#listar_notas_fiscais_das_cobrancas_de_uma_assinatura) | **GET** /v3/subscriptions/{id}/invoices           | Listar notas fiscais das cobranças de uma assinatura |
| [**recuperar_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#recuperar_configuracao_para_emissao_de_notas_fiscais) | **GET** /v3/subscriptions/{id}/invoiceSettings    | Recuperar configuração para emissão de notas fiscais |
| [**recuperar_uma_unica_assinatura**](AssinaturasApi.md#recuperar_uma_unica_assinatura)                                             | **GET** /v3/subscriptions/{id}                    | Recuperar uma única assinatura                       |
| [**remover_assinatura**](AssinaturasApi.md#remover_assinatura)                                                                     | **DELETE** /v3/subscriptions/{id}                 | Remover assinatura                                   |
| [**remover_configuracao_para_emissao_de_notas_fiscais**](AssinaturasApi.md#remover_configuracao_para_emissao_de_notas_fiscais)     | **DELETE** /v3/subscriptions/{id}/invoiceSettings | Remover configuração para emissão de Notas Fiscais   |

# **atualizar_assinatura_existente**

> SubscriptionGetResponseDTO atualizar_assinatura_existente(id, subscription_update_request_dto=subscription_update_request_dto)

Atualizar assinatura existente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_get_response_dto import SubscriptionGetResponseDTO
from asaas.models.subscription_update_request_dto import SubscriptionUpdateRequestDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas
    subscription_update_request_dto = asaas.SubscriptionUpdateRequestDTO() # SubscriptionUpdateRequestDTO |  (optional)

    try:
        # Atualizar assinatura existente
        api_response = api_instance.atualizar_assinatura_existente(id, subscription_update_request_dto=subscription_update_request_dto)
        print("The response of AssinaturasApi->atualizar_assinatura_existente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->atualizar_assinatura_existente: %s\n" % e)
```

### Parameters

| Name                                | Type                                                                | Description                                | Notes      |
| ----------------------------------- | ------------------------------------------------------------------- | ------------------------------------------ | ---------- |
| **id**                              | **str**                                                             | Identificador único da assinatura no Asaas |
| **subscription_update_request_dto** | [**SubscriptionUpdateRequestDTO**](SubscriptionUpdateRequestDTO.md) |                                            | [optional] |

### Return type

[**SubscriptionGetResponseDTO**](SubscriptionGetResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **atualizar_cartao_de_credito_assinatura**

> SubscriptionGetResponseDTO atualizar_cartao_de_credito_assinatura(id, subscription_update_credit_card_request_dto=subscription_update_credit_card_request_dto)

Atualiza o cartão de crédito sem efetuar cobrança

Este endpoint atualiza o cartão de crédito da assinatura sem realizar a cobrança imediata. Além disso, todas as cobranças pendentes vinculadas a assinatura também são atualizadas.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_get_response_dto import SubscriptionGetResponseDTO
from asaas.models.subscription_update_credit_card_request_dto import SubscriptionUpdateCreditCardRequestDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas
    subscription_update_credit_card_request_dto = asaas.SubscriptionUpdateCreditCardRequestDTO() # SubscriptionUpdateCreditCardRequestDTO |  (optional)

    try:
        # Atualiza o cartão de crédito sem efetuar cobrança
        api_response = api_instance.atualizar_cartao_de_credito_assinatura(id, subscription_update_credit_card_request_dto=subscription_update_credit_card_request_dto)
        print("The response of AssinaturasApi->atualizar_cartao_de_credito_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->atualizar_cartao_de_credito_assinatura: %s\n" % e)
```

### Parameters

| Name                                            | Type                                                                                    | Description                                | Notes      |
| ----------------------------------------------- | --------------------------------------------------------------------------------------- | ------------------------------------------ | ---------- |
| **id**                                          | **str**                                                                                 | Identificador único da assinatura no Asaas |
| **subscription_update_credit_card_request_dto** | [**SubscriptionUpdateCreditCardRequestDTO**](SubscriptionUpdateCreditCardRequestDTO.md) |                                            | [optional] |

### Return type

[**SubscriptionGetResponseDTO**](SubscriptionGetResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **atualizar_configuracao_para_emissao_de_notas_fiscais**

> SubscriptionInvoiceConfigGetResponseDTO atualizar_configuracao_para_emissao_de_notas_fiscais(id, subscription_invoice_config_update_request_dto=subscription_invoice_config_update_request_dto)

Atualizar configuração para emissão de Notas Fiscais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_invoice_config_get_response_dto import SubscriptionInvoiceConfigGetResponseDTO
from asaas.models.subscription_invoice_config_update_request_dto import SubscriptionInvoiceConfigUpdateRequestDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas
    subscription_invoice_config_update_request_dto = asaas.SubscriptionInvoiceConfigUpdateRequestDTO() # SubscriptionInvoiceConfigUpdateRequestDTO |  (optional)

    try:
        # Atualizar configuração para emissão de Notas Fiscais
        api_response = api_instance.atualizar_configuracao_para_emissao_de_notas_fiscais(id, subscription_invoice_config_update_request_dto=subscription_invoice_config_update_request_dto)
        print("The response of AssinaturasApi->atualizar_configuracao_para_emissao_de_notas_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->atualizar_configuracao_para_emissao_de_notas_fiscais: %s\n" % e)
```

### Parameters

| Name                                               | Type                                                                                          | Description                                | Notes      |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------- | ------------------------------------------ | ---------- |
| **id**                                             | **str**                                                                                       | Identificador único da assinatura no Asaas |
| **subscription_invoice_config_update_request_dto** | [**SubscriptionInvoiceConfigUpdateRequestDTO**](SubscriptionInvoiceConfigUpdateRequestDTO.md) |                                            | [optional] |

### Return type

[**SubscriptionInvoiceConfigGetResponseDTO**](SubscriptionInvoiceConfigGetResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **criar_assinatura_com_cartao_de_credito**

> SubscriptionSaveWithCreditCardResponseDTO criar_assinatura_com_cartao_de_credito(subscription_save_with_credit_card_request_dto=subscription_save_with_credit_card_request_dto)

Criar assinatura com cartão de crédito

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_save_with_credit_card_request_dto import SubscriptionSaveWithCreditCardRequestDTO
from asaas.models.subscription_save_with_credit_card_response_dto import SubscriptionSaveWithCreditCardResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    subscription_save_with_credit_card_request_dto = asaas.SubscriptionSaveWithCreditCardRequestDTO() # SubscriptionSaveWithCreditCardRequestDTO |  (optional)

    try:
        # Criar assinatura com cartão de crédito
        api_response = api_instance.criar_assinatura_com_cartao_de_credito(subscription_save_with_credit_card_request_dto=subscription_save_with_credit_card_request_dto)
        print("The response of AssinaturasApi->criar_assinatura_com_cartao_de_credito:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->criar_assinatura_com_cartao_de_credito: %s\n" % e)
```

### Parameters

| Name                                               | Type                                                                                        | Description | Notes      |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------- | ----------- | ---------- |
| **subscription_save_with_credit_card_request_dto** | [**SubscriptionSaveWithCreditCardRequestDTO**](SubscriptionSaveWithCreditCardRequestDTO.md) |             | [optional] |

### Return type

[**SubscriptionSaveWithCreditCardResponseDTO**](SubscriptionSaveWithCreditCardResponseDTO.md)

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

# **criar_configuracao_para_emissao_de_notas_fiscais**

> SubscriptionInvoiceConfigGetResponseDTO criar_configuracao_para_emissao_de_notas_fiscais(id, subscription_configure_invoice_request_dto=subscription_configure_invoice_request_dto)

Criar configuração para emissão de Notas Fiscais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_configure_invoice_request_dto import SubscriptionConfigureInvoiceRequestDTO
from asaas.models.subscription_invoice_config_get_response_dto import SubscriptionInvoiceConfigGetResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas
    subscription_configure_invoice_request_dto = asaas.SubscriptionConfigureInvoiceRequestDTO() # SubscriptionConfigureInvoiceRequestDTO |  (optional)

    try:
        # Criar configuração para emissão de Notas Fiscais
        api_response = api_instance.criar_configuracao_para_emissao_de_notas_fiscais(id, subscription_configure_invoice_request_dto=subscription_configure_invoice_request_dto)
        print("The response of AssinaturasApi->criar_configuracao_para_emissao_de_notas_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->criar_configuracao_para_emissao_de_notas_fiscais: %s\n" % e)
```

### Parameters

| Name                                           | Type                                                                                    | Description                                | Notes      |
| ---------------------------------------------- | --------------------------------------------------------------------------------------- | ------------------------------------------ | ---------- |
| **id**                                         | **str**                                                                                 | Identificador único da assinatura no Asaas |
| **subscription_configure_invoice_request_dto** | [**SubscriptionConfigureInvoiceRequestDTO**](SubscriptionConfigureInvoiceRequestDTO.md) |                                            | [optional] |

### Return type

[**SubscriptionInvoiceConfigGetResponseDTO**](SubscriptionInvoiceConfigGetResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **criar_nova_assinatura**

> SubscriptionGetResponseDTO criar_nova_assinatura(subscription_save_request_dto=subscription_save_request_dto)

Criar nova assinatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_get_response_dto import SubscriptionGetResponseDTO
from asaas.models.subscription_save_request_dto import SubscriptionSaveRequestDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    subscription_save_request_dto = asaas.SubscriptionSaveRequestDTO() # SubscriptionSaveRequestDTO |  (optional)

    try:
        # Criar nova assinatura
        api_response = api_instance.criar_nova_assinatura(subscription_save_request_dto=subscription_save_request_dto)
        print("The response of AssinaturasApi->criar_nova_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->criar_nova_assinatura: %s\n" % e)
```

### Parameters

| Name                              | Type                                                            | Description | Notes      |
| --------------------------------- | --------------------------------------------------------------- | ----------- | ---------- |
| **subscription_save_request_dto** | [**SubscriptionSaveRequestDTO**](SubscriptionSaveRequestDTO.md) |             | [optional] |

### Return type

[**SubscriptionGetResponseDTO**](SubscriptionGetResponseDTO.md)

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

# **gerar_carne_de_assinatura**

> bytes gerar_carne_de_assinatura(id, month=month, year=year, sort=sort, order=order)

Gerar carnê de assinatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas
    month = 56 # int | Mês final para geração do carnê (optional)
    year = 56 # int | Ano final para geração do carnê (optional)
    sort = 'sort_example' # str | Filtrar pelo nome da coluna (optional)
    order = 'asc' # str | Ordenação da coluna (optional)

    try:
        # Gerar carnê de assinatura
        api_response = api_instance.gerar_carne_de_assinatura(id, month=month, year=year, sort=sort, order=order)
        print("The response of AssinaturasApi->gerar_carne_de_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->gerar_carne_de_assinatura: %s\n" % e)
```

### Parameters

| Name      | Type    | Description                                | Notes      |
| --------- | ------- | ------------------------------------------ | ---------- |
| **id**    | **str** | Identificador único da assinatura no Asaas |
| **month** | **int** | Mês final para geração do carnê            | [optional] |
| **year**  | **int** | Ano final para geração do carnê            | [optional] |
| **sort**  | **str** | Filtrar pelo nome da coluna                | [optional] |
| **order** | **str** | Ordenação da coluna                        | [optional] |

### Return type

**bytes**

### Authorization

[Authorization](index.md#Authorization)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json

### HTTP response details

| Status code | Description                                                                                                       | Response headers |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ---------------- |
| **200**     | Ok                                                                                                                | -                |
| **401**     | Unauthorized                                                                                                      | -                |
| **403**     | Forbidden. Ocorre quando o body da requisição está preenchido, chamadas de método GET precisam ter um body vazio. | -                |
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **listar_assinaturas**

> SubscriptionListResponseDTO listar_assinaturas(offset=offset, limit=limit, customer=customer, customer_group_name=customer_group_name, billing_type=billing_type, status=status, deleted_only=deleted_only, include_deleted=include_deleted, external_reference=external_reference, order=order, sort=sort)

Listar assinaturas

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_list_request_billing_type import SubscriptionListRequestBillingType
from asaas.models.subscription_list_request_subscription_status import SubscriptionListRequestSubscriptionStatus
from asaas.models.subscription_list_response_dto import SubscriptionListResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    customer = 'customer_example' # str | Filtrar pelo Identificador único do cliente (optional)
    customer_group_name = 'customer_group_name_example' # str | Filtrar pelo nome do grupo de cliente (optional)
    billing_type = asaas.SubscriptionListRequestBillingType() # SubscriptionListRequestBillingType | Filtrar por forma de pagamento (optional)
    status = asaas.SubscriptionListRequestSubscriptionStatus() # SubscriptionListRequestSubscriptionStatus | Filtrar pelo status (optional)
    deleted_only = 'deleted_only_example' # str | Envie true para retornar somente as assinaturas removidas (optional)
    include_deleted = 'include_deleted_example' # str | Envie true para recuperar também as assinaturas removidas (optional)
    external_reference = 'external_reference_example' # str | Filtrar pelo Identificador do seu sistema (optional)
    order = 'order_example' # str | Ordem crescente ou decrescente (optional)
    sort = 'sort_example' # str | Por qual campo será ordenado (optional)

    try:
        # Listar assinaturas
        api_response = api_instance.listar_assinaturas(offset=offset, limit=limit, customer=customer, customer_group_name=customer_group_name, billing_type=billing_type, status=status, deleted_only=deleted_only, include_deleted=include_deleted, external_reference=external_reference, order=order, sort=sort)
        print("The response of AssinaturasApi->listar_assinaturas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->listar_assinaturas: %s\n" % e)
```

### Parameters

| Name                    | Type                                                 | Description                                               | Notes      |
| ----------------------- | ---------------------------------------------------- | --------------------------------------------------------- | ---------- |
| **offset**              | **int**                                              | Elemento inicial da lista                                 | [optional] |
| **limit**               | **int**                                              | Número de elementos da lista (max: 100)                   | [optional] |
| **customer**            | **str**                                              | Filtrar pelo Identificador único do cliente               | [optional] |
| **customer_group_name** | **str**                                              | Filtrar pelo nome do grupo de cliente                     | [optional] |
| **billing_type**        | [**SubscriptionListRequestBillingType**](.md)        | Filtrar por forma de pagamento                            | [optional] |
| **status**              | [**SubscriptionListRequestSubscriptionStatus**](.md) | Filtrar pelo status                                       | [optional] |
| **deleted_only**        | **str**                                              | Envie true para retornar somente as assinaturas removidas | [optional] |
| **include_deleted**     | **str**                                              | Envie true para recuperar também as assinaturas removidas | [optional] |
| **external_reference**  | **str**                                              | Filtrar pelo Identificador do seu sistema                 | [optional] |
| **order**               | **str**                                              | Ordem crescente ou decrescente                            | [optional] |
| **sort**                | **str**                                              | Por qual campo será ordenado                              | [optional] |

### Return type

[**SubscriptionListResponseDTO**](SubscriptionListResponseDTO.md)

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

# **listar_cobrancas_de_uma_assinatura**

> PaymentListResponseDTO listar_cobrancas_de_uma_assinatura(id, status=status)

Listar cobranças de uma assinatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_list_response_dto import PaymentListResponseDTO
from asaas.models.subscription_list_payments_request_payment_status import SubscriptionListPaymentsRequestPaymentStatus
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas
    status = asaas.SubscriptionListPaymentsRequestPaymentStatus() # SubscriptionListPaymentsRequestPaymentStatus | Filtrar por status das cobranças (optional)

    try:
        # Listar cobranças de uma assinatura
        api_response = api_instance.listar_cobrancas_de_uma_assinatura(id, status=status)
        print("The response of AssinaturasApi->listar_cobrancas_de_uma_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->listar_cobrancas_de_uma_assinatura: %s\n" % e)
```

### Parameters

| Name       | Type                                                    | Description                                | Notes      |
| ---------- | ------------------------------------------------------- | ------------------------------------------ | ---------- |
| **id**     | **str**                                                 | Identificador único da assinatura no Asaas |
| **status** | [**SubscriptionListPaymentsRequestPaymentStatus**](.md) | Filtrar por status das cobranças           | [optional] |

### Return type

[**PaymentListResponseDTO**](PaymentListResponseDTO.md)

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
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **listar_notas_fiscais_das_cobrancas_de_uma_assinatura**

> InvoiceListResponseDTO listar_notas_fiscais_das_cobrancas_de_uma_assinatura(id, offset=offset, limit=limit, effective_date_ge=effective_date_ge, effective_date_le=effective_date_le, external_reference=external_reference, status=status, customer=customer)

Listar notas fiscais das cobranças de uma assinatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.invoice_list_response_dto import InvoiceListResponseDTO
from asaas.models.subscription_get_invoices_request_invoice_status import SubscriptionGetInvoicesRequestInvoiceStatus
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'inv_000000000232' # str | Identificador único da assinatura no Asaas
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    effective_date_ge = '2024-08-20' # str | Filtrar a partir de uma data de emissão (optional)
    effective_date_le = '2024-08-20' # str | Filtrar até uma data de emissão (optional)
    external_reference = 'external_reference_example' # str | Identificador da nota fiscal no seu sistema (optional)
    status = asaas.SubscriptionGetInvoicesRequestInvoiceStatus() # SubscriptionGetInvoicesRequestInvoiceStatus | Filtrar por status da nota fiscal (optional)
    customer = 'cus_000000002750' # str | Filtrar pelo identificador único do cliente (optional)

    try:
        # Listar notas fiscais das cobranças de uma assinatura
        api_response = api_instance.listar_notas_fiscais_das_cobrancas_de_uma_assinatura(id, offset=offset, limit=limit, effective_date_ge=effective_date_ge, effective_date_le=effective_date_le, external_reference=external_reference, status=status, customer=customer)
        print("The response of AssinaturasApi->listar_notas_fiscais_das_cobrancas_de_uma_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->listar_notas_fiscais_das_cobrancas_de_uma_assinatura: %s\n" % e)
```

### Parameters

| Name                   | Type                                                   | Description                                 | Notes      |
| ---------------------- | ------------------------------------------------------ | ------------------------------------------- | ---------- |
| **id**                 | **str**                                                | Identificador único da assinatura no Asaas  |
| **offset**             | **int**                                                | Elemento inicial da lista                   | [optional] |
| **limit**              | **int**                                                | Número de elementos da lista (max: 100)     | [optional] |
| **effective_date_ge**  | **str**                                                | Filtrar a partir de uma data de emissão     | [optional] |
| **effective_date_le**  | **str**                                                | Filtrar até uma data de emissão             | [optional] |
| **external_reference** | **str**                                                | Identificador da nota fiscal no seu sistema | [optional] |
| **status**             | [**SubscriptionGetInvoicesRequestInvoiceStatus**](.md) | Filtrar por status da nota fiscal           | [optional] |
| **customer**           | **str**                                                | Filtrar pelo identificador único do cliente | [optional] |

### Return type

[**InvoiceListResponseDTO**](InvoiceListResponseDTO.md)

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
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_configuracao_para_emissao_de_notas_fiscais**

> SubscriptionInvoiceConfigGetResponseDTO recuperar_configuracao_para_emissao_de_notas_fiscais(id)

Recuperar configuração para emissão de notas fiscais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_invoice_config_get_response_dto import SubscriptionInvoiceConfigGetResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas

    try:
        # Recuperar configuração para emissão de notas fiscais
        api_response = api_instance.recuperar_configuracao_para_emissao_de_notas_fiscais(id)
        print("The response of AssinaturasApi->recuperar_configuracao_para_emissao_de_notas_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->recuperar_configuracao_para_emissao_de_notas_fiscais: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                | Notes |
| ------ | ------- | ------------------------------------------ | ----- |
| **id** | **str** | Identificador único da assinatura no Asaas |

### Return type

[**SubscriptionInvoiceConfigGetResponseDTO**](SubscriptionInvoiceConfigGetResponseDTO.md)

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
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **recuperar_uma_unica_assinatura**

> SubscriptionGetResponseDTO recuperar_uma_unica_assinatura(id)

Recuperar uma única assinatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_get_response_dto import SubscriptionGetResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas

    try:
        # Recuperar uma única assinatura
        api_response = api_instance.recuperar_uma_unica_assinatura(id)
        print("The response of AssinaturasApi->recuperar_uma_unica_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->recuperar_uma_unica_assinatura: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                | Notes |
| ------ | ------- | ------------------------------------------ | ----- |
| **id** | **str** | Identificador único da assinatura no Asaas |

### Return type

[**SubscriptionGetResponseDTO**](SubscriptionGetResponseDTO.md)

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
| **404**     | Not found                                                                                                         | -                |
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **remover_assinatura**

> SubscriptionDeleteResponseDTO remover_assinatura(id)

Remover assinatura

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_delete_response_dto import SubscriptionDeleteResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas

    try:
        # Remover assinatura
        api_response = api_instance.remover_assinatura(id)
        print("The response of AssinaturasApi->remover_assinatura:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->remover_assinatura: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                | Notes |
| ------ | ------- | ------------------------------------------ | ----- |
| **id** | **str** | Identificador único da assinatura no Asaas |

### Return type

[**SubscriptionDeleteResponseDTO**](SubscriptionDeleteResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **remover_configuracao_para_emissao_de_notas_fiscais**

> SubscriptionDeleteInvoiceConfigResponseDTO remover_configuracao_para_emissao_de_notas_fiscais(id)

Remover configuração para emissão de Notas Fiscais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.subscription_delete_invoice_config_response_dto import SubscriptionDeleteInvoiceConfigResponseDTO
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
    api_instance = asaas.AssinaturasApi(api_client)
    id = 'sub_VXJBYgP2u0eO' # str | Identificador único da assinatura no Asaas

    try:
        # Remover configuração para emissão de Notas Fiscais
        api_response = api_instance.remover_configuracao_para_emissao_de_notas_fiscais(id)
        print("The response of AssinaturasApi->remover_configuracao_para_emissao_de_notas_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssinaturasApi->remover_configuracao_para_emissao_de_notas_fiscais: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                | Notes |
| ------ | ------- | ------------------------------------------ | ----- |
| **id** | **str** | Identificador único da assinatura no Asaas |

### Return type

[**SubscriptionDeleteInvoiceConfigResponseDTO**](SubscriptionDeleteInvoiceConfigResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)
