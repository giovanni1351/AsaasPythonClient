# asaas.CobranasComDadosResumidosApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                                                                                                 | HTTP request                                             | Description                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------- | ------------------------------------------------------------------------------- |
| [**atualizar_cobranca_existente_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#atualizar_cobranca_existente_com_dados_resumidos_na_resposta)                                       | **PUT** /v3/lean/payments/{id}                           | Atualizar cobrança existente com dados resumidos na resposta                    |
| [**capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta)                     | **POST** /v3/lean/payments/{id}/captureAuthorizedPayment | Capturar cobrança com Pré-Autorização com dados resumidos na resposta           |
| [**confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta)                             | **POST** /v3/lean/payments/{id}/receiveInCash            | Confirmar recebimento em dinheiro com dados resumidos na resposta               |
| [**criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta)                       | **POST** /v3/lean/payments/                              | Criar cobrança com cartão de crédito com dados resumidos na resposta            |
| [**criar_nova_cobranca_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#criar_nova_cobranca_com_dados_resumidos_na_resposta)                                                         | **POST** /v3/lean/payments                               | Criar nova cobrança com dados resumidos na resposta                             |
| [**desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta) | **POST** /v3/lean/payments/{id}/undoReceivedInCash       | Desfazer confirmação de recebimento em dinheiro com dados resumidos na resposta |
| [**estornar_cobranca_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#estornar_cobranca_com_dados_resumidos_na_resposta)                                                             | **POST** /v3/lean/payments/{id}/refund                   | Estornar cobrança com dados resumidos na resposta                               |
| [**excluir_cobranca_com_dados_resumidos**](CobranasComDadosResumidosApi.md#excluir_cobranca_com_dados_resumidos)                                                                                       | **DELETE** /v3/lean/payments/{id}                        | Excluir cobrança com dados resumidos                                            |
| [**listar_cobrancas_com_dados_resumidos**](CobranasComDadosResumidosApi.md#listar_cobrancas_com_dados_resumidos)                                                                                       | **GET** /v3/lean/payments                                | Listar cobranças com dados resumidos                                            |
| [**recuperar_uma_unica_cobranca_com_dados_resumidos**](CobranasComDadosResumidosApi.md#recuperar_uma_unica_cobranca_com_dados_resumidos)                                                               | **GET** /v3/lean/payments/{id}                           | Recuperar uma única cobrança com dados resumidos                                |
| [**restaurar_cobranca_removida_com_dados_resumidos_na_resposta**](CobranasComDadosResumidosApi.md#restaurar_cobranca_removida_com_dados_resumidos_na_resposta)                                         | **POST** /v3/lean/payments/{id}/restore                  | Restaurar cobrança removida com dados resumidos na resposta                     |

# **atualizar_cobranca_existente_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO atualizar_cobranca_existente_com_dados_resumidos_na_resposta(id, body=body)

Atualizar cobrança existente com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Atualizar cobrança existente com dados resumidos na resposta
        api_response = api_instance.atualizar_cobranca_existente_com_dados_resumidos_na_resposta(id, body=body)
        print("The response of CobranasComDadosResumidosApi->atualizar_cobranca_existente_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->atualizar_cobranca_existente_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta(id, body=body)

Capturar cobrança com Pré-Autorização com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Capturar cobrança com Pré-Autorização com dados resumidos na resposta
        api_response = api_instance.capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta(id, body=body)
        print("The response of CobranasComDadosResumidosApi->capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->capturar_cobranca_com_pre_autorizacao_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta(id, payment_receive_in_cash_request_dto=payment_receive_in_cash_request_dto)

Confirmar recebimento em dinheiro com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
from asaas.models.payment_receive_in_cash_request_dto import PaymentReceiveInCashRequestDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    payment_receive_in_cash_request_dto = asaas.PaymentReceiveInCashRequestDTO() # PaymentReceiveInCashRequestDTO |  (optional)

    try:
        # Confirmar recebimento em dinheiro com dados resumidos na resposta
        api_response = api_instance.confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta(id, payment_receive_in_cash_request_dto=payment_receive_in_cash_request_dto)
        print("The response of CobranasComDadosResumidosApi->confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->confirmar_recebimento_em_dinheiro_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name                                    | Type                                                                    | Description                              | Notes      |
| --------------------------------------- | ----------------------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                                  | **str**                                                                 | Identificador único da cobrança no Asaas |
| **payment_receive_in_cash_request_dto** | [**PaymentReceiveInCashRequestDTO**](PaymentReceiveInCashRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta**

> PaymentLeanSaveWithCreditCardResponseDTO criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta(payment_save_with_credit_card_request_dto=payment_save_with_credit_card_request_dto)

Criar cobrança com cartão de crédito com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_save_with_credit_card_response_dto import PaymentLeanSaveWithCreditCardResponseDTO
from asaas.models.payment_save_with_credit_card_request_dto import PaymentSaveWithCreditCardRequestDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    payment_save_with_credit_card_request_dto = asaas.PaymentSaveWithCreditCardRequestDTO() # PaymentSaveWithCreditCardRequestDTO |  (optional)

    try:
        # Criar cobrança com cartão de crédito com dados resumidos na resposta
        api_response = api_instance.criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta(payment_save_with_credit_card_request_dto=payment_save_with_credit_card_request_dto)
        print("The response of CobranasComDadosResumidosApi->criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->criar_cobranca_com_cartao_de_credito_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name                                          | Type                                                                              | Description | Notes      |
| --------------------------------------------- | --------------------------------------------------------------------------------- | ----------- | ---------- |
| **payment_save_with_credit_card_request_dto** | [**PaymentSaveWithCreditCardRequestDTO**](PaymentSaveWithCreditCardRequestDTO.md) |             | [optional] |

### Return type

[**PaymentLeanSaveWithCreditCardResponseDTO**](PaymentLeanSaveWithCreditCardResponseDTO.md)

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

# **criar_nova_cobranca_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO criar_nova_cobranca_com_dados_resumidos_na_resposta(payment_save_request_dto=payment_save_request_dto)

Criar nova cobrança com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
from asaas.models.payment_save_request_dto import PaymentSaveRequestDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    payment_save_request_dto = asaas.PaymentSaveRequestDTO() # PaymentSaveRequestDTO |  (optional)

    try:
        # Criar nova cobrança com dados resumidos na resposta
        api_response = api_instance.criar_nova_cobranca_com_dados_resumidos_na_resposta(payment_save_request_dto=payment_save_request_dto)
        print("The response of CobranasComDadosResumidosApi->criar_nova_cobranca_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->criar_nova_cobranca_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name                         | Type                                                  | Description | Notes      |
| ---------------------------- | ----------------------------------------------------- | ----------- | ---------- |
| **payment_save_request_dto** | [**PaymentSaveRequestDTO**](PaymentSaveRequestDTO.md) |             | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta(id, body=body)

Desfazer confirmação de recebimento em dinheiro com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Desfazer confirmação de recebimento em dinheiro com dados resumidos na resposta
        api_response = api_instance.desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta(id, body=body)
        print("The response of CobranasComDadosResumidosApi->desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->desfazer_confirmacao_de_recebimento_em_dinheiro_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **estornar_cobranca_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO estornar_cobranca_com_dados_resumidos_na_resposta(id, payment_refund_request_dto=payment_refund_request_dto)

Estornar cobrança com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
from asaas.models.payment_refund_request_dto import PaymentRefundRequestDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    payment_refund_request_dto = asaas.PaymentRefundRequestDTO() # PaymentRefundRequestDTO |  (optional)

    try:
        # Estornar cobrança com dados resumidos na resposta
        api_response = api_instance.estornar_cobranca_com_dados_resumidos_na_resposta(id, payment_refund_request_dto=payment_refund_request_dto)
        print("The response of CobranasComDadosResumidosApi->estornar_cobranca_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->estornar_cobranca_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name                           | Type                                                      | Description                              | Notes      |
| ------------------------------ | --------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                         | **str**                                                   | Identificador único da cobrança no Asaas |
| **payment_refund_request_dto** | [**PaymentRefundRequestDTO**](PaymentRefundRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **excluir_cobranca_com_dados_resumidos**

> PaymentDeleteResponseDTO excluir_cobranca_com_dados_resumidos(id)

Excluir cobrança com dados resumidos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_delete_response_dto import PaymentDeleteResponseDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Excluir cobrança com dados resumidos
        api_response = api_instance.excluir_cobranca_com_dados_resumidos(id)
        print("The response of CobranasComDadosResumidosApi->excluir_cobranca_com_dados_resumidos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->excluir_cobranca_com_dados_resumidos: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentDeleteResponseDTO**](PaymentDeleteResponseDTO.md)

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

# **listar_cobrancas_com_dados_resumidos**

> PaymentLeanListResponseDTO listar_cobrancas_com_dados_resumidos(offset=offset, limit=limit, customer=customer, customer_group_name=customer_group_name, billing_type=billing_type, status=status, subscription=subscription, installment=installment, external_reference=external_reference, payment_date=payment_date, invoice_status=invoice_status, estimated_credit_date=estimated_credit_date, pix_qr_code_id=pix_qr_code_id, anticipated=anticipated, anticipable=anticipable, date_created_ge=date_created_ge, date_created_le=date_created_le, payment_date_ge=payment_date_ge, payment_date_le=payment_date_le, estimated_credit_date_ge=estimated_credit_date_ge, estimated_credit_date_le=estimated_credit_date_le, due_date_ge=due_date_ge, due_date_le=due_date_le, user=user, checkout_session=checkout_session)

Listar cobranças com dados resumidos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_list_response_dto import PaymentLeanListResponseDTO
from asaas.models.payment_list_request_billing_type import PaymentListRequestBillingType
from asaas.models.payment_list_request_invoice_status import PaymentListRequestInvoiceStatus
from asaas.models.payment_list_request_payment_status import PaymentListRequestPaymentStatus
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    customer = 'customer_example' # str | Filtrar pelo Identificador único do cliente (optional)
    customer_group_name = 'customer_group_name_example' # str | Filtrar pelo nome do grupo de cliente (optional)
    billing_type = asaas.PaymentListRequestBillingType() # PaymentListRequestBillingType | Filtrar por forma de pagamento (optional)
    status = asaas.PaymentListRequestPaymentStatus() # PaymentListRequestPaymentStatus | Filtrar por status (optional)
    subscription = 'subscription_example' # str | Filtrar pelo Identificador único da assinatura (optional)
    installment = 'installment_example' # str | Filtrar pelo Identificador único do parcelamento (optional)
    external_reference = 'external_reference_example' # str | Filtrar pelo Identificador do seu sistema (optional)
    payment_date = 'payment_date_example' # str | Filtrar pela data de pagamento (optional)
    invoice_status = asaas.PaymentListRequestInvoiceStatus() # PaymentListRequestInvoiceStatus | Filtro para retornar cobranças que possuem ou não nota fiscal (optional)
    estimated_credit_date = 'estimated_credit_date_example' # str | Filtrar pela data estimada de crédito (optional)
    pix_qr_code_id = 'pix_qr_code_id_example' # str | Filtrar recebimentos originados de um QrCode estático utilizando o id gerado na hora da criação do QrCode (optional)
    anticipated = True # bool | Filtrar registros antecipados ou não (optional)
    anticipable = True # bool | Filtrar registros antecipaveis ou não (optional)
    date_created_ge = 'date_created_ge_example' # str | Filtrar a partir da data de criação inicial (optional)
    date_created_le = 'date_created_le_example' # str | Filtrar até a data de criação final (optional)
    payment_date_ge = 'payment_date_ge_example' # str | Filtrar a partir da data de recebimento inicial (optional)
    payment_date_le = 'payment_date_le_example' # str | Filtrar até a data de recebimento final (optional)
    estimated_credit_date_ge = 'estimated_credit_date_ge_example' # str | Filtrar a partir da data estimada de crédito inicial (optional)
    estimated_credit_date_le = 'estimated_credit_date_le_example' # str | Filtrar até a data estimada de crédito final (optional)
    due_date_ge = 'due_date_ge_example' # str | Filtrar a partir da data de vencimento inicial (optional)
    due_date_le = 'due_date_le_example' # str | Filtrar até a data de vencimento final (optional)
    user = 'user_example' # str | Filtrar pelo endereço de e-mail do usuário que criou a cobrança (optional)
    checkout_session = 'checkout_session_example' # str | Filtrar pelo identificador único da checkout (optional)

    try:
        # Listar cobranças com dados resumidos
        api_response = api_instance.listar_cobrancas_com_dados_resumidos(offset=offset, limit=limit, customer=customer, customer_group_name=customer_group_name, billing_type=billing_type, status=status, subscription=subscription, installment=installment, external_reference=external_reference, payment_date=payment_date, invoice_status=invoice_status, estimated_credit_date=estimated_credit_date, pix_qr_code_id=pix_qr_code_id, anticipated=anticipated, anticipable=anticipable, date_created_ge=date_created_ge, date_created_le=date_created_le, payment_date_ge=payment_date_ge, payment_date_le=payment_date_le, estimated_credit_date_ge=estimated_credit_date_ge, estimated_credit_date_le=estimated_credit_date_le, due_date_ge=due_date_ge, due_date_le=due_date_le, user=user, checkout_session=checkout_session)
        print("The response of CobranasComDadosResumidosApi->listar_cobrancas_com_dados_resumidos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->listar_cobrancas_com_dados_resumidos: %s\n" % e)
```

### Parameters

| Name                         | Type                                       | Description                                                                                               | Notes      |
| ---------------------------- | ------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ---------- |
| **offset**                   | **int**                                    | Elemento inicial da lista                                                                                 | [optional] |
| **limit**                    | **int**                                    | Número de elementos da lista (max: 100)                                                                   | [optional] |
| **customer**                 | **str**                                    | Filtrar pelo Identificador único do cliente                                                               | [optional] |
| **customer_group_name**      | **str**                                    | Filtrar pelo nome do grupo de cliente                                                                     | [optional] |
| **billing_type**             | [**PaymentListRequestBillingType**](.md)   | Filtrar por forma de pagamento                                                                            | [optional] |
| **status**                   | [**PaymentListRequestPaymentStatus**](.md) | Filtrar por status                                                                                        | [optional] |
| **subscription**             | **str**                                    | Filtrar pelo Identificador único da assinatura                                                            | [optional] |
| **installment**              | **str**                                    | Filtrar pelo Identificador único do parcelamento                                                          | [optional] |
| **external_reference**       | **str**                                    | Filtrar pelo Identificador do seu sistema                                                                 | [optional] |
| **payment_date**             | **str**                                    | Filtrar pela data de pagamento                                                                            | [optional] |
| **invoice_status**           | [**PaymentListRequestInvoiceStatus**](.md) | Filtro para retornar cobranças que possuem ou não nota fiscal                                             | [optional] |
| **estimated_credit_date**    | **str**                                    | Filtrar pela data estimada de crédito                                                                     | [optional] |
| **pix_qr_code_id**           | **str**                                    | Filtrar recebimentos originados de um QrCode estático utilizando o id gerado na hora da criação do QrCode | [optional] |
| **anticipated**              | **bool**                                   | Filtrar registros antecipados ou não                                                                      | [optional] |
| **anticipable**              | **bool**                                   | Filtrar registros antecipaveis ou não                                                                     | [optional] |
| **date_created_ge**          | **str**                                    | Filtrar a partir da data de criação inicial                                                               | [optional] |
| **date_created_le**          | **str**                                    | Filtrar até a data de criação final                                                                       | [optional] |
| **payment_date_ge**          | **str**                                    | Filtrar a partir da data de recebimento inicial                                                           | [optional] |
| **payment_date_le**          | **str**                                    | Filtrar até a data de recebimento final                                                                   | [optional] |
| **estimated_credit_date_ge** | **str**                                    | Filtrar a partir da data estimada de crédito inicial                                                      | [optional] |
| **estimated_credit_date_le** | **str**                                    | Filtrar até a data estimada de crédito final                                                              | [optional] |
| **due_date_ge**              | **str**                                    | Filtrar a partir da data de vencimento inicial                                                            | [optional] |
| **due_date_le**              | **str**                                    | Filtrar até a data de vencimento final                                                                    | [optional] |
| **user**                     | **str**                                    | Filtrar pelo endereço de e-mail do usuário que criou a cobrança                                           | [optional] |
| **checkout_session**         | **str**                                    | Filtrar pelo identificador único da checkout                                                              | [optional] |

### Return type

[**PaymentLeanListResponseDTO**](PaymentLeanListResponseDTO.md)

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

# **recuperar_uma_unica_cobranca_com_dados_resumidos**

> PaymentLeanGetResponseDTO recuperar_uma_unica_cobranca_com_dados_resumidos(id)

Recuperar uma única cobrança com dados resumidos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Recuperar uma única cobrança com dados resumidos
        api_response = api_instance.recuperar_uma_unica_cobranca_com_dados_resumidos(id)
        print("The response of CobranasComDadosResumidosApi->recuperar_uma_unica_cobranca_com_dados_resumidos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->recuperar_uma_unica_cobranca_com_dados_resumidos: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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

# **restaurar_cobranca_removida_com_dados_resumidos_na_resposta**

> PaymentLeanGetResponseDTO restaurar_cobranca_removida_com_dados_resumidos_na_resposta(id, body=body)

Restaurar cobrança removida com dados resumidos na resposta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_lean_get_response_dto import PaymentLeanGetResponseDTO
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
    api_instance = asaas.CobranasComDadosResumidosApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Restaurar cobrança removida com dados resumidos na resposta
        api_response = api_instance.restaurar_cobranca_removida_com_dados_resumidos_na_resposta(id, body=body)
        print("The response of CobranasComDadosResumidosApi->restaurar_cobranca_removida_com_dados_resumidos_na_resposta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasComDadosResumidosApi->restaurar_cobranca_removida_com_dados_resumidos_na_resposta: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentLeanGetResponseDTO**](PaymentLeanGetResponseDTO.md)

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
