# PaymentLimitsResponseCreationDTO

Limites de criação

## Properties

| Name      | Type                                                                                  | Description | Notes      |
| --------- | ------------------------------------------------------------------------------------- | ----------- | ---------- |
| **daily** | [**PaymentLimitsResponseCreationDailyDTO**](PaymentLimitsResponseCreationDailyDTO.md) |             | [optional] |

## Example

```python
from asaas.models.payment_limits_response_creation_dto import PaymentLimitsResponseCreationDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLimitsResponseCreationDTO from a JSON string
payment_limits_response_creation_dto_instance = PaymentLimitsResponseCreationDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLimitsResponseCreationDTO.to_json())

# convert the object into a dict
payment_limits_response_creation_dto_dict = payment_limits_response_creation_dto_instance.to_dict()
# create an instance of PaymentLimitsResponseCreationDTO from a dict
payment_limits_response_creation_dto_from_dict = PaymentLimitsResponseCreationDTO.from_dict(payment_limits_response_creation_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
