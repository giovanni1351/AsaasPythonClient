# AccountSaveRequestDTO

## Properties

| Name               | Type                                                                    | Description                                                                         | Notes      |
| ------------------ | ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ---------- |
| **name**           | **str**                                                                 | Nome da subconta                                                                    |
| **email**          | **str**                                                                 | Email da subconta                                                                   |
| **login_email**    | **str**                                                                 | Email para login da subconta, caso não informado será utilizado o email da subconta | [optional] |
| **cpf_cnpj**       | **str**                                                                 | CPF ou CNPJ do proprietário da subconta                                             |
| **birth_date**     | **date**                                                                | Data de nascimento (somente quando Pessoa Física)                                   | [optional] |
| **company_type**   | [**AccountSaveRequestCompanyType**](AccountSaveRequestCompanyType.md)   |                                                                                     | [optional] |
| **phone**          | **str**                                                                 | Telefone Fixo                                                                       | [optional] |
| **mobile_phone**   | **str**                                                                 | Telefone Celular                                                                    |
| **site**           | **str**                                                                 | URL of the subbacount website                                                       | [optional] |
| **income_value**   | **float**                                                               | Faturamento/Renda mensal                                                            |
| **address**        | **str**                                                                 | Logradouro                                                                          |
| **address_number** | **str**                                                                 | Número do endereço                                                                  |
| **complement**     | **str**                                                                 | Complemento do endereço                                                             | [optional] |
| **province**       | **str**                                                                 | Bairro                                                                              |
| **postal_code**    | **str**                                                                 | CEP do endereço                                                                     |
| **webhooks**       | [**List[WebhookConfigSaveRequestDTO]**](WebhookConfigSaveRequestDTO.md) | Array com as configurações de Webhooks desejadas                                    | [optional] |

## Example

```python
from asaas.models.account_save_request_dto import AccountSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AccountSaveRequestDTO from a JSON string
account_save_request_dto_instance = AccountSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(AccountSaveRequestDTO.to_json())

# convert the object into a dict
account_save_request_dto_dict = account_save_request_dto_instance.to_dict()
# create an instance of AccountSaveRequestDTO from a dict
account_save_request_dto_from_dict = AccountSaveRequestDTO.from_dict(account_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
