# asaas.PixAutomticoApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                                        | HTTP request                                       | Description                                |
| --------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ------------------------------------------ |
| [**cancelar_uma_autorizacao_pix_automatico**](PixAutomticoApi.md#cancelar_uma_autorizacao_pix_automatico)                                     | **DELETE** /v3/pix/automatic/authorizations/{id}   | Cancelar uma autorização                   |
| [**criar_uma_autorizacao_pix_automatico**](PixAutomticoApi.md#criar_uma_autorizacao_pix_automatico)                                           | **POST** /v3/pix/automatic/authorizations          | Criar uma autorização                      |
| [**listar_autorizacoes_pix_automatico**](PixAutomticoApi.md#listar_autorizacoes_pix_automatico)                                               | **GET** /v3/pix/automatic/authorizations           | Listar autorizações                        |
| [**listar_instrucoes_de_pagamento_pix_automatico**](PixAutomticoApi.md#listar_instrucoes_de_pagamento_pix_automatico)                         | **GET** /v3/pix/automatic/paymentInstructions      | Listar instruções de pagamento             |
| [**recuperar_uma_unica_autorizacao_pix_automatico**](PixAutomticoApi.md#recuperar_uma_unica_autorizacao_pix_automatico)                       | **GET** /v3/pix/automatic/authorizations/{id}      | Recuperar uma única autorização            |
| [**recuperar_uma_unica_instrucao_de_pagamento_pix_automatico**](PixAutomticoApi.md#recuperar_uma_unica_instrucao_de_pagamento_pix_automatico) | **GET** /v3/pix/automatic/paymentInstructions/{id} | Recuperar uma única instrução de pagamento |

# **cancelar_uma_autorizacao_pix_automatico**

> PixReceiverAutomaticRecurringAuthorizationGetResponseDTO cancelar_uma_autorizacao_pix_automatico(id)

Cancelar uma autorização

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_receiver_automatic_recurring_authorization_get_response_dto import PixReceiverAutomaticRecurringAuthorizationGetResponseDTO
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
    api_instance = asaas.PixAutomticoApi(api_client)
    id = 'a33047b1-fb19-4b68-9373-a7ba8a8162aa' # str | Identificador único da autorização de Pix Automático no Asaas

    try:
        # Cancelar uma autorização
        api_response = api_instance.cancelar_uma_autorizacao_pix_automatico(id)
        print("The response of PixAutomticoApi->cancelar_uma_autorizacao_pix_automatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixAutomticoApi->cancelar_uma_autorizacao_pix_automatico: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                                   | Notes |
| ------ | ------- | ------------------------------------------------------------- | ----- |
| **id** | **str** | Identificador único da autorização de Pix Automático no Asaas |

### Return type

[**PixReceiverAutomaticRecurringAuthorizationGetResponseDTO**](PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.md)

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

# **criar_uma_autorizacao_pix_automatico**

> PixReceiverAutomaticRecurringAuthorizationGetResponseDTO criar_uma_autorizacao_pix_automatico(pix_receiver_automatic_recurring_authorization_save_request_dto=pix_receiver_automatic_recurring_authorization_save_request_dto)

Criar uma autorização

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_receiver_automatic_recurring_authorization_get_response_dto import PixReceiverAutomaticRecurringAuthorizationGetResponseDTO
from asaas.models.pix_receiver_automatic_recurring_authorization_save_request_dto import PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO
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
    api_instance = asaas.PixAutomticoApi(api_client)
    pix_receiver_automatic_recurring_authorization_save_request_dto = asaas.PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO() # PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO |  (optional)

    try:
        # Criar uma autorização
        api_response = api_instance.criar_uma_autorizacao_pix_automatico(pix_receiver_automatic_recurring_authorization_save_request_dto=pix_receiver_automatic_recurring_authorization_save_request_dto)
        print("The response of PixAutomticoApi->criar_uma_autorizacao_pix_automatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixAutomticoApi->criar_uma_autorizacao_pix_automatico: %s\n" % e)
```

### Parameters

| Name                                                                | Type                                                                                                                        | Description | Notes      |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ----------- | ---------- |
| **pix_receiver_automatic_recurring_authorization_save_request_dto** | [**PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO**](PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO.md) |             | [optional] |

### Return type

[**PixReceiverAutomaticRecurringAuthorizationGetResponseDTO**](PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.md)

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

# **listar_autorizacoes_pix_automatico**

> PixReceiverAutomaticRecurringAuthorizationListResponseDTO listar_autorizacoes_pix_automatico(offset=offset, limit=limit, status=status, customer_id=customer_id)

Listar autorizações

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_receiver_automatic_recurring_authorization_list_request_pix_receiver_automatic_recurring_authorization_status import PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus
from asaas.models.pix_receiver_automatic_recurring_authorization_list_response_dto import PixReceiverAutomaticRecurringAuthorizationListResponseDTO
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
    api_instance = asaas.PixAutomticoApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    status = asaas.PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus() # PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus | Filtrar pelo status atual da autorização (optional)
    customer_id = 'cus_000005735721' # str | Filtrar pelo identificador único do cliente (optional)

    try:
        # Listar autorizações
        api_response = api_instance.listar_autorizacoes_pix_automatico(offset=offset, limit=limit, status=status, customer_id=customer_id)
        print("The response of PixAutomticoApi->listar_autorizacoes_pix_automatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixAutomticoApi->listar_autorizacoes_pix_automatico: %s\n" % e)
```

### Parameters

| Name            | Type                                                                                                             | Description                                 | Notes      |
| --------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------- | ---------- |
| **offset**      | **int**                                                                                                          | Elemento inicial da lista                   | [optional] |
| **limit**       | **int**                                                                                                          | Número de elementos da lista (max: 100)     | [optional] |
| **status**      | [**PixReceiverAutomaticRecurringAuthorizationListRequestPixReceiverAutomaticRecurringAuthorizationStatus**](.md) | Filtrar pelo status atual da autorização    | [optional] |
| **customer_id** | **str**                                                                                                          | Filtrar pelo identificador único do cliente | [optional] |

### Return type

[**PixReceiverAutomaticRecurringAuthorizationListResponseDTO**](PixReceiverAutomaticRecurringAuthorizationListResponseDTO.md)

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

# **listar_instrucoes_de_pagamento_pix_automatico**

> PixAutomaticRecurringPaymentInstructionListResponseDTO listar_instrucoes_de_pagamento_pix_automatico(authorization_id=authorization_id, customer_id=customer_id, payment_id=payment_id, status=status)

Listar instruções de pagamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_automatic_recurring_payment_instruction_list_request_pix_automatic_recurring_payment_instruction_status import PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus
from asaas.models.pix_automatic_recurring_payment_instruction_list_response_dto import PixAutomaticRecurringPaymentInstructionListResponseDTO
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
    api_instance = asaas.PixAutomticoApi(api_client)
    authorization_id = 'authorization_id_example' # str | Filtrar pelo identificador único da autorização da instrução (optional)
    customer_id = 'cus_000005735721' # str | Filtrar pelo identificador único do cliente (optional)
    payment_id = 'payment_id_example' # str | Filtrar pelo identificador único da cobrança (optional)
    status = asaas.PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus() # PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus | Filtrar pelo status da instrução (optional)

    try:
        # Listar instruções de pagamento
        api_response = api_instance.listar_instrucoes_de_pagamento_pix_automatico(authorization_id=authorization_id, customer_id=customer_id, payment_id=payment_id, status=status)
        print("The response of PixAutomticoApi->listar_instrucoes_de_pagamento_pix_automatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixAutomticoApi->listar_instrucoes_de_pagamento_pix_automatico: %s\n" % e)
```

### Parameters

| Name                 | Type                                                                                                       | Description                                                  | Notes      |
| -------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | ---------- |
| **authorization_id** | **str**                                                                                                    | Filtrar pelo identificador único da autorização da instrução | [optional] |
| **customer_id**      | **str**                                                                                                    | Filtrar pelo identificador único do cliente                  | [optional] |
| **payment_id**       | **str**                                                                                                    | Filtrar pelo identificador único da cobrança                 | [optional] |
| **status**           | [**PixAutomaticRecurringPaymentInstructionListRequestPixAutomaticRecurringPaymentInstructionStatus**](.md) | Filtrar pelo status da instrução                             | [optional] |

### Return type

[**PixAutomaticRecurringPaymentInstructionListResponseDTO**](PixAutomaticRecurringPaymentInstructionListResponseDTO.md)

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

# **recuperar_uma_unica_autorizacao_pix_automatico**

> PixReceiverAutomaticRecurringAuthorizationGetResponseDTO recuperar_uma_unica_autorizacao_pix_automatico(id)

Recuperar uma única autorização

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_receiver_automatic_recurring_authorization_get_response_dto import PixReceiverAutomaticRecurringAuthorizationGetResponseDTO
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
    api_instance = asaas.PixAutomticoApi(api_client)
    id = 'a33047b1-fb19-4b68-9373-a7ba8a8162aa' # str | Identificador único da autorização de Pix Automático no Asaas

    try:
        # Recuperar uma única autorização
        api_response = api_instance.recuperar_uma_unica_autorizacao_pix_automatico(id)
        print("The response of PixAutomticoApi->recuperar_uma_unica_autorizacao_pix_automatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixAutomticoApi->recuperar_uma_unica_autorizacao_pix_automatico: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                                   | Notes |
| ------ | ------- | ------------------------------------------------------------- | ----- |
| **id** | **str** | Identificador único da autorização de Pix Automático no Asaas |

### Return type

[**PixReceiverAutomaticRecurringAuthorizationGetResponseDTO**](PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.md)

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

# **recuperar_uma_unica_instrucao_de_pagamento_pix_automatico**

> PixAutomaticRecurringPaymentInstructionGetResponseDTO recuperar_uma_unica_instrucao_de_pagamento_pix_automatico(id)

Recuperar uma única instrução de pagamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.pix_automatic_recurring_payment_instruction_get_response_dto import PixAutomaticRecurringPaymentInstructionGetResponseDTO
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
    api_instance = asaas.PixAutomticoApi(api_client)
    id = 'cbfdf6ef-9bd8-48ba-b8cd-efd61a9f614c' # str | Identificador único da instrução de pagamento de Pix Automático no Asaas

    try:
        # Recuperar uma única instrução de pagamento
        api_response = api_instance.recuperar_uma_unica_instrucao_de_pagamento_pix_automatico(id)
        print("The response of PixAutomticoApi->recuperar_uma_unica_instrucao_de_pagamento_pix_automatico:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PixAutomticoApi->recuperar_uma_unica_instrucao_de_pagamento_pix_automatico: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                                              | Notes |
| ------ | ------- | ------------------------------------------------------------------------ | ----- |
| **id** | **str** | Identificador único da instrução de pagamento de Pix Automático no Asaas |

### Return type

[**PixAutomaticRecurringPaymentInstructionGetResponseDTO**](PixAutomaticRecurringPaymentInstructionGetResponseDTO.md)

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
