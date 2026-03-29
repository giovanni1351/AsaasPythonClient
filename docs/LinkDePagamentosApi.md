# asaas.LinkDePagamentosApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                          | HTTP request                                                        | Description                                      |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------ |
| [**adicionar_uma_imagem_aum_link_de_pagamentos**](LinkDePagamentosApi.md#adicionar_uma_imagem_aum_link_de_pagamentos)           | **POST** /v3/paymentLinks/{id}/images                               | Adicionar uma imagem a um link de pagamentos     |
| [**atualizar_um_link_de_pagamentos**](LinkDePagamentosApi.md#atualizar_um_link_de_pagamentos)                                   | **PUT** /v3/paymentLinks/{id}                                       | Atualizar um link de pagamentos                  |
| [**criar_um_link_de_pagamentos**](LinkDePagamentosApi.md#criar_um_link_de_pagamentos)                                           | **POST** /v3/paymentLinks                                           | Criar um link de pagamentos                      |
| [**definir_imagem_principal_do_link_de_pagamentos**](LinkDePagamentosApi.md#definir_imagem_principal_do_link_de_pagamentos)     | **PUT** /v3/paymentLinks/{paymentLinkId}/images/{imageId}/setAsMain | Definir imagem principal do link de pagamentos   |
| [**listar_imagens_de_um_link_de_pagamentos**](LinkDePagamentosApi.md#listar_imagens_de_um_link_de_pagamentos)                   | **GET** /v3/paymentLinks/{id}/images                                | Listar imagens de um link de pagamentos          |
| [**listar_links_de_pagamentos**](LinkDePagamentosApi.md#listar_links_de_pagamentos)                                             | **GET** /v3/paymentLinks                                            | Listar links de pagamentos                       |
| [**recuperar_um_unico_link_de_pagamentos**](LinkDePagamentosApi.md#recuperar_um_unico_link_de_pagamentos)                       | **GET** /v3/paymentLinks/{id}                                       | Recuperar um único link de pagamentos            |
| [**recuperar_uma_unica_imagem_do_link_de_pagamentos**](LinkDePagamentosApi.md#recuperar_uma_unica_imagem_do_link_de_pagamentos) | **GET** /v3/paymentLinks/{paymentLinkId}/images/{imageId}           | Recuperar uma única imagem do link de pagamentos |
| [**remover_um_link_de_pagamentos**](LinkDePagamentosApi.md#remover_um_link_de_pagamentos)                                       | **DELETE** /v3/paymentLinks/{id}                                    | Remover um link de pagamentos                    |
| [**remover_uma_imagem_do_link_de_pagamentos**](LinkDePagamentosApi.md#remover_uma_imagem_do_link_de_pagamentos)                 | **DELETE** /v3/paymentLinks/{paymentLinkId}/images/{imageId}        | Remover uma imagem do link de pagamentos         |
| [**restaurar_um_link_de_pagamentos**](LinkDePagamentosApi.md#restaurar_um_link_de_pagamentos)                                   | **POST** /v3/paymentLinks/{id}/restore                              | Restaurar um link de pagamentos                  |

# **adicionar_uma_imagem_aum_link_de_pagamentos**

> PaymentLinkFileGetResponseDTO adicionar_uma_imagem_aum_link_de_pagamentos(id, main=main, image=image)

Adicionar uma imagem a um link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_file_get_response_dto import PaymentLinkFileGetResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas
    main = True # bool | true para definir como a imagem principal (optional)
    image = None # bytes | Arquivo (optional)

    try:
        # Adicionar uma imagem a um link de pagamentos
        api_response = api_instance.adicionar_uma_imagem_aum_link_de_pagamentos(id, main=main, image=image)
        print("The response of LinkDePagamentosApi->adicionar_uma_imagem_aum_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->adicionar_uma_imagem_aum_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name      | Type      | Description                                            | Notes      |
| --------- | --------- | ------------------------------------------------------ | ---------- |
| **id**    | **str**   | Identificador único do seu link de pagamentos no Asaas |
| **main**  | **bool**  | true para definir como a imagem principal              | [optional] |
| **image** | **bytes** | Arquivo                                                | [optional] |

### Return type

[**PaymentLinkFileGetResponseDTO**](PaymentLinkFileGetResponseDTO.md)

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

# **atualizar_um_link_de_pagamentos**

> PaymentLinkGetResponseDTO atualizar_um_link_de_pagamentos(id, payment_link_update_request_dto=payment_link_update_request_dto)

Atualizar um link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_get_response_dto import PaymentLinkGetResponseDTO
from asaas.models.payment_link_update_request_dto import PaymentLinkUpdateRequestDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas
    payment_link_update_request_dto = asaas.PaymentLinkUpdateRequestDTO() # PaymentLinkUpdateRequestDTO |  (optional)

    try:
        # Atualizar um link de pagamentos
        api_response = api_instance.atualizar_um_link_de_pagamentos(id, payment_link_update_request_dto=payment_link_update_request_dto)
        print("The response of LinkDePagamentosApi->atualizar_um_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->atualizar_um_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name                                | Type                                                              | Description                                            | Notes      |
| ----------------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------ | ---------- |
| **id**                              | **str**                                                           | Identificador único do seu link de pagamentos no Asaas |
| **payment_link_update_request_dto** | [**PaymentLinkUpdateRequestDTO**](PaymentLinkUpdateRequestDTO.md) |                                                        | [optional] |

### Return type

[**PaymentLinkGetResponseDTO**](PaymentLinkGetResponseDTO.md)

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

# **criar_um_link_de_pagamentos**

> PaymentLinkGetResponseDTO criar_um_link_de_pagamentos(payment_link_save_request_dto=payment_link_save_request_dto)

Criar um link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_get_response_dto import PaymentLinkGetResponseDTO
from asaas.models.payment_link_save_request_dto import PaymentLinkSaveRequestDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    payment_link_save_request_dto = asaas.PaymentLinkSaveRequestDTO() # PaymentLinkSaveRequestDTO |  (optional)

    try:
        # Criar um link de pagamentos
        api_response = api_instance.criar_um_link_de_pagamentos(payment_link_save_request_dto=payment_link_save_request_dto)
        print("The response of LinkDePagamentosApi->criar_um_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->criar_um_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name                              | Type                                                          | Description | Notes      |
| --------------------------------- | ------------------------------------------------------------- | ----------- | ---------- |
| **payment_link_save_request_dto** | [**PaymentLinkSaveRequestDTO**](PaymentLinkSaveRequestDTO.md) |             | [optional] |

### Return type

[**PaymentLinkGetResponseDTO**](PaymentLinkGetResponseDTO.md)

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

# **definir_imagem_principal_do_link_de_pagamentos**

> PaymentLinkFileGetResponseDTO definir_imagem_principal_do_link_de_pagamentos(payment_link_id, image_id, body=body)

Definir imagem principal do link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_file_get_response_dto import PaymentLinkFileGetResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    payment_link_id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas
    image_id = '417d1fe7-f530-4368-935f-699045f2bf5d' # str | Identificador único da imagem do seu link de pagamentos no Asaas
    body = None # object |  (optional)

    try:
        # Definir imagem principal do link de pagamentos
        api_response = api_instance.definir_imagem_principal_do_link_de_pagamentos(payment_link_id, image_id, body=body)
        print("The response of LinkDePagamentosApi->definir_imagem_principal_do_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->definir_imagem_principal_do_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name                | Type       | Description                                                      | Notes      |
| ------------------- | ---------- | ---------------------------------------------------------------- | ---------- |
| **payment_link_id** | **str**    | Identificador único do seu link de pagamentos no Asaas           |
| **image_id**        | **str**    | Identificador único da imagem do seu link de pagamentos no Asaas |
| **body**            | **object** |                                                                  | [optional] |

### Return type

[**PaymentLinkFileGetResponseDTO**](PaymentLinkFileGetResponseDTO.md)

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

# **listar_imagens_de_um_link_de_pagamentos**

> PaymentLinkFileListResponseDTO listar_imagens_de_um_link_de_pagamentos(id)

Listar imagens de um link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_file_list_response_dto import PaymentLinkFileListResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas

    try:
        # Listar imagens de um link de pagamentos
        api_response = api_instance.listar_imagens_de_um_link_de_pagamentos(id)
        print("The response of LinkDePagamentosApi->listar_imagens_de_um_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->listar_imagens_de_um_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                            | Notes |
| ------ | ------- | ------------------------------------------------------ | ----- |
| **id** | **str** | Identificador único do seu link de pagamentos no Asaas |

### Return type

[**PaymentLinkFileListResponseDTO**](PaymentLinkFileListResponseDTO.md)

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

# **listar_links_de_pagamentos**

> PaymentLinkListResponseDTO listar_links_de_pagamentos(offset=offset, limit=limit, active=active, include_deleted=include_deleted, name=name, external_reference=external_reference)

Listar links de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_list_response_dto import PaymentLinkListResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    active = True # bool | Filtrar por links de pagamentos ativados ou desativados (optional)
    include_deleted = True # bool | True para recuperar também os links de pagamentos removidos (optional)
    name = 'name_example' # str | Filtrar pelo nome do link de pagamentos (optional)
    external_reference = 'external_reference_example' # str | Filtrar pelo Identificador do seu sistema (optional)

    try:
        # Listar links de pagamentos
        api_response = api_instance.listar_links_de_pagamentos(offset=offset, limit=limit, active=active, include_deleted=include_deleted, name=name, external_reference=external_reference)
        print("The response of LinkDePagamentosApi->listar_links_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->listar_links_de_pagamentos: %s\n" % e)
```

### Parameters

| Name                   | Type     | Description                                                 | Notes      |
| ---------------------- | -------- | ----------------------------------------------------------- | ---------- |
| **offset**             | **int**  | Elemento inicial da lista                                   | [optional] |
| **limit**              | **int**  | Número de elementos da lista (max: 100)                     | [optional] |
| **active**             | **bool** | Filtrar por links de pagamentos ativados ou desativados     | [optional] |
| **include_deleted**    | **bool** | True para recuperar também os links de pagamentos removidos | [optional] |
| **name**               | **str**  | Filtrar pelo nome do link de pagamentos                     | [optional] |
| **external_reference** | **str**  | Filtrar pelo Identificador do seu sistema                   | [optional] |

### Return type

[**PaymentLinkListResponseDTO**](PaymentLinkListResponseDTO.md)

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

# **recuperar_um_unico_link_de_pagamentos**

> PaymentLinkGetResponseDTO recuperar_um_unico_link_de_pagamentos(id)

Recuperar um único link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_get_response_dto import PaymentLinkGetResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas

    try:
        # Recuperar um único link de pagamentos
        api_response = api_instance.recuperar_um_unico_link_de_pagamentos(id)
        print("The response of LinkDePagamentosApi->recuperar_um_unico_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->recuperar_um_unico_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                            | Notes |
| ------ | ------- | ------------------------------------------------------ | ----- |
| **id** | **str** | Identificador único do seu link de pagamentos no Asaas |

### Return type

[**PaymentLinkGetResponseDTO**](PaymentLinkGetResponseDTO.md)

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

# **recuperar_uma_unica_imagem_do_link_de_pagamentos**

> PaymentLinkFileGetResponseDTO recuperar_uma_unica_imagem_do_link_de_pagamentos(payment_link_id, image_id)

Recuperar uma única imagem do link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_file_get_response_dto import PaymentLinkFileGetResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    payment_link_id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas
    image_id = '417d1fe7-f530-4368-935f-699045f2bf5d' # str | Identificador único da imagem do seu link de pagamentos no Asaas

    try:
        # Recuperar uma única imagem do link de pagamentos
        api_response = api_instance.recuperar_uma_unica_imagem_do_link_de_pagamentos(payment_link_id, image_id)
        print("The response of LinkDePagamentosApi->recuperar_uma_unica_imagem_do_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->recuperar_uma_unica_imagem_do_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name                | Type    | Description                                                      | Notes |
| ------------------- | ------- | ---------------------------------------------------------------- | ----- |
| **payment_link_id** | **str** | Identificador único do seu link de pagamentos no Asaas           |
| **image_id**        | **str** | Identificador único da imagem do seu link de pagamentos no Asaas |

### Return type

[**PaymentLinkFileGetResponseDTO**](PaymentLinkFileGetResponseDTO.md)

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

# **remover_um_link_de_pagamentos**

> PaymentLinkDeleteResponseDTO remover_um_link_de_pagamentos(id)

Remover um link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_delete_response_dto import PaymentLinkDeleteResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas

    try:
        # Remover um link de pagamentos
        api_response = api_instance.remover_um_link_de_pagamentos(id)
        print("The response of LinkDePagamentosApi->remover_um_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->remover_um_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name   | Type    | Description                                            | Notes |
| ------ | ------- | ------------------------------------------------------ | ----- |
| **id** | **str** | Identificador único do seu link de pagamentos no Asaas |

### Return type

[**PaymentLinkDeleteResponseDTO**](PaymentLinkDeleteResponseDTO.md)

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

# **remover_uma_imagem_do_link_de_pagamentos**

> PaymentLinkFileDeleteResponseDTO remover_uma_imagem_do_link_de_pagamentos(payment_link_id, image_id)

Remover uma imagem do link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_file_delete_response_dto import PaymentLinkFileDeleteResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    payment_link_id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas
    image_id = '417d1fe7-f530-4368-935f-699045f2bf5d' # str | Identificador único da imagem do seu link de pagamentos no Asaas

    try:
        # Remover uma imagem do link de pagamentos
        api_response = api_instance.remover_uma_imagem_do_link_de_pagamentos(payment_link_id, image_id)
        print("The response of LinkDePagamentosApi->remover_uma_imagem_do_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->remover_uma_imagem_do_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name                | Type    | Description                                                      | Notes |
| ------------------- | ------- | ---------------------------------------------------------------- | ----- |
| **payment_link_id** | **str** | Identificador único do seu link de pagamentos no Asaas           |
| **image_id**        | **str** | Identificador único da imagem do seu link de pagamentos no Asaas |

### Return type

[**PaymentLinkFileDeleteResponseDTO**](PaymentLinkFileDeleteResponseDTO.md)

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

# **restaurar_um_link_de_pagamentos**

> PaymentLinkGetResponseDTO restaurar_um_link_de_pagamentos(id, body=body)

Restaurar um link de pagamentos

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.payment_link_get_response_dto import PaymentLinkGetResponseDTO
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
    api_instance = asaas.LinkDePagamentosApi(api_client)
    id = '725104409743' # str | Identificador único do seu link de pagamentos no Asaas
    body = None # object |  (optional)

    try:
        # Restaurar um link de pagamentos
        api_response = api_instance.restaurar_um_link_de_pagamentos(id, body=body)
        print("The response of LinkDePagamentosApi->restaurar_um_link_de_pagamentos:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling LinkDePagamentosApi->restaurar_um_link_de_pagamentos: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                                            | Notes      |
| -------- | ---------- | ------------------------------------------------------ | ---------- |
| **id**   | **str**    | Identificador único do seu link de pagamentos no Asaas |
| **body** | **object** |                                                        | [optional] |

### Return type

[**PaymentLinkGetResponseDTO**](PaymentLinkGetResponseDTO.md)

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
