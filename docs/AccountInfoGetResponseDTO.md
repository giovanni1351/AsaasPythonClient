# AccountInfoGetResponseDTO

## Properties

| Name                           | Type                                                                                                    | Description                                                                              | Notes      |
| ------------------------------ | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------- |
| **status**                     | [**AccountInfoGetResponseStatus**](AccountInfoGetResponseStatus.md)                                     |                                                                                          | [optional] |
| **person_type**                | [**AccountInfoGetResponsePersonType**](AccountInfoGetResponsePersonType.md)                             |                                                                                          | [optional] |
| **cpf_cnpj**                   | **str**                                                                                                 | CPF ou CNPJ do proprietário da conta                                                     | [optional] |
| **name**                       | **str**                                                                                                 | Nome do proprietário da conta                                                            | [optional] |
| **birth_date**                 | **date**                                                                                                | Data de nascimento necessária caso as informações forem de pessoa física                 | [optional] |
| **company_name**               | **str**                                                                                                 | Nome da empresa                                                                          | [optional] |
| **company_type**               | [**AccountInfoGetResponseCompanyType**](AccountInfoGetResponseCompanyType.md)                           |                                                                                          | [optional] |
| **income_value**               | **float**                                                                                               | Faturamento/Renda mensal                                                                 | [optional] |
| **email**                      | **str**                                                                                                 | E-mail da conta                                                                          | [optional] |
| **phone**                      | **str**                                                                                                 | Telefone                                                                                 | [optional] |
| **mobile_phone**               | **str**                                                                                                 | Telefone Celular                                                                         | [optional] |
| **postal_code**                | **str**                                                                                                 | CEP do endereço                                                                          | [optional] |
| **address**                    | **str**                                                                                                 | Logradouro                                                                               | [optional] |
| **address_number**             | **str**                                                                                                 | Número do endereço                                                                       | [optional] |
| **complement**                 | **str**                                                                                                 | Complemento do endereço                                                                  | [optional] |
| **province**                   | **str**                                                                                                 | Bairro                                                                                   | [optional] |
| **city**                       | [**AccountInfoCityDTO**](AccountInfoCityDTO.md)                                                         |                                                                                          | [optional] |
| **denial_reason**              | **str**                                                                                                 | Motivo pelo qual é necessário reenviar as informações                                    | [optional] |
| **trading_name**               | **str**                                                                                                 | Nome de exibição (preenchido automaticamente)                                            | [optional] |
| **site**                       | **str**                                                                                                 | Website                                                                                  | [optional] |
| **available_company_names**    | **List[str]**                                                                                           | Nomes de empresa disponíveis. Preenchido apenas para contas do tipo Pessoa Jurídica(PJ). | [optional] |
| **commercial_info_expiration** | [**AccountInfoCommercialInfoExpirationResponseDTO**](AccountInfoCommercialInfoExpirationResponseDTO.md) |                                                                                          | [optional] |

## Example

```python
from asaas.models.account_info_get_response_dto import AccountInfoGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountInfoGetResponseDTO from a JSON string
account_info_get_response_dto_instance = AccountInfoGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountInfoGetResponseDTO.to_json())

# convert the object into a dict
account_info_get_response_dto_dict = account_info_get_response_dto_instance.to_dict()
# create an instance of AccountInfoGetResponseDTO from a dict
account_info_get_response_dto_from_dict = AccountInfoGetResponseDTO.from_dict(account_info_get_response_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
