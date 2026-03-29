# CheckoutSessionCustomerDataDTO

Dados do cliente

## Properties

| Name               | Type    | Description                                   | Notes      |
| ------------------ | ------- | --------------------------------------------- | ---------- |
| **name**           | **str** | Nome do cliente                               | [optional] |
| **cpf_cnpj**       | **str** | CPF ou CNPJ do cliente                        | [optional] |
| **email**          | **str** | E-mail do cliente                             | [optional] |
| **phone**          | **str** | Telefone do cliente                           | [optional] |
| **address**        | **str** | Endereço do cliente                           | [optional] |
| **address_number** | **int** | Número do endereço                            | [optional] |
| **complement**     | **str** | Complemento do endereço (máx. 255 caracteres) | [optional] |
| **province**       | **str** | Província do endereço                         | [optional] |
| **postal_code**    | **str** | Código postal do endereço                     | [optional] |
| **city**           | **int** | Código da cidade                              | [optional] |

## Example

```python
from asaas.models.checkout_session_customer_data_dto import CheckoutSessionCustomerDataDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionCustomerDataDTO from a JSON string
checkout_session_customer_data_dto_instance = CheckoutSessionCustomerDataDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionCustomerDataDTO.to_json())

# convert the object into a dict
checkout_session_customer_data_dto_dict = checkout_session_customer_data_dto_instance.to_dict()
# create an instance of CheckoutSessionCustomerDataDTO from a dict
checkout_session_customer_data_dto_from_dict = CheckoutSessionCustomerDataDTO.from_dict(checkout_session_customer_data_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
