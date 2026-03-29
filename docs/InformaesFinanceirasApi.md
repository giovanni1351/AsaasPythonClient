# asaas.InformaesFinanceirasApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                  | HTTP request                           | Description                |
| --------------------------------------------------------------------------------------- | -------------------------------------- | -------------------------- |
| [**estatisticas_de_cobrancas**](InformaesFinanceirasApi.md#estatisticas_de_cobrancas)   | **GET** /v3/finance/payment/statistics | Estatísticas de cobranças  |
| [**recuperar_saldo_da_conta**](InformaesFinanceirasApi.md#recuperar_saldo_da_conta)     | **GET** /v3/finance/balance            | Recuperar saldo da conta   |
| [**recuperar_valores_de_split**](InformaesFinanceirasApi.md#recuperar_valores_de_split) | **GET** /v3/finance/split/statistics   | Recuperar valores de split |

# **estatisticas_de_cobrancas**

> FinanceGetPaymentStatisticsResponseDTO estatisticas_de_cobrancas(customer=customer, billing_type=billing_type, status=status, anticipated=anticipated, date_created_ge=date_created_ge, date_created_le=date_created_le, due_date_ge=due_date_ge, due_date_le=due_date_le, estimated_credit_date_ge=estimated_credit_date_ge, estimated_credit_date_le=estimated_credit_date_le, external_reference=external_reference)

Estatísticas de cobranças

Retorna valores totais das cobranças da sua conta Asaas de acordo com os filtros informados.

### Exemplos de filtros:

Valor total a receber: `GET https://api.asaas.com/v3/finance/payment/statistics?status=PENDING`

Valor total a receber com cobranças por boleto bancário: `GET https://api.asaas.com/v3/finance/payment/statistics?billingType=BOLETO&status=PENDING`

Valor total recebido por cobranças por cartão de crédito: `GET https://api.asaas.com/v3/finance/payment/statistics?billingType=CREDIT_CARD&status=RECEIVED`

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.finance_get_payment_statistics_request_billing_type import FinanceGetPaymentStatisticsRequestBillingType
from asaas.models.finance_get_payment_statistics_request_payment_status import FinanceGetPaymentStatisticsRequestPaymentStatus
from asaas.models.finance_get_payment_statistics_response_dto import FinanceGetPaymentStatisticsResponseDTO
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
    api_instance = asaas.InformaesFinanceirasApi(api_client)
    customer = 'cus_3EZfkUThUMAt' # str | Filtrar pelo identificador único do cliente (optional)
    billing_type = asaas.FinanceGetPaymentStatisticsRequestBillingType() # FinanceGetPaymentStatisticsRequestBillingType | Filtrar por forma de pagamento (optional)
    status = asaas.FinanceGetPaymentStatisticsRequestPaymentStatus() # FinanceGetPaymentStatisticsRequestPaymentStatus | Filtrar por status (optional)
    anticipated = false # bool | Filtrar registros antecipados ou não (optional)
    date_created_ge = '2023-01-01' # str | Filtrar a partir da data de criação inicial (optional)
    date_created_le = '2023-01-01' # str | Filtrar a partir da data de criação final (optional)
    due_date_ge = '2023-01-01' # str | Filtrar a partir da data de vencimento inicial (optional)
    due_date_le = '2023-01-01' # str | Filtrar a partir da data de vencimento final (optional)
    estimated_credit_date_ge = '2023-01-01' # str | Filtrar a partir da data estimada de crédito inicial (optional)
    estimated_credit_date_le = '2023-01-01' # str | Filtrar a partir da data estimada de crédito final (optional)
    external_reference = '056984' # str | Filtrar pelo identificador do seu sistema (optional)

    try:
        # Estatísticas de cobranças
        api_response = api_instance.estatisticas_de_cobrancas(customer=customer, billing_type=billing_type, status=status, anticipated=anticipated, date_created_ge=date_created_ge, date_created_le=date_created_le, due_date_ge=due_date_ge, due_date_le=due_date_le, estimated_credit_date_ge=estimated_credit_date_ge, estimated_credit_date_le=estimated_credit_date_le, external_reference=external_reference)
        print("The response of InformaesFinanceirasApi->estatisticas_de_cobrancas:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFinanceirasApi->estatisticas_de_cobrancas: %s\n" % e)
```

### Parameters

| Name                         | Type                                                       | Description                                          | Notes      |
| ---------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ---------- |
| **customer**                 | **str**                                                    | Filtrar pelo identificador único do cliente          | [optional] |
| **billing_type**             | [**FinanceGetPaymentStatisticsRequestBillingType**](.md)   | Filtrar por forma de pagamento                       | [optional] |
| **status**                   | [**FinanceGetPaymentStatisticsRequestPaymentStatus**](.md) | Filtrar por status                                   | [optional] |
| **anticipated**              | **bool**                                                   | Filtrar registros antecipados ou não                 | [optional] |
| **date_created_ge**          | **str**                                                    | Filtrar a partir da data de criação inicial          | [optional] |
| **date_created_le**          | **str**                                                    | Filtrar a partir da data de criação final            | [optional] |
| **due_date_ge**              | **str**                                                    | Filtrar a partir da data de vencimento inicial       | [optional] |
| **due_date_le**              | **str**                                                    | Filtrar a partir da data de vencimento final         | [optional] |
| **estimated_credit_date_ge** | **str**                                                    | Filtrar a partir da data estimada de crédito inicial | [optional] |
| **estimated_credit_date_le** | **str**                                                    | Filtrar a partir da data estimada de crédito final   | [optional] |
| **external_reference**       | **str**                                                    | Filtrar pelo identificador do seu sistema            | [optional] |

### Return type

[**FinanceGetPaymentStatisticsResponseDTO**](FinanceGetPaymentStatisticsResponseDTO.md)

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

# **recuperar_saldo_da_conta**

> FinanceBalanceResponseDTO recuperar_saldo_da_conta()

Recuperar saldo da conta

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.finance_balance_response_dto import FinanceBalanceResponseDTO
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
    api_instance = asaas.InformaesFinanceirasApi(api_client)

    try:
        # Recuperar saldo da conta
        api_response = api_instance.recuperar_saldo_da_conta()
        print("The response of InformaesFinanceirasApi->recuperar_saldo_da_conta:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFinanceirasApi->recuperar_saldo_da_conta: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**FinanceBalanceResponseDTO**](FinanceBalanceResponseDTO.md)

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

# **recuperar_valores_de_split**

> FinanceGetSplitStatisticsResponseDTO recuperar_valores_de_split()

Recuperar valores de split

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.finance_get_split_statistics_response_dto import FinanceGetSplitStatisticsResponseDTO
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
    api_instance = asaas.InformaesFinanceirasApi(api_client)

    try:
        # Recuperar valores de split
        api_response = api_instance.recuperar_valores_de_split()
        print("The response of InformaesFinanceirasApi->recuperar_valores_de_split:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFinanceirasApi->recuperar_valores_de_split: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**FinanceGetSplitStatisticsResponseDTO**](FinanceGetSplitStatisticsResponseDTO.md)

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
