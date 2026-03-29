# FiscalInfoGetResponseDTO

## Properties

| Name                                       | Type     | Description                                                                                                                                                                                                                                 | Notes                        |
| ------------------------------------------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| **object**                                 | **str**  | Tipo de objeto                                                                                                                                                                                                                              | [optional]                   |
| **email**                                  | **str**  | Email utilizado pelo Asaas para enviar notificações e alertas de notas fiscais                                                                                                                                                              | [optional]                   |
| **municipal_inscription**                  | **str**  | Inscrição municipal da empresa                                                                                                                                                                                                              | [optional]                   |
| **simples_nacional**                       | **bool** | Indica se a empresa é optante pelo simples nacional                                                                                                                                                                                         | [optional] [default to True] |
| **cultural_projects_promoter**             | **bool** | Identifica se a empresa é classificada como incentivador cultural                                                                                                                                                                           | [optional] [default to True] |
| **cnae**                                   | **str**  | Código CNAE                                                                                                                                                                                                                                 | [optional]                   |
| **special_tax_regime**                     | **str**  | Identificador do regime especial de tributação                                                                                                                                                                                              | [optional]                   |
| **service_list_item**                      | **str**  | Item da lista de serviço, conforme http://www.planalto.gov.br/ccivil_03/leis/LCP/Lcp116.htm                                                                                                                                                 | [optional]                   |
| **nbs_code**                               | **str**  | Código NBS (Nomenclatura Brasileira de Serviços). Deve constar na NFS-e quando exigido pela prefeitura e/ou para serviços de importação ou exportação. Consulte a necessidade desta informação com a sua prefeitura ou a sua contabilidade. | [optional]                   |
| **rps_serie**                              | **str**  | Número de Série cadastrado para a empresa                                                                                                                                                                                                   | [optional]                   |
| **rps_number**                             | **int**  | Número de RPS utilizado na última nota fiscal emitida para a sua empresa                                                                                                                                                                    | [optional]                   |
| **lote_number**                            | **int**  | Número do Lote utilizado na última nota fiscal emitida pela sua empresa                                                                                                                                                                     | [optional]                   |
| **username**                               | **str**  | Usuário para acesso ao site da prefeitura da sua cidade                                                                                                                                                                                     | [optional]                   |
| **password_sent**                          | **bool** | Indica se a senha para acesso ao site da prefeitura foi informada                                                                                                                                                                           | [optional] [default to True] |
| **access_token_sent**                      | **bool** | Indica se o token para acesso ao site da prefeitura foi informado (Caso o acesso ao site da sua prefeitura seja através por Token)                                                                                                          | [optional] [default to True] |
| **certificate_sent**                       | **bool** | Indica se o certificado digital para acesso ao site da prefeitura foi informado                                                                                                                                                             | [optional] [default to True] |
| **national_portal_tax_calculation_regime** | **str**  | Identificador do regime de apuração tributária pelo Simples Nacional                                                                                                                                                                        | [optional]                   |

## Example

```python
from asaas.models.fiscal_info_get_response_dto import FiscalInfoGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoGetResponseDTO from a JSON string
fiscal_info_get_response_dto_instance = FiscalInfoGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoGetResponseDTO.to_json())

# convert the object into a dict
fiscal_info_get_response_dto_dict = fiscal_info_get_response_dto_instance.to_dict()
# create an instance of FiscalInfoGetResponseDTO from a dict
fiscal_info_get_response_dto_from_dict = FiscalInfoGetResponseDTO.from_dict(fiscal_info_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
