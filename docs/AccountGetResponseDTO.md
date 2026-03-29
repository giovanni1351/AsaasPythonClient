# AccountGetResponseDTO

## Properties

| Name                           | Type                                                                                                    | Description                                                                         | Notes      |
| ------------------------------ | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ---------- |
| **object**                     | **str**                                                                                                 | Tipo de objeto                                                                      | [optional] |
| **id**                         | **str**                                                                                                 | Identificador único da subconta no Asaas                                            | [optional] |
| **name**                       | **str**                                                                                                 | Nome da subconta                                                                    | [optional] |
| **email**                      | **str**                                                                                                 | Email da subconta                                                                   | [optional] |
| **login_email**                | **str**                                                                                                 | Email para login da subconta, caso não informado será utilizado o email da subconta | [optional] |
| **phone**                      | **str**                                                                                                 | Telefone Fixo                                                                       | [optional] |
| **mobile_phone**               | **str**                                                                                                 | Telefone Celular                                                                    | [optional] |
| **address**                    | **str**                                                                                                 | Logradouro                                                                          | [optional] |
| **address_number**             | **str**                                                                                                 | Número do endereço                                                                  | [optional] |
| **complement**                 | **str**                                                                                                 | Complemento do endereço                                                             | [optional] |
| **province**                   | **str**                                                                                                 | Bairro                                                                              | [optional] |
| **postal_code**                | **str**                                                                                                 | CEP do endereço                                                                     | [optional] |
| **cpf_cnpj**                   | **str**                                                                                                 | CPF ou CNPJ do proprietário da subconta                                             | [optional] |
| **birth_date**                 | **date**                                                                                                | Data de nascimento (somente quando Pessoa Física)                                   | [optional] |
| **person_type**                | [**AccountGetResponsePersonType**](AccountGetResponsePersonType.md)                                     |                                                                                     | [optional] |
| **company_type**               | [**AccountGetResponseCompanyType**](AccountGetResponseCompanyType.md)                                   |                                                                                     | [optional] |
| **city**                       | **int**                                                                                                 | Identificador único da cidade no Asaas                                              | [optional] |
| **state**                      | **str**                                                                                                 | Sigla do Estado (SP, RJ, SC, ...)                                                   | [optional] |
| **country**                    | **str**                                                                                                 | País (Fixo Brasil)                                                                  | [optional] |
| **trading_name**               | **str**                                                                                                 | Nome de exibição (preenchido automaticamente)                                       | [optional] |
| **site**                       | **str**                                                                                                 | URL of the subbacount website                                                       | [optional] |
| **wallet_id**                  | **str**                                                                                                 | Unique wallet identifier to split charges or transfer between Asaas accounts        | [optional] |
| **account_number**             | [**AccountNumberDTO**](AccountNumberDTO.md)                                                             |                                                                                     | [optional] |
| **commercial_info_expiration** | [**AccountInfoCommercialInfoExpirationResponseDTO**](AccountInfoCommercialInfoExpirationResponseDTO.md) |                                                                                     | [optional] |
| **access_token**               | [**CustomerApiAccessTokenBaseResponseDTO**](CustomerApiAccessTokenBaseResponseDTO.md)                   |                                                                                     | [optional] |

## Example

```python
from asaas.models.account_get_response_dto import AccountGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountGetResponseDTO from a JSON string
account_get_response_dto_instance = AccountGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AccountGetResponseDTO.to_json())

# convert the object into a dict
account_get_response_dto_dict = account_get_response_dto_instance.to_dict()
# create an instance of AccountGetResponseDTO from a dict
account_get_response_dto_from_dict = AccountGetResponseDTO.from_dict(account_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
