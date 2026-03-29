# asaas.AesEmSandboxApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                            | HTTP request                              | Description                                          |
| ----------------------------------------------------------------- | ----------------------------------------- | ---------------------------------------------------- |
| [**confirmar_pagamento**](AesEmSandboxApi.md#confirmar_pagamento) | **POST** /v3/sandbox/payment/{id}/confirm | (Apenas sandbox) Confirmar o pagamento               |
| [**forcar_vencimento**](AesEmSandboxApi.md#forcar_vencimento)     | **POST** /v3/sandbox/payment/{id}/overdue | (Apenas sandbox) Forçar o vencimento de uma cobrança |

# **confirmar_pagamento**

> PaymentGetResponseDTO confirmar_pagamento(id, body=body)

(Apenas sandbox) Confirmar o pagamento

Esse endpoint confirma o pagamento de uma cobrança no ambiente sandbox.

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
    api_instance = asaas.AesEmSandboxApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # (Apenas sandbox) Confirmar o pagamento
        api_response = api_instance.confirmar_pagamento(id, body=body)
        print("The response of AesEmSandboxApi->confirmar_pagamento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AesEmSandboxApi->confirmar_pagamento: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **forcar_vencimento**

> PaymentGetResponseDTO forcar_vencimento(id, body=body)

(Apenas sandbox) Forçar o vencimento de uma cobrança

Esse endpoint força o vencimento de uma cobrança no ambiente sandbox.

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
    api_instance = asaas.AesEmSandboxApi(api_client)
    id = 'id_example' # str | Identificador único da cobrança no Asaas
    body = None # object |  (optional)

    try:
        # (Apenas sandbox) Forçar o vencimento de uma cobrança
        api_response = api_instance.forcar_vencimento(id, body=body)
        print("The response of AesEmSandboxApi->forcar_vencimento:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AesEmSandboxApi->forcar_vencimento: %s\n" % e)
```

### Parameters

| Name     | Type       | Description                              | Notes      |
| -------- | ---------- | ---------------------------------------- | ---------- |
| **id**   | **str**    | Identificador único da cobrança no Asaas |
| **body** | **object** |                                          | [optional] |

### Return type

[**PaymentGetResponseDTO**](PaymentGetResponseDTO.md)

### Authorization

[Authorization](../README.md#Authorization)

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
