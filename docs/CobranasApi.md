# asaas.CobranasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                      | HTTP request                                        | Description                                        |
| --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | -------------------------------------------------- |
| [**atualizar_cobranca_existente**](CobranasApi.md#atualizar_cobranca_existente)                                             | **PUT** /v3/payments/{id}                           | Atualizar cobrança existente                       |
| [**capturar_cobranca_com_pre_autorizacao**](CobranasApi.md#capturar_cobranca_com_pre_autorizacao)                           | **POST** /v3/payments/{id}/captureAuthorizedPayment | Capturar cobrança com Pré-Autorização              |
| [**confirmar_recebimento_em_dinheiro**](CobranasApi.md#confirmar_recebimento_em_dinheiro)                                   | **POST** /v3/payments/{id}/receiveInCash            | Confirmar recebimento em dinheiro                  |
| [**criar_cobranca_com_cartao_de_credito**](CobranasApi.md#criar_cobranca_com_cartao_de_credito)                             | **POST** /v3/payments/                              | Criar cobrança com cartão de crédito               |
| [**criar_nova_cobranca**](CobranasApi.md#criar_nova_cobranca)                                                               | **POST** /v3/payments                               | Criar nova cobrança                                |
| [**desfazer_confirmacao_de_recebimento_em_dinheiro**](CobranasApi.md#desfazer_confirmacao_de_recebimento_em_dinheiro)       | **POST** /v3/payments/{id}/undoReceivedInCash       | Desfazer confirmação de recebimento em dinheiro    |
| [**estornar_cobranca**](CobranasApi.md#estornar_cobranca)                                                                   | **POST** /v3/payments/{id}/refund                   | Estornar cobrança                                  |
| [**excluir_cobranca**](CobranasApi.md#excluir_cobranca)                                                                     | **DELETE** /v3/payments/{id}                        | Excluir cobrança                                   |
| [**informacoes_sobre_visualizacao_da_cobranca**](CobranasApi.md#informacoes_sobre_visualizacao_da_cobranca)                 | **GET** /v3/payments/{id}/viewingInfo               | Informações sobre visualização da cobrança         |
| [**listar_cobrancas**](CobranasApi.md#listar_cobrancas)                                                                     | **GET** /v3/payments                                | Listar cobranças                                   |
| [**obter_linha_digitavel_do_boleto**](CobranasApi.md#obter_linha_digitavel_do_boleto)                                       | **GET** /v3/payments/{id}/identificationField       | Obter linha digitável do boleto                    |
| [**obter_qr_code_para_pagamentos_via_pix**](CobranasApi.md#obter_qr_code_para_pagamentos_via_pix)                           | **GET** /v3/payments/{id}/pixQrCode                 | Obter QR Code para pagamentos via Pix              |
| [**pagar_uma_cobranca_com_cartao_de_credito**](CobranasApi.md#pagar_uma_cobranca_com_cartao_de_credito)                     | **POST** /v3/payments/{id}/payWithCreditCard        | Pagar uma cobrança com cartão de crédito           |
| [**recuperando_limites_de_cobrancas**](CobranasApi.md#recuperando_limites_de_cobrancas)                                     | **GET** /v3/payments/limits                         | Recuperando limites de cobranças                   |
| [**recuperar_informacoes_de_pagamento_de_uma_cobranca**](CobranasApi.md#recuperar_informacoes_de_pagamento_de_uma_cobranca) | **GET** /v3/payments/{id}/billingInfo               | Recuperar informações de pagamento de uma cobrança |
| [**recuperar_status_de_uma_cobranca**](CobranasApi.md#recuperar_status_de_uma_cobranca)                                     | **GET** /v3/payments/{id}/status                    | Recuperar status de uma cobrança                   |
| [**recuperar_uma_unica_cobranca**](CobranasApi.md#recuperar_uma_unica_cobranca)                                             | **GET** /v3/payments/{id}                           | Recuperar uma única cobrança                       |
| [**restaurar_cobranca_removida**](CobranasApi.md#restaurar_cobranca_removida)                                               | **POST** /v3/payments/{id}/restore                  | Restaurar cobrança removida                        |
| [**simulador_de_vendas**](CobranasApi.md#simulador_de_vendas)                                                               | **POST** /v3/payments/simulate                      | Simulador de vendas                                |

# **atualizar_cobranca_existente**

> PaymentGetResponseDTO atualizar_cobranca_existente(id, payment_update_request_dto=payment_update_request_dto)

Atualizar cobrança existente

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
from asaas.models.payment_update_request_dto import PaymentUpdateRequestDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'pay_080225913252' # str | Identificador único da cobrança no Asaas
    payment_update_request_dto = asaas.PaymentUpdateRequestDTO() # PaymentUpdateRequestDTO |  (optional)

    try:
        # Atualizar cobrança existente
        api_response = api_instance.atualizar_cobranca_existente(id, payment_update_request_dto=payment_update_request_dto)
        print("The response of CobranasApi->atualizar_cobranca_existente:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->atualizar_cobranca_existente: %s\n" % e)
```

### Parameters

| Name                           | Type                                                      | Description                              | Notes      |
| ------------------------------ | --------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                         | **str**                                                   | Identificador único da cobrança no Asaas |
| **payment_update_request_dto** | [**PaymentUpdateRequestDTO**](PaymentUpdateRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **capturar_cobranca_com_pre_autorizacao**

> PaymentGetResponseDTO capturar_cobranca_com_pre_autorizacao(id, body=body)

Capturar cobrança com Pré-Autorização

### Example

- Api Key Authentication (Authorization):

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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Capturar cobrança com Pré-Autorização
        api_response = api_instance.capturar_cobranca_com_pre_autorizacao(id, body=body)
        print("The response of CobranasApi->capturar_cobranca_com_pre_autorizacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->capturar_cobranca_com_pre_autorizacao: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **confirmar_recebimento_em_dinheiro**

> PaymentGetResponseDTO confirmar_recebimento_em_dinheiro(id, payment_receive_in_cash_request_dto=payment_receive_in_cash_request_dto)

Confirmar recebimento em dinheiro

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    payment_receive_in_cash_request_dto = asaas.PaymentReceiveInCashRequestDTO() # PaymentReceiveInCashRequestDTO |  (optional)

    try:
        # Confirmar recebimento em dinheiro
        api_response = api_instance.confirmar_recebimento_em_dinheiro(id, payment_receive_in_cash_request_dto=payment_receive_in_cash_request_dto)
        print("The response of CobranasApi->confirmar_recebimento_em_dinheiro:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->confirmar_recebimento_em_dinheiro: %s\n" % e)
```

### Parameters

| Name                                    | Type                                                                    | Description                              | Notes      |
| --------------------------------------- | ----------------------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                                  | **str**                                                                 | Identificador único da cobrança no Asaas |
| **payment_receive_in_cash_request_dto** | [**PaymentReceiveInCashRequestDTO**](PaymentReceiveInCashRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **criar_cobranca_com_cartao_de_credito**

> PaymentGetResponseDTO criar_cobranca_com_cartao_de_credito(payment_save_with_credit_card_request_dto=payment_save_with_credit_card_request_dto)

Criar cobrança com cartão de crédito

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    payment_save_with_credit_card_request_dto = asaas.PaymentSaveWithCreditCardRequestDTO() # PaymentSaveWithCreditCardRequestDTO |  (optional)

    try:
        # Criar cobrança com cartão de crédito
        api_response = api_instance.criar_cobranca_com_cartao_de_credito(payment_save_with_credit_card_request_dto=payment_save_with_credit_card_request_dto)
        print("The response of CobranasApi->criar_cobranca_com_cartao_de_credito:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->criar_cobranca_com_cartao_de_credito: %s\n" % e)
```

### Parameters

| Name                                          | Type                                                                              | Description | Notes      |
| --------------------------------------------- | --------------------------------------------------------------------------------- | ----------- | ---------- |
| **payment_save_with_credit_card_request_dto** | [**PaymentSaveWithCreditCardRequestDTO**](PaymentSaveWithCreditCardRequestDTO.md) |             | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **criar_nova_cobranca**

> PaymentGetResponseDTO criar_nova_cobranca(payment_save_request_dto=payment_save_request_dto)

Criar nova cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    payment_save_request_dto = asaas.PaymentSaveRequestDTO() # PaymentSaveRequestDTO |  (optional)

    try:
        # Criar nova cobrança
        api_response = api_instance.criar_nova_cobranca(payment_save_request_dto=payment_save_request_dto)
        print("The response of CobranasApi->criar_nova_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->criar_nova_cobranca: %s\n" % e)
```

### Parameters

| Name                         | Type                                                  | Description | Notes      |
| ---------------------------- | ----------------------------------------------------- | ----------- | ---------- |
| **payment_save_request_dto** | [**PaymentSaveRequestDTO**](PaymentSaveRequestDTO.md) |             | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **desfazer_confirmacao_de_recebimento_em_dinheiro**

> PaymentGetResponseDTO desfazer_confirmacao_de_recebimento_em_dinheiro(id, body=body)

Desfazer confirmação de recebimento em dinheiro

### Example

- Api Key Authentication (Authorization):

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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Desfazer confirmação de recebimento em dinheiro
        api_response = api_instance.desfazer_confirmacao_de_recebimento_em_dinheiro(id, body=body)
        print("The response of CobranasApi->desfazer_confirmacao_de_recebimento_em_dinheiro:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->desfazer_confirmacao_de_recebimento_em_dinheiro: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **estornar_cobranca**

> PaymentGetResponseDTO estornar_cobranca(id, payment_refund_request_dto=payment_refund_request_dto)

Estornar cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    payment_refund_request_dto = asaas.PaymentRefundRequestDTO() # PaymentRefundRequestDTO |  (optional)

    try:
        # Estornar cobrança
        api_response = api_instance.estornar_cobranca(id, payment_refund_request_dto=payment_refund_request_dto)
        print("The response of CobranasApi->estornar_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->estornar_cobranca: %s\n" % e)
```

### Parameters

| Name                           | Type                                                      | Description                              | Notes      |
| ------------------------------ | --------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                         | **str**                                                   | Identificador único da cobrança no Asaas |
| **payment_refund_request_dto** | [**PaymentRefundRequestDTO**](PaymentRefundRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **excluir_cobranca**

> PaymentDeleteResponseDTO excluir_cobranca(id)

Excluir cobrança

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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Excluir cobrança
        api_response = api_instance.excluir_cobranca(id)
        print("The response of CobranasApi->excluir_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->excluir_cobranca: %s\n" % e)
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

# **informacoes_sobre_visualizacao_da_cobranca**

> PaymentViewingInfoResponseDTO informacoes_sobre_visualizacao_da_cobranca(id)

Informações sobre visualização da cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_viewing_info_response_dto import PaymentViewingInfoResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Informações sobre visualização da cobrança
        api_response = api_instance.informacoes_sobre_visualizacao_da_cobranca(id)
        print("The response of CobranasApi->informacoes_sobre_visualizacao_da_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->informacoes_sobre_visualizacao_da_cobranca: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentViewingInfoResponseDTO**](PaymentViewingInfoResponseDTO.md)

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

# **listar_cobrancas**

> PaymentListResponseDTO listar_cobrancas(offset=offset, limit=limit, customer=customer, customer_group_name=customer_group_name, billing_type=billing_type, status=status, subscription=subscription, installment=installment, external_reference=external_reference, payment_date=payment_date, invoice_status=invoice_status, estimated_credit_date=estimated_credit_date, pix_qr_code_id=pix_qr_code_id, anticipated=anticipated, anticipable=anticipable, date_created_ge=date_created_ge, date_created_le=date_created_le, payment_date_ge=payment_date_ge, payment_date_le=payment_date_le, estimated_credit_date_ge=estimated_credit_date_ge, estimated_credit_date_le=estimated_credit_date_le, due_date_ge=due_date_ge, due_date_le=due_date_le, user=user, checkout_session=checkout_session)

Listar cobranças

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_list_request_billing_type import PaymentListRequestBillingType
from asaas.models.payment_list_request_invoice_status import PaymentListRequestInvoiceStatus
from asaas.models.payment_list_request_payment_status import PaymentListRequestPaymentStatus
from asaas.models.payment_list_response_dto import PaymentListResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
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
        # Listar cobranças
        api_response = api_instance.listar_cobrancas(offset=offset, limit=limit, customer=customer, customer_group_name=customer_group_name, billing_type=billing_type, status=status, subscription=subscription, installment=installment, external_reference=external_reference, payment_date=payment_date, invoice_status=invoice_status, estimated_credit_date=estimated_credit_date, pix_qr_code_id=pix_qr_code_id, anticipated=anticipated, anticipable=anticipable, date_created_ge=date_created_ge, date_created_le=date_created_le, payment_date_ge=payment_date_ge, payment_date_le=payment_date_le, estimated_credit_date_ge=estimated_credit_date_ge, estimated_credit_date_le=estimated_credit_date_le, due_date_ge=due_date_ge, due_date_le=due_date_le, user=user, checkout_session=checkout_session)
        print("The response of CobranasApi->listar_cobrancas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->listar_cobrancas: %s\n" % e)
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
| **400**     | Bad Request                                                                                                       | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **obter_linha_digitavel_do_boleto**

> PaymentIdentificationFieldResponseDTO obter_linha_digitavel_do_boleto(id)

Obter linha digitável do boleto

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_identification_field_response_dto import PaymentIdentificationFieldResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Obter linha digitável do boleto
        api_response = api_instance.obter_linha_digitavel_do_boleto(id)
        print("The response of CobranasApi->obter_linha_digitavel_do_boleto:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->obter_linha_digitavel_do_boleto: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentIdentificationFieldResponseDTO**](PaymentIdentificationFieldResponseDTO.md)

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

# **obter_qr_code_para_pagamentos_via_pix**

> PaymentPixQrCodeResponseDTO obter_qr_code_para_pagamentos_via_pix(id)

Obter QR Code para pagamentos via Pix

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_pix_qr_code_response_dto import PaymentPixQrCodeResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Obter QR Code para pagamentos via Pix
        api_response = api_instance.obter_qr_code_para_pagamentos_via_pix(id)
        print("The response of CobranasApi->obter_qr_code_para_pagamentos_via_pix:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->obter_qr_code_para_pagamentos_via_pix: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentPixQrCodeResponseDTO**](PaymentPixQrCodeResponseDTO.md)

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

# **pagar_uma_cobranca_com_cartao_de_credito**

> PaymentGetResponseDTO pagar_uma_cobranca_com_cartao_de_credito(id, payment_pay_with_credit_card_request_dto=payment_pay_with_credit_card_request_dto)

Pagar uma cobrança com cartão de crédito

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_get_response_dto import PaymentGetResponseDTO
from asaas.models.payment_pay_with_credit_card_request_dto import PaymentPayWithCreditCardRequestDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    payment_pay_with_credit_card_request_dto = asaas.PaymentPayWithCreditCardRequestDTO() # PaymentPayWithCreditCardRequestDTO |  (optional)

    try:
        # Pagar uma cobrança com cartão de crédito
        api_response = api_instance.pagar_uma_cobranca_com_cartao_de_credito(id, payment_pay_with_credit_card_request_dto=payment_pay_with_credit_card_request_dto)
        print("The response of CobranasApi->pagar_uma_cobranca_com_cartao_de_credito:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->pagar_uma_cobranca_com_cartao_de_credito: %s\n" % e)
```

### Parameters

| Name                                         | Type                                                                            | Description                              | Notes      |
| -------------------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------------- | ---------- |
| **id**                                       | **str**                                                                         | Identificador único da cobrança no Asaas |
| **payment_pay_with_credit_card_request_dto** | [**PaymentPayWithCreditCardRequestDTO**](PaymentPayWithCreditCardRequestDTO.md) |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **recuperando_limites_de_cobrancas**

> PaymentLimitsResponseDTO recuperando_limites_de_cobrancas()

Recuperando limites de cobranças

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_limits_response_dto import PaymentLimitsResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)

    try:
        # Recuperando limites de cobranças
        api_response = api_instance.recuperando_limites_de_cobrancas()
        print("The response of CobranasApi->recuperando_limites_de_cobrancas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->recuperando_limites_de_cobrancas: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PaymentLimitsResponseDTO**](PaymentLimitsResponseDTO.md)

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

# **recuperar_informacoes_de_pagamento_de_uma_cobranca**

> PaymentBillingInfoResponseDTO recuperar_informacoes_de_pagamento_de_uma_cobranca(id)

Recuperar informações de pagamento de uma cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_billing_info_response_dto import PaymentBillingInfoResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Recuperar informações de pagamento de uma cobrança
        api_response = api_instance.recuperar_informacoes_de_pagamento_de_uma_cobranca(id)
        print("The response of CobranasApi->recuperar_informacoes_de_pagamento_de_uma_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->recuperar_informacoes_de_pagamento_de_uma_cobranca: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentBillingInfoResponseDTO**](PaymentBillingInfoResponseDTO.md)

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

# **recuperar_status_de_uma_cobranca**

> PaymentStatusResponseDTO recuperar_status_de_uma_cobranca(id)

Recuperar status de uma cobrança

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_status_response_dto import PaymentStatusResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Recuperar status de uma cobrança
        api_response = api_instance.recuperar_status_de_uma_cobranca(id)
        print("The response of CobranasApi->recuperar_status_de_uma_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->recuperar_status_de_uma_cobranca: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentStatusResponseDTO**](PaymentStatusResponseDTO.md)

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

# **recuperar_uma_unica_cobranca**

> PaymentGetResponseDTO recuperar_uma_unica_cobranca(id)

Recuperar uma única cobrança

### Example

- Api Key Authentication (Authorization):

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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas

    try:
        # Recuperar uma única cobrança
        api_response = api_instance.recuperar_uma_unica_cobranca(id)
        print("The response of CobranasApi->recuperar_uma_unica_cobranca:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->recuperar_uma_unica_cobranca: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                              | Notes |
| ------ | ------- | ---------------------------------------- | ----- |
| **id** | **str** | Identificador único da cobrança no Asaas |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **restaurar_cobranca_removida**

> PaymentGetResponseDTO restaurar_cobranca_removida(id, body=body)

Restaurar cobrança removida

### Example

- Api Key Authentication (Authorization):

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
    api_instance = asaas.CobranasApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # Restaurar cobrança removida
        api_response = api_instance.restaurar_cobranca_removida(id, body=body)
        print("The response of CobranasApi->restaurar_cobranca_removida:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->restaurar_cobranca_removida: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

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

# **simulador_de_vendas**

> PaymentSimulateResponseDTO simulador_de_vendas(payment_simulate_request_dto=payment_simulate_request_dto)

Simulador de vendas

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_simulate_request_dto import PaymentSimulateRequestDTO
from asaas.models.payment_simulate_response_dto import PaymentSimulateResponseDTO
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
    api_instance = asaas.CobranasApi(api_client)
    payment_simulate_request_dto = asaas.PaymentSimulateRequestDTO() # PaymentSimulateRequestDTO |  (optional)

    try:
        # Simulador de vendas
        api_response = api_instance.simulador_de_vendas(payment_simulate_request_dto=payment_simulate_request_dto)
        print("The response of CobranasApi->simulador_de_vendas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CobranasApi->simulador_de_vendas: %s\n" % e)
```

### Parameters

| Name                             | Type                                                          | Description | Notes      |
| -------------------------------- | ------------------------------------------------------------- | ----------- | ---------- |
| **payment_simulate_request_dto** | [**PaymentSimulateRequestDTO**](PaymentSimulateRequestDTO.md) |             | [optional] |

### Return type

[**PaymentSimulateResponseDTO**](PaymentSimulateResponseDTO.md)

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
