# PaymentLimitsResponseCreationDailyDTO

Limites diários

## Properties

| Name            | Type     | Description                     | Notes      |
| --------------- | -------- | ------------------------------- | ---------- |
| **limit**       | **int**  | Limite total                    | [optional] |
| **used**        | **int**  | Limite usado                    | [optional] |
| **was_reached** | **bool** | Indica se o limite foi atingido | [optional] |

## Example

```python
from asaas.models.payment_limits_response_creation_daily_dto import PaymentLimitsResponseCreationDailyDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLimitsResponseCreationDailyDTO from a JSON string
payment_limits_response_creation_daily_dto_instance = PaymentLimitsResponseCreationDailyDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLimitsResponseCreationDailyDTO.to_json())

# convert the object into a dict
payment_limits_response_creation_daily_dto_dict = payment_limits_response_creation_daily_dto_instance.to_dict()
# create an instance of PaymentLimitsResponseCreationDailyDTO from a dict
payment_limits_response_creation_daily_dto_from_dict = PaymentLimitsResponseCreationDailyDTO.from_dict(payment_limits_response_creation_daily_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
