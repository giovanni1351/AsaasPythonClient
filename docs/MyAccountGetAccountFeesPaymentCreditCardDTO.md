# MyAccountGetAccountFeesPaymentCreditCardDTO

Taxas de cartão de crédito

## Properties

| Name                                                  | Type         | Description                                                   | Notes      |
| ----------------------------------------------------- | ------------ | ------------------------------------------------------------- | ---------- |
| **operation_value**                                   | **float**    | Taxa operacional por cobrança                                 | [optional] |
| **one_installment_percentage**                        | **float**    | Taxa percentual à vista                                       | [optional] |
| **up_to_six_installments_percentage**                 | **float**    | Taxa percentual para 2 à 6 parcelas                           | [optional] |
| **up_to_twelve_installments_percentage**              | **float**    | Taxa percentual para 7 à 12 parcelas                          | [optional] |
| **up_to_twenty_one_installments_percentage**          | **float**    | Taxa percentual para 13 à 21 parcelas                         | [optional] |
| **discount_one_installment_percentage**               | **float**    | Taxa percentual à vista promocional (Se houver)               | [optional] |
| **discount_up_to_six_installments_percentage**        | **float**    | Taxa percentual para 2 à 6 parcelas promocional (Se houver)   | [optional] |
| **discount_up_to_twelve_installments_percentage**     | **float**    | Taxa percentual para 7 à 12 parcelas promocional (Se houver)  | [optional] |
| **discount_up_to_twenty_one_installments_percentage** | **float**    | Taxa percentual para 13 à 21 parcelas promocional (Se houver) | [optional] |
| **discount_expiration**                               | **datetime** | Data de expiração da taxa promocional (Se houver)             | [optional] |
| **days_to_receive**                                   | **int**      | Dias para recebimento da cobrança                             | [optional] |

## Example

```python
from asaas.models.my_account_get_account_fees_payment_credit_card_dto import MyAccountGetAccountFeesPaymentCreditCardDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesPaymentCreditCardDTO from a JSON string
my_account_get_account_fees_payment_credit_card_dto_instance = MyAccountGetAccountFeesPaymentCreditCardDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesPaymentCreditCardDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_payment_credit_card_dto_dict = my_account_get_account_fees_payment_credit_card_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesPaymentCreditCardDTO from a dict
my_account_get_account_fees_payment_credit_card_dto_from_dict = MyAccountGetAccountFeesPaymentCreditCardDTO.from_dict(my_account_get_account_fees_payment_credit_card_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
