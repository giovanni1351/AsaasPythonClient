# PaymentDiscountDTO

Informações de desconto

## Properties

| Name                    | Type                                                              | Description                                                                                                                                                | Notes      |
| ----------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| **value**               | **float**                                                         | Valor percentual ou fixo de desconto a ser aplicado sobre o valor da cobrança                                                                              | [optional] |
| **due_date_limit_days** | **int**                                                           | Dias antes do vencimento para aplicar desconto. Ex: 0 &#x3D; até o vencimento, 1 &#x3D; até um dia antes, 2 &#x3D; até dois dias antes, e assim por diante | [optional] |
| **type**                | [**PaymentDiscountDiscountType**](PaymentDiscountDiscountType.md) |                                                                                                                                                            | [optional] |

## Example

```python
from asaas.models.payment_discount_dto import PaymentDiscountDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDiscountDTO from a JSON string
payment_discount_dto_instance = PaymentDiscountDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDiscountDTO.to_json())

# convert the object into a dict
payment_discount_dto_dict = payment_discount_dto_instance.to_dict()
# create an instance of PaymentDiscountDTO from a dict
payment_discount_dto_from_dict = PaymentDiscountDTO.from_dict(payment_discount_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
