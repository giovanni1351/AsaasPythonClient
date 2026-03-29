# CreditCardHolderInfoRequestDTO

Informações do titular do cartão de crédito

## Properties

| Name                   | Type    | Description                                  | Notes      |
| ---------------------- | ------- | -------------------------------------------- | ---------- |
| **name**               | **str** | Nome do titular do cartão                    |
| **email**              | **str** | Email do titular do cartão                   |
| **cpf_cnpj**           | **str** | CPF ou CNPJ do titular do cartão             |
| **postal_code**        | **str** | CEP do titular do cartão                     |
| **address_number**     | **str** | Número do endereço do titular do cartão      |
| **address_complement** | **str** | Complemento do endereço do titular do cartão | [optional] |
| **phone**              | **str** | Telefone com DDD do titular do cartão        |
| **mobile_phone**       | **str** | Celular do titular do cartão                 | [optional] |

## Example

```python
from asaas.models.credit_card_holder_info_request_dto import CreditCardHolderInfoRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditCardHolderInfoRequestDTO from a JSON string
credit_card_holder_info_request_dto_instance = CreditCardHolderInfoRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CreditCardHolderInfoRequestDTO.to_json())

# convert the object into a dict
credit_card_holder_info_request_dto_dict = credit_card_holder_info_request_dto_instance.to_dict()
# create an instance of CreditCardHolderInfoRequestDTO from a dict
credit_card_holder_info_request_dto_from_dict = CreditCardHolderInfoRequestDTO.from_dict(credit_card_holder_info_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
