# asaas.ChargebackApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                              | HTTP request                          | Description                   |
| ----------------------------------------------------------------------------------- | ------------------------------------- | ----------------------------- |
| [**criar_disputa_de_chargeback**](ChargebackApi.md#criar_disputa_de_chargeback)     | **POST** /v3/chargebacks/{id}/dispute | Criar disputa de chargeback   |
| [**listar_chargebacks**](ChargebackApi.md#listar_chargebacks)                       | **GET** /v3/chargebacks/              | Listar chargebacks            |
| [**recuperar_um_unico_chargeback**](ChargebackApi.md#recuperar_um_unico_chargeback) | **GET** /v3/payments/{id}/chargeback  | Recuperar um único chargeback |

# **criar_disputa_de_chargeback**

> ChargebackSaveDisputeResponseDTO criar_disputa_de_chargeback(id, files)

Criar disputa de chargeback

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.chargeback_save_dispute_response_dto import ChargebackSaveDisputeResponseDTO
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
    api_instance = asaas.ChargebackApi(api_client)
    id = '8e784c3e-afe8-4844-bb93-6b445763' # str | Identificador único do chargeback para o qual a disputa será criada.
    files = None # bytes | Arquivos para criar a disputa (Máximo: 11).

    try:
        # Criar disputa de chargeback
        api_response = api_instance.criar_disputa_de_chargeback(id, files)
        print("The response of ChargebackApi->criar_disputa_de_chargeback:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChargebackApi->criar_disputa_de_chargeback: %s\n" % e)
```

### Parameters

| Name      | Type      | Description                                                          | Notes |
| --------- | --------- | -------------------------------------------------------------------- | ----- |
| **id**    | **str**   | Identificador único do chargeback para o qual a disputa será criada. |
| **files** | **bytes** | Arquivos para criar a disputa (Máximo: 11).                          |

### Return type

[**ChargebackSaveDisputeResponseDTO**](ChargebackSaveDisputeResponseDTO.md)

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
| **404**     | Not found    | -                |
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **listar_chargebacks**

> ChargebackListResponseDTO listar_chargebacks(offset=offset, limit=limit, credit_card_brand=credit_card_brand, origin_dispute_date_le=origin_dispute_date_le, origin_dispute_date_ge=origin_dispute_date_ge, origin_transaction_date_le=origin_transaction_date_le, origin_transaction_date_ge=origin_transaction_date_ge, status=status)

Listar chargebacks

Este método retorna uma lista paginada com todos os chargebacks para o(s) filtro(s) informado(s).

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.chargeback_list_request_chargeback_status import ChargebackListRequestChargebackStatus
from asaas.models.chargeback_list_request_credit_card_brand import ChargebackListRequestCreditCardBrand
from asaas.models.chargeback_list_response_dto import ChargebackListResponseDTO
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
    api_instance = asaas.ChargebackApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    credit_card_brand = asaas.ChargebackListRequestCreditCardBrand() # ChargebackListRequestCreditCardBrand | Filtrar por bandeira do cartão utilizado. (optional)
    origin_dispute_date_le = '2024-12-05' # str | Filtrar até uma data de abertura de chargeback. (optional)
    origin_dispute_date_ge = '2023-11-01' # str | Filtrar a partir de uma data de abertura de chargeback. (optional)
    origin_transaction_date_le = '2024-12-05' # str | Filtrar até uma data de transação. (optional)
    origin_transaction_date_ge = '2024-10-10' # str | Filtrar a partir de uma data de transação. (optional)
    status = asaas.ChargebackListRequestChargebackStatus() # ChargebackListRequestChargebackStatus | Filtrar por status do chargeback. (optional)

    try:
        # Listar chargebacks
        api_response = api_instance.listar_chargebacks(offset=offset, limit=limit, credit_card_brand=credit_card_brand, origin_dispute_date_le=origin_dispute_date_le, origin_dispute_date_ge=origin_dispute_date_ge, origin_transaction_date_le=origin_transaction_date_le, origin_transaction_date_ge=origin_transaction_date_ge, status=status)
        print("The response of ChargebackApi->listar_chargebacks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChargebackApi->listar_chargebacks: %s\n" % e)
```

### Parameters

| Name                           | Type                                             | Description                                             | Notes      |
| ------------------------------ | ------------------------------------------------ | ------------------------------------------------------- | ---------- |
| **offset**                     | **int**                                          | Elemento inicial da lista                               | [optional] |
| **limit**                      | **int**                                          | Número de elementos da lista (max: 100)                 | [optional] |
| **credit_card_brand**          | [**ChargebackListRequestCreditCardBrand**](.md)  | Filtrar por bandeira do cartão utilizado.               | [optional] |
| **origin_dispute_date_le**     | **str**                                          | Filtrar até uma data de abertura de chargeback.         | [optional] |
| **origin_dispute_date_ge**     | **str**                                          | Filtrar a partir de uma data de abertura de chargeback. | [optional] |
| **origin_transaction_date_le** | **str**                                          | Filtrar até uma data de transação.                      | [optional] |
| **origin_transaction_date_ge** | **str**                                          | Filtrar a partir de uma data de transação.              | [optional] |
| **status**                     | [**ChargebackListRequestChargebackStatus**](.md) | Filtrar por status do chargeback.                       | [optional] |

### Return type

[**ChargebackListResponseDTO**](ChargebackListResponseDTO.md)

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

# **recuperar_um_unico_chargeback**

> PaymentChargebackResponseDTO recuperar_um_unico_chargeback(id)

Recuperar um único chargeback

Este endpoint recupera um chargeback específico a partir do ID de uma cobrança ou parcelamento.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_chargeback_response_dto import PaymentChargebackResponseDTO
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
    api_instance = asaas.ChargebackApi(api_client)
    id = 'pay_s02s330x4pox1x0y' # str | Identificador único do pagamento ou do parcelamento para o qual o chargeback será recuperado.

    try:
        # Recuperar um único chargeback
        api_response = api_instance.recuperar_um_unico_chargeback(id)
        print("The response of ChargebackApi->recuperar_um_unico_chargeback:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ChargebackApi->recuperar_um_unico_chargeback: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                                                                   | Notes |
| ------ | ------- | --------------------------------------------------------------------------------------------- | ----- |
| **id** | **str** | Identificador único do pagamento ou do parcelamento para o qual o chargeback será recuperado. |

### Return type

[**PaymentChargebackResponseDTO**](PaymentChargebackResponseDTO.md)

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
