# PaymentSaveWithCreditCardCreditCardDTO

Informações do cartão de crédito

## Properties

| Name                   | Type                                                                                                            | Description                                                 | Notes      |
| ---------------------- | --------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | ---------- |
| **credit_card_number** | **str**                                                                                                         | Últimos 4 dígitos do cartão utilizado                       | [optional] |
| **credit_card_brand**  | [**PaymentSaveWithCreditCardCreditCardCreditCardBrand**](PaymentSaveWithCreditCardCreditCardCreditCardBrand.md) |                                                             | [optional] |
| **credit_card_token**  | **str**                                                                                                         | Token do cartão de crédito caso a tokenização esteja ativa. | [optional] |

## Example

```python
from asaas.models.payment_save_with_credit_card_credit_card_dto import PaymentSaveWithCreditCardCreditCardDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSaveWithCreditCardCreditCardDTO from a JSON string
payment_save_with_credit_card_credit_card_dto_instance = PaymentSaveWithCreditCardCreditCardDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSaveWithCreditCardCreditCardDTO.to_json())

# convert the object into a dict
payment_save_with_credit_card_credit_card_dto_dict = payment_save_with_credit_card_credit_card_dto_instance.to_dict()
# create an instance of PaymentSaveWithCreditCardCreditCardDTO from a dict
payment_save_with_credit_card_credit_card_dto_from_dict = PaymentSaveWithCreditCardCreditCardDTO.from_dict(payment_save_with_credit_card_credit_card_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
