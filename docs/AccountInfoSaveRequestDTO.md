# AccountInfoSaveRequestDTO

## Properties

| Name               | Type                                                                          | Description                                                              | Notes      |
| ------------------ | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------- |
| **person_type**    | [**AccountInfoSaveRequestPersonType**](AccountInfoSaveRequestPersonType.md)   |                                                                          | [optional] |
| **cpf_cnpj**       | **str**                                                                       | CPF ou CNPJ do proprietário da conta                                     | [optional] |
| **birth_date**     | **date**                                                                      | Data de nascimento necessária caso as informações forem de pessoa física | [optional] |
| **company_type**   | [**AccountInfoSaveRequestCompanyType**](AccountInfoSaveRequestCompanyType.md) |                                                                          | [optional] |
| **company_name**   | **str**                                                                       | Nome da empresa                                                          | [optional] |
| **income_value**   | **float**                                                                     | Faturamento/Renda mensal                                                 | [optional] |
| **email**          | **str**                                                                       | E-mail da conta                                                          | [optional] |
| **phone**          | **str**                                                                       | Telefone                                                                 | [optional] |
| **mobile_phone**   | **str**                                                                       | Telefone Celular                                                         | [optional] |
| **site**           | **str**                                                                       | Website                                                                  | [optional] |
| **postal_code**    | **str**                                                                       | CEP do endereço                                                          | [optional] |
| **address**        | **str**                                                                       | Logradouro                                                               | [optional] |
| **address_number** | **str**                                                                       | Número do endereço                                                       | [optional] |
| **complement**     | **str**                                                                       | Complemento do endereço                                                  | [optional] |
| **province**       | **str**                                                                       | Bairro                                                                   | [optional] |

## Example

```python
from asaas.models.account_info_save_request_dto import AccountInfoSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountInfoSaveRequestDTO from a JSON string
account_info_save_request_dto_instance = AccountInfoSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(AccountInfoSaveRequestDTO.to_json())

# convert the object into a dict
account_info_save_request_dto_dict = account_info_save_request_dto_instance.to_dict()
# create an instance of AccountInfoSaveRequestDTO from a dict
account_info_save_request_dto_from_dict = AccountInfoSaveRequestDTO.from_dict(account_info_save_request_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
