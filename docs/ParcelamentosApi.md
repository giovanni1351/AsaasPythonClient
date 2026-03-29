# asaas.ParcelamentosApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                   | HTTP request                              | Description                                                  |
| -------------------------------------------------------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------ |
| [**atualizar_splits_do_parcelamento**](ParcelamentosApi.md#atualizar_splits_do_parcelamento)             | **PUT** /v3/installments/{id}/splits      | Atualizar splits do parcelamento                             |
| [**cancelar_cobrancas_de_um_parcelamento**](ParcelamentosApi.md#cancelar_cobrancas_de_um_parcelamento)   | **DELETE** /v3/installments/{id}/payments | Cancelar cobranças de um parcelamento (pendentes e vencidas) |
| [**criar_parcelamento**](ParcelamentosApi.md#criar_parcelamento)                                         | **POST** /v3/installments                 | Criar parcelamento                                           |
| [**criar_parcelamento_com_carto_de_crdito**](ParcelamentosApi.md#criar_parcelamento_com_carto_de_crdito) | **POST** /v3/installments/                | Criar parcelamento com cartão de crédito                     |
| [**estornar_parcelamento**](ParcelamentosApi.md#estornar_parcelamento)                                   | **POST** /v3/installments/{id}/refund     | Estornar parcelamento                                        |
| [**gerar_carne_de_parcelamento**](ParcelamentosApi.md#gerar_carne_de_parcelamento)                       | **GET** /v3/installments/{id}/paymentBook | Gerar carnê de parcelamento                                  |
| [**listar_cobranas_de_um_parcelamento**](ParcelamentosApi.md#listar_cobranas_de_um_parcelamento)         | **GET** /v3/installments/{id}/payments    | Listar cobranças de um parcelamento                          |
| [**listar_parcelamentos**](ParcelamentosApi.md#listar_parcelamentos)                                     | **GET** /v3/installments                  | Listar parcelamentos                                         |
| [**recuperar_um_unico_parcelamento**](ParcelamentosApi.md#recuperar_um_unico_parcelamento)               | **GET** /v3/installments/{id}             | Recuperar um único parcelamento                              |
| [**remover_parcelamento**](ParcelamentosApi.md#remover_parcelamento)                                     | **DELETE** /v3/installments/{id}          | Remover parcelamento                                         |

# **atualizar_splits_do_parcelamento**

> InstallmentUpdateSplitResponseDTO atualizar_splits_do_parcelamento(id, installment_update_split_request_dto=installment_update_split_request_dto)

Atualizar splits do parcelamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_update_split_request_dto import InstallmentUpdateSplitRequestDTO
from asaas.models.installment_update_split_response_dto import InstallmentUpdateSplitResponseDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '2765d086-c7c5-5cca-898a-4262d212587c' # str | ID do parcelamento
    installment_update_split_request_dto = asaas.InstallmentUpdateSplitRequestDTO() # InstallmentUpdateSplitRequestDTO |  (optional)

    try:
        # Atualizar splits do parcelamento
        api_response = api_instance.atualizar_splits_do_parcelamento(id, installment_update_split_request_dto=installment_update_split_request_dto)
        print("The response of ParcelamentosApi->atualizar_splits_do_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->atualizar_splits_do_parcelamento: %s\n" % e)
```

### Parameters

| Name                                     | Type                                                                        | Description        | Notes      |
| ---------------------------------------- | --------------------------------------------------------------------------- | ------------------ | ---------- |
| **id**                                   | **str**                                                                     | ID do parcelamento |
| **installment_update_split_request_dto** | [**InstallmentUpdateSplitRequestDTO**](InstallmentUpdateSplitRequestDTO.md) |                    | [optional] |

### Return type

[**InstallmentUpdateSplitResponseDTO**](InstallmentUpdateSplitResponseDTO.md)

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

# **cancelar_cobrancas_de_um_parcelamento**

> InstallmentDeletePaymentsResponseDTO cancelar_cobrancas_de_um_parcelamento(id)

Cancelar cobranças de um parcelamento (pendentes e vencidas)

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_delete_payments_response_dto import InstallmentDeletePaymentsResponseDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '5a2c890b-dd63-4b5a-9169-96c8d7828f4c' # str | Identificador único do parcelamento que terá cobranças removidas.

    try:
        # Cancelar cobranças de um parcelamento (pendentes e vencidas)
        api_response = api_instance.cancelar_cobrancas_de_um_parcelamento(id)
        print("The response of ParcelamentosApi->cancelar_cobrancas_de_um_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->cancelar_cobrancas_de_um_parcelamento: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                                       | Notes |
| ------ | ------- | ----------------------------------------------------------------- | ----- |
| **id** | **str** | Identificador único do parcelamento que terá cobranças removidas. |

### Return type

[**InstallmentDeletePaymentsResponseDTO**](InstallmentDeletePaymentsResponseDTO.md)

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

# **criar_parcelamento**

> InstallmentGetResponseDTO criar_parcelamento(installment_save_request_dto=installment_save_request_dto)

Criar parcelamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_get_response_dto import InstallmentGetResponseDTO
from asaas.models.installment_save_request_dto import InstallmentSaveRequestDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    installment_save_request_dto = asaas.InstallmentSaveRequestDTO() # InstallmentSaveRequestDTO |  (optional)

    try:
        # Criar parcelamento
        api_response = api_instance.criar_parcelamento(installment_save_request_dto=installment_save_request_dto)
        print("The response of ParcelamentosApi->criar_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->criar_parcelamento: %s\n" % e)
```

### Parameters

| Name                             | Type                                                          | Description | Notes      |
| -------------------------------- | ------------------------------------------------------------- | ----------- | ---------- |
| **installment_save_request_dto** | [**InstallmentSaveRequestDTO**](InstallmentSaveRequestDTO.md) |             | [optional] |

### Return type

[**InstallmentGetResponseDTO**](InstallmentGetResponseDTO.md)

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

# **criar_parcelamento_com_carto_de_crdito**

> InstallmentGetResponseDTO criar_parcelamento_com_carto_de_crdito(installment_save_with_credit_card_request_dto=installment_save_with_credit_card_request_dto)

Criar parcelamento com cartão de crédito

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_get_response_dto import InstallmentGetResponseDTO
from asaas.models.installment_save_with_credit_card_request_dto import InstallmentSaveWithCreditCardRequestDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    installment_save_with_credit_card_request_dto = asaas.InstallmentSaveWithCreditCardRequestDTO() # InstallmentSaveWithCreditCardRequestDTO |  (optional)

    try:
        # Criar parcelamento com cartão de crédito
        api_response = api_instance.criar_parcelamento_com_carto_de_crdito(installment_save_with_credit_card_request_dto=installment_save_with_credit_card_request_dto)
        print("The response of ParcelamentosApi->criar_parcelamento_com_carto_de_crdito:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->criar_parcelamento_com_carto_de_crdito: %s\n" % e)
```

### Parameters

| Name                                              | Type                                                                                      | Description | Notes      |
| ------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------- | ---------- |
| **installment_save_with_credit_card_request_dto** | [**InstallmentSaveWithCreditCardRequestDTO**](InstallmentSaveWithCreditCardRequestDTO.md) |             | [optional] |

### Return type

[**InstallmentGetResponseDTO**](InstallmentGetResponseDTO.md)

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

# **estornar_parcelamento**

> InstallmentGetResponseDTO estornar_parcelamento(id, installment_refund_request_dto=installment_refund_request_dto)

Estornar parcelamento

É possível estornar um parcelamento via cartão de crédito recebido ou confirmado.

Como já ocorre no processo de estorno de uma cobrança avulsa por cartão de crédito, o saldo correspondente do parcelamento é debitado de sua conta no Asaas e a cobrança é cancelada no cartão do seu cliente. O cancelamento pode levar até 10 dias úteis para aparecer na fatura de seu cliente.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_get_response_dto import InstallmentGetResponseDTO
from asaas.models.installment_refund_request_dto import InstallmentRefundRequestDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '2765d086-c7c5-5cca-898a-4262d212587c' # str | Identificador único do parcelamento a ser estornado.
    installment_refund_request_dto = asaas.InstallmentRefundRequestDTO() # InstallmentRefundRequestDTO |  (optional)

    try:
        # Estornar parcelamento
        api_response = api_instance.estornar_parcelamento(id, installment_refund_request_dto=installment_refund_request_dto)
        print("The response of ParcelamentosApi->estornar_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->estornar_parcelamento: %s\n" % e)
```

### Parameters

| Name                               | Type                                                              | Description                                          | Notes      |
| ---------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------- | ---------- |
| **id**                             | **str**                                                           | Identificador único do parcelamento a ser estornado. |
| **installment_refund_request_dto** | [**InstallmentRefundRequestDTO**](InstallmentRefundRequestDTO.md) |                                                      | [optional] |

### Return type

[**InstallmentGetResponseDTO**](InstallmentGetResponseDTO.md)

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

# **gerar_carne_de_parcelamento**

> bytes gerar_carne_de_parcelamento(id, sort=sort, order=order)

Gerar carnê de parcelamento

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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '2765d086-c7c5-5cca-898a-4262d212587c' # str | Identificador único do parcelamento no Asaas
    sort = 'sort_example' # str | Filtrar pelo nome da coluna (optional)
    order = 'asc' # str | Ordenação da coluna (optional)

    try:
        # Gerar carnê de parcelamento
        api_response = api_instance.gerar_carne_de_parcelamento(id, sort=sort, order=order)
        print("The response of ParcelamentosApi->gerar_carne_de_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->gerar_carne_de_parcelamento: %s\n" % e)
```

### Parameters

| Name      | Type    | Description                                  | Notes      |
| --------- | ------- | -------------------------------------------- | ---------- |
| **id**    | **str** | Identificador único do parcelamento no Asaas |
| **sort**  | **str** | Filtrar pelo nome da coluna                  | [optional] |
| **order** | **str** | Ordenação da coluna                          | [optional] |

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

# **listar_cobranas_de_um_parcelamento**

> PaymentListResponseDTO listar_cobranas_de_um_parcelamento(id, status=status)

Listar cobranças de um parcelamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_list_payments_request_payment_status import InstallmentListPaymentsRequestPaymentStatus
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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '2765d086-c7c5-5cca-898a-4262d212587c' # str | Identificador único do parcelamento no Asaas
    status = asaas.InstallmentListPaymentsRequestPaymentStatus() # InstallmentListPaymentsRequestPaymentStatus | Filtrar por status das cobranças (optional)

    try:
        # Listar cobranças de um parcelamento
        api_response = api_instance.listar_cobranas_de_um_parcelamento(id, status=status)
        print("The response of ParcelamentosApi->listar_cobranas_de_um_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->listar_cobranas_de_um_parcelamento: %s\n" % e)
```

### Parameters

| Name       | Type                                                   | Description                                  | Notes      |
| ---------- | ------------------------------------------------------ | -------------------------------------------- | ---------- |
| **id**     | **str**                                                | Identificador único do parcelamento no Asaas |
| **status** | [**InstallmentListPaymentsRequestPaymentStatus**](.md) | Filtrar por status das cobranças             | [optional] |

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

# **listar_parcelamentos**

> InstallmentListResponseDTO listar_parcelamentos(offset=offset, limit=limit)

Listar parcelamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_list_response_dto import InstallmentListResponseDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)

    try:
        # Listar parcelamentos
        api_response = api_instance.listar_parcelamentos(offset=offset, limit=limit)
        print("The response of ParcelamentosApi->listar_parcelamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->listar_parcelamentos: %s\n" % e)
```

### Parameters

| Name       | Type    | Description                             | Notes      |
| ---------- | ------- | --------------------------------------- | ---------- |
| **offset** | **int** | Elemento inicial da lista               | [optional] |
| **limit**  | **int** | Número de elementos da lista (max: 100) | [optional] |

### Return type

[**InstallmentListResponseDTO**](InstallmentListResponseDTO.md)

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

# **recuperar_um_unico_parcelamento**

> InstallmentGetResponseDTO recuperar_um_unico_parcelamento(id)

Recuperar um único parcelamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_get_response_dto import InstallmentGetResponseDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '2765d086-c7c5-5cca-898a-4262d212587c' # str | Identificador único do parcelamento no Asaas

    try:
        # Recuperar um único parcelamento
        api_response = api_instance.recuperar_um_unico_parcelamento(id)
        print("The response of ParcelamentosApi->recuperar_um_unico_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->recuperar_um_unico_parcelamento: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                  | Notes |
| ------ | ------- | -------------------------------------------- | ----- |
| **id** | **str** | Identificador único do parcelamento no Asaas |

### Return type

[**InstallmentGetResponseDTO**](InstallmentGetResponseDTO.md)

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

# **remover_parcelamento**

> InstallmentDeleteResponseDTO remover_parcelamento(id)

Remover parcelamento

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.installment_delete_response_dto import InstallmentDeleteResponseDTO
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
    api_instance = asaas.ParcelamentosApi(api_client)
    id = '5a2c890b-dd63-4b5a-9169-96c8d7828f4c' # str | Identificador único do parcelamento a ser removido.

    try:
        # Remover parcelamento
        api_response = api_instance.remover_parcelamento(id)
        print("The response of ParcelamentosApi->remover_parcelamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ParcelamentosApi->remover_parcelamento: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                         | Notes |
| ------ | ------- | --------------------------------------------------- | ----- |
| **id** | **str** | Identificador único do parcelamento a ser removido. |

### Return type

[**InstallmentDeleteResponseDTO**](InstallmentDeleteResponseDTO.md)

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
