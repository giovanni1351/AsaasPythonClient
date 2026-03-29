# CreditCardTokenizeRequestDTO

## Properties

| Name                        | Type                                                                    | Description                                                                              | Notes |
| --------------------------- | ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ----- |
| **customer**                | **str**                                                                 | Identificador único do cliente no Asaas                                                  |
| **credit_card**             | [**CreditCardRequestDTO**](CreditCardRequestDTO.md)                     |                                                                                          |
| **credit_card_holder_info** | [**CreditCardHolderInfoRequestDTO**](CreditCardHolderInfoRequestDTO.md) |                                                                                          |
| **remote_ip**               | **str**                                                                 | IP de onde o cliente está fazendo a compra. Não deve ser informado o IP do seu servidor. |

## Example

```python
from asaas.models.credit_card_tokenize_request_dto import CreditCardTokenizeRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditCardTokenizeRequestDTO from a JSON string
credit_card_tokenize_request_dto_instance = CreditCardTokenizeRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CreditCardTokenizeRequestDTO.to_json())

# convert the object into a dict
credit_card_tokenize_request_dto_dict = credit_card_tokenize_request_dto_instance.to_dict()
# create an instance of CreditCardTokenizeRequestDTO from a dict
credit_card_tokenize_request_dto_from_dict = CreditCardTokenizeRequestDTO.from_dict(credit_card_tokenize_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
