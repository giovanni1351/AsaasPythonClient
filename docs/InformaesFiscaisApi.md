# asaas.InformaesFiscaisApi

All URIs are relative to *https://api-sandbox.asaas.com*

| Method                                                                                                                  | HTTP request                                   | Description                                  |
| ----------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | -------------------------------------------- |
| [**configurar_portal_emissor_de_notas_fiscais**](InformaesFiscaisApi.md#configurar_portal_emissor_de_notas_fiscais)     | **POST** /v3/fiscalInfo/nationalPortal         | Configurar portal emissor de notas fiscais   |
| [**criar_e_atualizar_informacoes_fiscais**](InformaesFiscaisApi.md#criar_e_atualizar_informacoes_fiscais)               | **POST** /v3/fiscalInfo/                       | Criar e atualizar informações fiscais        |
| [**listar_codigos_de_classificacoes_tributarias**](InformaesFiscaisApi.md#listar_codigos_de_classificacoes_tributarias) | **GET** /v3/fiscalInfo/taxClassificationCodes  | Listar códigos de classificações tributárias |
| [**listar_codigos_de_operadores_de_indicacoes**](InformaesFiscaisApi.md#listar_codigos_de_operadores_de_indicacoes)     | **GET** /v3/fiscalInfo/operationIndicatorCodes | Listar códigos de indicadores de operações   |
| [**listar_codigos_de_situacoes_tributarias**](InformaesFiscaisApi.md#listar_codigos_de_situacoes_tributarias)           | **GET** /v3/fiscalInfo/taxSituationCodes       | Listar códigos de situações tributárias      |
| [**listar_codigos_nbs**](InformaesFiscaisApi.md#listar_codigos_nbs)                                                     | **GET** /v3/fiscalInfo/nbsCodes                | Listar códigos NBS                           |
| [**listar_codigos_servicos_federais**](InformaesFiscaisApi.md#listar_codigos_servicos_federais)                         | **GET** /v3/fiscalInfo/federalServiceCodes     | Listar códigos de serviços federais          |
| [**listar_configuracoes_municipais**](InformaesFiscaisApi.md#listar_configuracoes_municipais)                           | **GET** /v3/fiscalInfo/municipalOptions        | Listar configurações municipais              |
| [**listar_servicos_municipais**](InformaesFiscaisApi.md#listar_servicos_municipais)                                     | **GET** /v3/fiscalInfo/services                | Listar serviços municipais                   |
| [**recuperar_informacoes_fiscais**](InformaesFiscaisApi.md#recuperar_informacoes_fiscais)                               | **GET** /v3/fiscalInfo/                        | Recuperar informações fiscais                |

# **configurar_portal_emissor_de_notas_fiscais**

> FiscalInfoUpdateUseNationalPortalResponseDTO configurar_portal_emissor_de_notas_fiscais(fiscal_info_update_use_national_portal_request_dto=fiscal_info_update_use_national_portal_request_dto)

Configurar portal emissor de notas fiscais

Aqui é possível habilitar ou desabilitar o uso do portal nacional como emissor de notas fiscais.

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_update_use_national_portal_request_dto import FiscalInfoUpdateUseNationalPortalRequestDTO
from asaas.models.fiscal_info_update_use_national_portal_response_dto import FiscalInfoUpdateUseNationalPortalResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    fiscal_info_update_use_national_portal_request_dto = asaas.FiscalInfoUpdateUseNationalPortalRequestDTO() # FiscalInfoUpdateUseNationalPortalRequestDTO |  (optional)

    try:
        # Configurar portal emissor de notas fiscais
        api_response = api_instance.configurar_portal_emissor_de_notas_fiscais(fiscal_info_update_use_national_portal_request_dto=fiscal_info_update_use_national_portal_request_dto)
        print("The response of InformaesFiscaisApi->configurar_portal_emissor_de_notas_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->configurar_portal_emissor_de_notas_fiscais: %s\n" % e)
```

### Parameters

| Name                                                   | Type                                                                                              | Description | Notes      |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------- | ----------- | ---------- |
| **fiscal_info_update_use_national_portal_request_dto** | [**FiscalInfoUpdateUseNationalPortalRequestDTO**](FiscalInfoUpdateUseNationalPortalRequestDTO.md) |             | [optional] |

### Return type

[**FiscalInfoUpdateUseNationalPortalResponseDTO**](FiscalInfoUpdateUseNationalPortalResponseDTO.md)

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

# **criar_e_atualizar_informacoes_fiscais**

> FiscalInfoGetResponseDTO criar_e_atualizar_informacoes_fiscais(email, simples_nacional, municipal_inscription=municipal_inscription, cultural_projects_promoter=cultural_projects_promoter, cnae=cnae, special_tax_regime=special_tax_regime, service_list_item=service_list_item, nbs_code=nbs_code, rps_serie=rps_serie, rps_number=rps_number, lote_number=lote_number, username=username, password=password, access_token=access_token, certificate_file=certificate_file, certificate_password=certificate_password, national_portal_tax_calculation_regime=national_portal_tax_calculation_regime)

Criar e atualizar informações fiscais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_get_response_dto import FiscalInfoGetResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    email = 'email_example' # str | Email utilizado pelo Asaas para enviar notificações e alertas de notas fiscais
    simples_nacional = True # bool | Indica se a empresa é optante pelo simples nacional (default to True)
    municipal_inscription = 'municipal_inscription_example' # str | Inscrição municipal da empresa (optional)
    cultural_projects_promoter = True # bool | Identifica se a empresa é classificada como incentivador cultural (optional) (default to True)
    cnae = 'cnae_example' # str | Código CNAE (optional)
    special_tax_regime = 'special_tax_regime_example' # str | Identificador do regime especial de tributação (optional)
    service_list_item = 'service_list_item_example' # str | Item da lista de serviço, conforme http://www.planalto.gov.br/ccivil_03/leis/LCP/Lcp116.htm (optional)
    nbs_code = 'nbs_code_example' # str | Código NBS (Nomenclatura Brasileira de Serviços). Deve constar na NFS-e quando exigido pela prefeitura e/ou para serviços de importação ou exportação. Consulte a necessidade desta informação com a sua prefeitura ou a sua contabilidade. (optional)
    rps_serie = 'rps_serie_example' # str | Número de Série utilizado pela sua empresa para emissão de notas fiscais. Para NFSe no padrão nacional, a série deve seguir a forma de autenticação: Certificado digital (00001 a 49999) ou Usuário e senha (80000 a 89999). Para emissão municipal, na maioria das cidades o número de série utilizado é '1' ou 'E' (optional)
    rps_number = 56 # int | Número do RPS utilizado na última nota fiscal emitida pela sua empresa. Se a sua última NF emitida tem RPS igual a '100', esse campo deve ser preenchido com '101'. Se você nunca emitiu notas fiscais pelo site da sua prefeitura, informe '1' nesse campo (optional)
    lote_number = 56 # int | Número do Lote utilizado na última nota fiscal emitida pela sua empresa. Se o último lote utilizado na sua prefeitura for '25', esse campo deve ser preenchido com '26'. Informe esse campo apenas se sua prefeitura exigir a utilização de lotes (optional)
    username = 'username_example' # str | Usuário para acesso ao site da prefeitura da sua cidade (optional)
    password = 'password_example' # str | Senha para acesso ao site da prefeitura (optional)
    access_token = 'access_token_example' # str | Token de acesso ao site da prefeitura (Caso o acesso ao site da sua prefeitura seja através por Token) (optional)
    certificate_file = None # bytes | Arquivo (optional)
    certificate_password = 'certificate_password_example' # str | Senha do certificado digital enviado (Caso o acesso ao site da sua prefeitura através de certificado digital) (optional)
    national_portal_tax_calculation_regime = 'national_portal_tax_calculation_regime_example' # str | Identificador do regime de apuração tributária pelo Simples Nacional. Deve ser preenchido somente por empresas enquadradas como ME ou EPP optantes do Simples Nacional. Consulte a necessidade desta informação com a sua prefeitura ou a sua contabilidade. (optional)

    try:
        # Criar e atualizar informações fiscais
        api_response = api_instance.criar_e_atualizar_informacoes_fiscais(email, simples_nacional, municipal_inscription=municipal_inscription, cultural_projects_promoter=cultural_projects_promoter, cnae=cnae, special_tax_regime=special_tax_regime, service_list_item=service_list_item, nbs_code=nbs_code, rps_serie=rps_serie, rps_number=rps_number, lote_number=lote_number, username=username, password=password, access_token=access_token, certificate_file=certificate_file, certificate_password=certificate_password, national_portal_tax_calculation_regime=national_portal_tax_calculation_regime)
        print("The response of InformaesFiscaisApi->criar_e_atualizar_informacoes_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->criar_e_atualizar_informacoes_fiscais: %s\n" % e)
```

### Parameters

| Name                                       | Type      | Description                                                                                                                                                                                                                                                                                                                          | Notes                        |
| ------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------- |
| **email**                                  | **str**   | Email utilizado pelo Asaas para enviar notificações e alertas de notas fiscais                                                                                                                                                                                                                                                       |
| **simples_nacional**                       | **bool**  | Indica se a empresa é optante pelo simples nacional                                                                                                                                                                                                                                                                                  | [default to True]            |
| **municipal_inscription**                  | **str**   | Inscrição municipal da empresa                                                                                                                                                                                                                                                                                                       | [optional]                   |
| **cultural_projects_promoter**             | **bool**  | Identifica se a empresa é classificada como incentivador cultural                                                                                                                                                                                                                                                                    | [optional] [default to True] |
| **cnae**                                   | **str**   | Código CNAE                                                                                                                                                                                                                                                                                                                          | [optional]                   |
| **special_tax_regime**                     | **str**   | Identificador do regime especial de tributação                                                                                                                                                                                                                                                                                       | [optional]                   |
| **service_list_item**                      | **str**   | Item da lista de serviço, conforme http://www.planalto.gov.br/ccivil_03/leis/LCP/Lcp116.htm                                                                                                                                                                                                                                          | [optional]                   |
| **nbs_code**                               | **str**   | Código NBS (Nomenclatura Brasileira de Serviços). Deve constar na NFS-e quando exigido pela prefeitura e/ou para serviços de importação ou exportação. Consulte a necessidade desta informação com a sua prefeitura ou a sua contabilidade.                                                                                          | [optional]                   |
| **rps_serie**                              | **str**   | Número de Série utilizado pela sua empresa para emissão de notas fiscais. Para NFSe no padrão nacional, a série deve seguir a forma de autenticação: Certificado digital (00001 a 49999) ou Usuário e senha (80000 a 89999). Para emissão municipal, na maioria das cidades o número de série utilizado é &#39;1&#39; ou &#39;E&#39; | [optional]                   |
| **rps_number**                             | **int**   | Número do RPS utilizado na última nota fiscal emitida pela sua empresa. Se a sua última NF emitida tem RPS igual a &#39;100&#39;, esse campo deve ser preenchido com &#39;101&#39;. Se você nunca emitiu notas fiscais pelo site da sua prefeitura, informe &#39;1&#39; nesse campo                                                  | [optional]                   |
| **lote_number**                            | **int**   | Número do Lote utilizado na última nota fiscal emitida pela sua empresa. Se o último lote utilizado na sua prefeitura for &#39;25&#39;, esse campo deve ser preenchido com &#39;26&#39;. Informe esse campo apenas se sua prefeitura exigir a utilização de lotes                                                                    | [optional]                   |
| **username**                               | **str**   | Usuário para acesso ao site da prefeitura da sua cidade                                                                                                                                                                                                                                                                              | [optional]                   |
| **password**                               | **str**   | Senha para acesso ao site da prefeitura                                                                                                                                                                                                                                                                                              | [optional]                   |
| **access_token**                           | **str**   | Token de acesso ao site da prefeitura (Caso o acesso ao site da sua prefeitura seja através por Token)                                                                                                                                                                                                                               | [optional]                   |
| **certificate_file**                       | **bytes** | Arquivo                                                                                                                                                                                                                                                                                                                              | [optional]                   |
| **certificate_password**                   | **str**   | Senha do certificado digital enviado (Caso o acesso ao site da sua prefeitura através de certificado digital)                                                                                                                                                                                                                        | [optional]                   |
| **national_portal_tax_calculation_regime** | **str**   | Identificador do regime de apuração tributária pelo Simples Nacional. Deve ser preenchido somente por empresas enquadradas como ME ou EPP optantes do Simples Nacional. Consulte a necessidade desta informação com a sua prefeitura ou a sua contabilidade.                                                                         | [optional]                   |

### Return type

[**FiscalInfoGetResponseDTO**](FiscalInfoGetResponseDTO.md)

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
| **400**     | Bad Request  | -                |

[[Back to top]](#) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to Model list]](index.md#documentation-for-models) [[Back to README]](index.md)

# **listar_codigos_de_classificacoes_tributarias**

> FiscalInfoTaxClassificationCodeListResponseDTO listar_codigos_de_classificacoes_tributarias(offset=offset, limit=limit, code=code, description=description, tax_situation_code=tax_situation_code)

Listar códigos de classificações tributárias

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_tax_classification_code_list_response_dto import FiscalInfoTaxClassificationCodeListResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    code = '011001' # str | Código da classificação tributária (optional)
    description = 'Situações tributadas integralmente pela IBS e pela CBS' # str | Descrição (optional)
    tax_situation_code = '011' # str | Código da situação tributária (optional)

    try:
        # Listar códigos de classificações tributárias
        api_response = api_instance.listar_codigos_de_classificacoes_tributarias(offset=offset, limit=limit, code=code, description=description, tax_situation_code=tax_situation_code)
        print("The response of InformaesFiscaisApi->listar_codigos_de_classificacoes_tributarias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_codigos_de_classificacoes_tributarias: %s\n" % e)
```

### Parameters

| Name                   | Type    | Description                             | Notes      |
| ---------------------- | ------- | --------------------------------------- | ---------- |
| **offset**             | **int** | Elemento inicial da lista               | [optional] |
| **limit**              | **int** | Número de elementos da lista (max: 100) | [optional] |
| **code**               | **str** | Código da classificação tributária      | [optional] |
| **description**        | **str** | Descrição                               | [optional] |
| **tax_situation_code** | **str** | Código da situação tributária           | [optional] |

### Return type

[**FiscalInfoTaxClassificationCodeListResponseDTO**](FiscalInfoTaxClassificationCodeListResponseDTO.md)

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

# **listar_codigos_de_operadores_de_indicacoes**

> FiscalInfoOperationIndicatorCodeListResponseDTO listar_codigos_de_operadores_de_indicacoes(offset=offset, limit=limit, code=code, description=description)

Listar códigos de indicadores de operações

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_operation_indicator_code_list_response_dto import FiscalInfoOperationIndicatorCodeListResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    code = '020101' # str | Código do indicador da operação (optional)
    description = 'Execução de operações com bem imóvel, bem imaterial, inclusive direito, relacionado a bem imóvel' # str | Descrição (optional)

    try:
        # Listar códigos de indicadores de operações
        api_response = api_instance.listar_codigos_de_operadores_de_indicacoes(offset=offset, limit=limit, code=code, description=description)
        print("The response of InformaesFiscaisApi->listar_codigos_de_operadores_de_indicacoes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_codigos_de_operadores_de_indicacoes: %s\n" % e)
```

### Parameters

| Name            | Type    | Description                             | Notes      |
| --------------- | ------- | --------------------------------------- | ---------- |
| **offset**      | **int** | Elemento inicial da lista               | [optional] |
| **limit**       | **int** | Número de elementos da lista (max: 100) | [optional] |
| **code**        | **str** | Código do indicador da operação         | [optional] |
| **description** | **str** | Descrição                               | [optional] |

### Return type

[**FiscalInfoOperationIndicatorCodeListResponseDTO**](FiscalInfoOperationIndicatorCodeListResponseDTO.md)

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

# **listar_codigos_de_situacoes_tributarias**

> FiscalInfoTaxSituationCodeListResponseDTO listar_codigos_de_situacoes_tributarias(offset=offset, limit=limit, code=code, description=description)

Listar códigos de situações tributárias

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_tax_situation_code_list_response_dto import FiscalInfoTaxSituationCodeListResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    code = '200001' # str | Código da situação tributária (optional)
    description = 'Tributação com alíquotas uniformes reduzidas' # str | Descrição (optional)

    try:
        # Listar códigos de situações tributárias
        api_response = api_instance.listar_codigos_de_situacoes_tributarias(offset=offset, limit=limit, code=code, description=description)
        print("The response of InformaesFiscaisApi->listar_codigos_de_situacoes_tributarias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_codigos_de_situacoes_tributarias: %s\n" % e)
```

### Parameters

| Name            | Type    | Description                             | Notes      |
| --------------- | ------- | --------------------------------------- | ---------- |
| **offset**      | **int** | Elemento inicial da lista               | [optional] |
| **limit**       | **int** | Número de elementos da lista (max: 100) | [optional] |
| **code**        | **str** | Código da situação tributária           | [optional] |
| **description** | **str** | Descrição                               | [optional] |

### Return type

[**FiscalInfoTaxSituationCodeListResponseDTO**](FiscalInfoTaxSituationCodeListResponseDTO.md)

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

# **listar_codigos_nbs**

> FiscalInfoListInvoiceNbsCodesResponseDTO listar_codigos_nbs(offset=offset, limit=limit, code_description=code_description)

Listar códigos NBS

Listagem dos possíveis códigos NBS (Nomenclatura Brasileira de Serviços)

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_list_invoice_nbs_codes_response_dto import FiscalInfoListInvoiceNbsCodesResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    code_description = '1.0101.11.00 - Serviços de construção de edificações residenciais de um e dois pavimentos' # str | Código NBS e descrição (optional)

    try:
        # Listar códigos NBS
        api_response = api_instance.listar_codigos_nbs(offset=offset, limit=limit, code_description=code_description)
        print("The response of InformaesFiscaisApi->listar_codigos_nbs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_codigos_nbs: %s\n" % e)
```

### Parameters

| Name                 | Type    | Description                             | Notes      |
| -------------------- | ------- | --------------------------------------- | ---------- |
| **offset**           | **int** | Elemento inicial da lista               | [optional] |
| **limit**            | **int** | Número de elementos da lista (max: 100) | [optional] |
| **code_description** | **str** | Código NBS e descrição                  | [optional] |

### Return type

[**FiscalInfoListInvoiceNbsCodesResponseDTO**](FiscalInfoListInvoiceNbsCodesResponseDTO.md)

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

# **listar_codigos_servicos_federais**

> FiscalInfoFederalServiceCodeListResponseDTO listar_codigos_servicos_federais(offset=offset, limit=limit, code=code, description=description)

Listar códigos de serviços federais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_federal_service_code_list_response_dto import FiscalInfoFederalServiceCodeListResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    code = '040801' # str | Código tributário (optional)
    description = 'Terapia ocupacional' # str | Descrição (optional)

    try:
        # Listar códigos de serviços federais
        api_response = api_instance.listar_codigos_servicos_federais(offset=offset, limit=limit, code=code, description=description)
        print("The response of InformaesFiscaisApi->listar_codigos_servicos_federais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_codigos_servicos_federais: %s\n" % e)
```

### Parameters

| Name            | Type    | Description                             | Notes      |
| --------------- | ------- | --------------------------------------- | ---------- |
| **offset**      | **int** | Elemento inicial da lista               | [optional] |
| **limit**       | **int** | Número de elementos da lista (max: 100) | [optional] |
| **code**        | **str** | Código tributário                       | [optional] |
| **description** | **str** | Descrição                               | [optional] |

### Return type

[**FiscalInfoFederalServiceCodeListResponseDTO**](FiscalInfoFederalServiceCodeListResponseDTO.md)

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

# **listar_configuracoes_municipais**

> FiscalInfoMunicipalOptionsGetResponseDTO listar_configuracoes_municipais()

Listar configurações municipais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_municipal_options_get_response_dto import FiscalInfoMunicipalOptionsGetResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)

    try:
        # Listar configurações municipais
        api_response = api_instance.listar_configuracoes_municipais()
        print("The response of InformaesFiscaisApi->listar_configuracoes_municipais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_configuracoes_municipais: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**FiscalInfoMunicipalOptionsGetResponseDTO**](FiscalInfoMunicipalOptionsGetResponseDTO.md)

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

# **listar_servicos_municipais**

> FiscalInfoListMunicipalServicesResponseDTO listar_servicos_municipais(offset=offset, limit=limit, description=description)

Listar serviços municipais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_list_municipal_services_response_dto import FiscalInfoListMunicipalServicesResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)
    offset = 0 # int | Elemento inicial da lista (optional)
    limit = 10 # int | Número de elementos da lista (max: 100) (optional)
    description = '1.01' # str | Nome do serviço (optional)

    try:
        # Listar serviços municipais
        api_response = api_instance.listar_servicos_municipais(offset=offset, limit=limit, description=description)
        print("The response of InformaesFiscaisApi->listar_servicos_municipais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->listar_servicos_municipais: %s\n" % e)
```

### Parameters

| Name            | Type    | Description                             | Notes      |
| --------------- | ------- | --------------------------------------- | ---------- |
| **offset**      | **int** | Elemento inicial da lista               | [optional] |
| **limit**       | **int** | Número de elementos da lista (max: 100) | [optional] |
| **description** | **str** | Nome do serviço                         | [optional] |

### Return type

[**FiscalInfoListMunicipalServicesResponseDTO**](FiscalInfoListMunicipalServicesResponseDTO.md)

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

# **recuperar_informacoes_fiscais**

> FiscalInfoGetResponseDTO recuperar_informacoes_fiscais()

Recuperar informações fiscais

### Example

- Api Key Authentication (Authorization):

```python
import asaas
from asaas.models.fiscal_info_get_response_dto import FiscalInfoGetResponseDTO
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
    api_instance = asaas.InformaesFiscaisApi(api_client)

    try:
        # Recuperar informações fiscais
        api_response = api_instance.recuperar_informacoes_fiscais()
        print("The response of InformaesFiscaisApi->recuperar_informacoes_fiscais:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InformaesFiscaisApi->recuperar_informacoes_fiscais: %s\n" % e)
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**FiscalInfoGetResponseDTO**](FiscalInfoGetResponseDTO.md)

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
