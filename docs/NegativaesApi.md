# asaas.NegativaesApi

All URIs are relative to *https://api-sandbox.asaas.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelar_negativacao**](NegativaesApi.md#cancelar_negativacao) | **POST** /v3/paymentDunnings/{id}/cancel | Cancelar negativação
[**criar_uma_negativacao**](NegativaesApi.md#criar_uma_negativacao) | **POST** /v3/paymentDunnings | Criar uma negativação
[**listar_cobrancas_disponiveis_para_negativacao**](NegativaesApi.md#listar_cobrancas_disponiveis_para_negativacao) | **GET** /v3/paymentDunnings/paymentsAvailableForDunning | Listar cobranças disponíveis para negativação
[**listar_historico_de_eventos**](NegativaesApi.md#listar_historico_de_eventos) | **GET** /v3/paymentDunnings/{id}/history | Listar histórico de eventos
[**listar_negativacoes**](NegativaesApi.md#listar_negativacoes) | **GET** /v3/paymentDunnings | Listar negativações
[**listar_pagamentos_recebidos**](NegativaesApi.md#listar_pagamentos_recebidos) | **GET** /v3/paymentDunnings/{id}/partialPayments | Listar pagamentos recebidos
[**recuperar_uma_unica_negativacao**](NegativaesApi.md#recuperar_uma_unica_negativacao) | **GET** /v3/paymentDunnings/{id} | Recuperar uma única negativação
[**reenviar_documentos**](NegativaesApi.md#reenviar_documentos) | **POST** /v3/paymentDunnings/{id}/documents | Reenviar documentos
[**simular_uma_negativacao**](NegativaesApi.md#simular_uma_negativacao) | **POST** /v3/paymentDunnings/simulate | Simular uma negativação


# **cancelar_negativacao**
> PaymentDunningCancelResponseDTO cancelar_negativacao(id, body=body)

Cancelar negativação

Permite o cancelamento de uma negativação. Utilize a propriedade `canBeCancelled` retornado no objeto de negativação para verificar se a negativação pode ser cancelada.

Caso a negativação já tenha sido iniciada, ao solicitar o cancelamento a negativação ficará com o status de `AWAITING_CANCELLATION` até que seja efetivamente cancelada (`CANCELLED`).

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_cancel_response_dto import PaymentDunningCancelResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    id = 'ce35702d-0d9f-475a-ba46-e251ad265c91' # str | Identificador único da negativação a ser cancelada.
    body = None # object |  (optional)

    try:
        # Cancelar negativação
        api_response = api_instance.cancelar_negativacao(id, body=body)
        print("The response of NegativaesApi->cancelar_negativacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->cancelar_negativacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da negativação a ser cancelada. | 
 **body** | **object**|  | [optional] 

### Return type

[**PaymentDunningCancelResponseDTO**](PaymentDunningCancelResponseDTO.md)

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

# **criar_uma_negativacao**
> PaymentDunningShowResponseDTO criar_uma_negativacao(payment, type, customer_name, customer_cpf_cnpj, customer_primary_phone, customer_postal_code, customer_address, customer_address_number, customer_province, description=description, customer_secondary_phone=customer_secondary_phone, customer_complement=customer_complement, documents=documents)

Criar uma negativação



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_save_request_payment_dunning_type import PaymentDunningSaveRequestPaymentDunningType
from asaas.models.payment_dunning_show_response_dto import PaymentDunningShowResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    payment = 'payment_example' # str | Identificador único da cobrança a ser recuperada no Asaas
    type = asaas.PaymentDunningSaveRequestPaymentDunningType() # PaymentDunningSaveRequestPaymentDunningType | 
    customer_name = 'customer_name_example' # str | Nome do cliente
    customer_cpf_cnpj = 'customer_cpf_cnpj_example' # str | CPF ou CNPJ do cliente
    customer_primary_phone = 'customer_primary_phone_example' # str | Telefone principal do cliente
    customer_postal_code = 'customer_postal_code_example' # str | CEP do endereço do cliente
    customer_address = 'customer_address_example' # str | Logradouro do cliente
    customer_address_number = 'customer_address_number_example' # str | Número do endereço do cliente
    customer_province = 'customer_province_example' # str | Bairro do cliente
    description = 'description_example' # str | Descrição do produto ou serviço prestado (optional)
    customer_secondary_phone = 'customer_secondary_phone_example' # str | Telefone secundário do cliente (optional)
    customer_complement = 'customer_complement_example' # str | Complemento do endereço do cliente (optional)
    documents = None # bytes | Nota fiscal e/ou contrato com firma reconhecida em cartório (optional)

    try:
        # Criar uma negativação
        api_response = api_instance.criar_uma_negativacao(payment, type, customer_name, customer_cpf_cnpj, customer_primary_phone, customer_postal_code, customer_address, customer_address_number, customer_province, description=description, customer_secondary_phone=customer_secondary_phone, customer_complement=customer_complement, documents=documents)
        print("The response of NegativaesApi->criar_uma_negativacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->criar_uma_negativacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payment** | **str**| Identificador único da cobrança a ser recuperada no Asaas | 
 **type** | [**PaymentDunningSaveRequestPaymentDunningType**](PaymentDunningSaveRequestPaymentDunningType.md)|  | 
 **customer_name** | **str**| Nome do cliente | 
 **customer_cpf_cnpj** | **str**| CPF ou CNPJ do cliente | 
 **customer_primary_phone** | **str**| Telefone principal do cliente | 
 **customer_postal_code** | **str**| CEP do endereço do cliente | 
 **customer_address** | **str**| Logradouro do cliente | 
 **customer_address_number** | **str**| Número do endereço do cliente | 
 **customer_province** | **str**| Bairro do cliente | 
 **description** | **str**| Descrição do produto ou serviço prestado | [optional] 
 **customer_secondary_phone** | **str**| Telefone secundário do cliente | [optional] 
 **customer_complement** | **str**| Complemento do endereço do cliente | [optional] 
 **documents** | **bytes**| Nota fiscal e/ou contrato com firma reconhecida em cartório | [optional] 

### Return type

[**PaymentDunningShowResponseDTO**](PaymentDunningShowResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listar_cobrancas_disponiveis_para_negativacao**
> PaymentDunningPaymentsAvailableForDunningResponseDTO listar_cobrancas_disponiveis_para_negativacao(offset=offset, limit=limit)

Listar cobranças disponíveis para negativação

Retorna uma lista paginada de cobranças possíveis de negativação em conjunto com uma simulação de valores para cada tipo de negativação.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_payments_available_for_dunning_response_dto import PaymentDunningPaymentsAvailableForDunningResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (optional)

    try:
        # Listar cobranças disponíveis para negativação
        api_response = api_instance.listar_cobrancas_disponiveis_para_negativacao(offset=offset, limit=limit)
        print("The response of NegativaesApi->listar_cobrancas_disponiveis_para_negativacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->listar_cobrancas_disponiveis_para_negativacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista | [optional] 

### Return type

[**PaymentDunningPaymentsAvailableForDunningResponseDTO**](PaymentDunningPaymentsAvailableForDunningResponseDTO.md)

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

# **listar_historico_de_eventos**
> PaymentDunningListHistoryResponseDTO listar_historico_de_eventos(id, offset=offset, limit=limit)

Listar histórico de eventos

Retorna uma lista paginada com os eventos que ocorreram desde do início da negativação da cobrança.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_list_history_response_dto import PaymentDunningListHistoryResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    id = 'ce35702d-0d9f-475a-ba46-e251ad265c91' # str | Identificador único da negativação no Asaas
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (optional)

    try:
        # Listar histórico de eventos
        api_response = api_instance.listar_historico_de_eventos(id, offset=offset, limit=limit)
        print("The response of NegativaesApi->listar_historico_de_eventos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->listar_historico_de_eventos: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da negativação no Asaas | 
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista | [optional] 

### Return type

[**PaymentDunningListHistoryResponseDTO**](PaymentDunningListHistoryResponseDTO.md)

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

# **listar_negativacoes**
> PaymentDunningListResponseDTO listar_negativacoes(offset=offset, limit=limit, status=status, type=type, payment=payment, request_start_date=request_start_date, request_end_date=request_end_date)

Listar negativações



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_list_request_payment_dunning_status import PaymentDunningListRequestPaymentDunningStatus
from asaas.models.payment_dunning_list_request_payment_dunning_type import PaymentDunningListRequestPaymentDunningType
from asaas.models.payment_dunning_list_response_dto import PaymentDunningListResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    status = asaas.PaymentDunningListRequestPaymentDunningStatus() # PaymentDunningListRequestPaymentDunningStatus | Filtrar por status da negativação (optional)
    type = asaas.PaymentDunningListRequestPaymentDunningType() # PaymentDunningListRequestPaymentDunningType | Filtrar por tipo de negativação (optional)
    payment = 'payment_example' # str | Filtrar por negativações de uma determinada cobrança (optional)
    request_start_date = 'request_start_date_example' # str | Filtrar a partir da data de solicitação inicial (optional)
    request_end_date = 'request_end_date_example' # str | Filtrar a partir da data de solicitação final (optional)

    try:
        # Listar negativações
        api_response = api_instance.listar_negativacoes(offset=offset, limit=limit, status=status, type=type, payment=payment, request_start_date=request_start_date, request_end_date=request_end_date)
        print("The response of NegativaesApi->listar_negativacoes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->listar_negativacoes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista (max: 100) | [optional] 
 **status** | [**PaymentDunningListRequestPaymentDunningStatus**](.md)| Filtrar por status da negativação | [optional] 
 **type** | [**PaymentDunningListRequestPaymentDunningType**](.md)| Filtrar por tipo de negativação | [optional] 
 **payment** | **str**| Filtrar por negativações de uma determinada cobrança | [optional] 
 **request_start_date** | **str**| Filtrar a partir da data de solicitação inicial | [optional] 
 **request_end_date** | **str**| Filtrar a partir da data de solicitação final | [optional] 

### Return type

[**PaymentDunningListResponseDTO**](PaymentDunningListResponseDTO.md)

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

# **listar_pagamentos_recebidos**
> PaymentDunningListPartialPaymentsResponseDTO listar_pagamentos_recebidos(id, offset=offset, limit=limit)

Listar pagamentos recebidos

Retorna uma lista paginada com os pagamentos recebidos por meio da renegociação da dívida.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_list_partial_payments_response_dto import PaymentDunningListPartialPaymentsResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    id = 'ce35702d-0d9f-475a-ba46-e251ad265c91' # str | Identificador único da negativação no Asaas
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (optional)

    try:
        # Listar pagamentos recebidos
        api_response = api_instance.listar_pagamentos_recebidos(id, offset=offset, limit=limit)
        print("The response of NegativaesApi->listar_pagamentos_recebidos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->listar_pagamentos_recebidos: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da negativação no Asaas | 
 **offset** | **int**| Elemento inicial da lista | [optional] 
 **limit** | **int**| Número de elementos da lista | [optional] 

### Return type

[**PaymentDunningListPartialPaymentsResponseDTO**](PaymentDunningListPartialPaymentsResponseDTO.md)

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

# **recuperar_uma_unica_negativacao**
> PaymentDunningShowResponseDTO recuperar_uma_unica_negativacao(id)

Recuperar uma única negativação



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_show_response_dto import PaymentDunningShowResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    id = 'ce35702d-0d9f-475a-ba46-e251ad265c91' # str | Identificador único da negativação no Asaas

    try:
        # Recuperar uma única negativação
        api_response = api_instance.recuperar_uma_unica_negativacao(id)
        print("The response of NegativaesApi->recuperar_uma_unica_negativacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->recuperar_uma_unica_negativacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da negativação no Asaas | 

### Return type

[**PaymentDunningShowResponseDTO**](PaymentDunningShowResponseDTO.md)

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

# **reenviar_documentos**
> PaymentDunningSaveDocumentsResponseDTO reenviar_documentos(id, documents)

Reenviar documentos

Permite o reenvio dos documentos de uma negativação em caso de negação.

 Utilize a propriedade `isNecessaryResendDocumentation` retornado no objeto de negativação para verificar se é preciso o reenvio da documentação.

 Após o reenvio sua negativação retornará para o status de `AWAITING_APPROVAL`.

### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_save_documents_response_dto import PaymentDunningSaveDocumentsResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    id = 'ce35702d-0d9f-475a-ba46-e251ad265c91' # str | Identificador único da negativação no Asaas
    documents = None # bytes | Nota fiscal e/ou contrato com firma reconhecida em cartório

    try:
        # Reenviar documentos
        api_response = api_instance.reenviar_documentos(id, documents)
        print("The response of NegativaesApi->reenviar_documentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->reenviar_documentos: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Identificador único da negativação no Asaas | 
 **documents** | **bytes**| Nota fiscal e/ou contrato com firma reconhecida em cartório | 

### Return type

[**PaymentDunningSaveDocumentsResponseDTO**](PaymentDunningSaveDocumentsResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ok |  -  |
**401** | Unauthorized |  -  |
**404** | Not found |  -  |
**400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **simular_uma_negativacao**
> PaymentDunningSimulateResponseDTO simular_uma_negativacao(payment=payment, body=body)

Simular uma negativação



### Example

* Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_dunning_simulate_response_dto import PaymentDunningSimulateResponseDTO
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
    api_instance = asaas.NegativaesApi(api_client)
    payment = 'pay_080225913252' # str | Identificador único da cobrança a ser recuperada no Asaas (optional)
    body = None # object |  (optional)

    try:
        # Simular uma negativação
        api_response = api_instance.simular_uma_negativacao(payment=payment, body=body)
        print("The response of NegativaesApi->simular_uma_negativacao:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling NegativaesApi->simular_uma_negativacao: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payment** | **str**| Identificador único da cobrança a ser recuperada no Asaas | [optional] 
 **body** | **object**|  | [optional] 

### Return type

[**PaymentDunningSimulateResponseDTO**](PaymentDunningSimulateResponseDTO.md)

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

