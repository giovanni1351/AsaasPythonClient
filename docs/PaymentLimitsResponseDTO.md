# PaymentLimitsResponseDTO

## Properties

| Name         | Type                                                                        | Description | Notes      |
| ------------ | --------------------------------------------------------------------------- | ----------- | ---------- |
| **creation** | [**PaymentLimitsResponseCreationDTO**](PaymentLimitsResponseCreationDTO.md) |             | [optional] |

## Example

```python
from asaas.models.payment_limits_response_dto import PaymentLimitsResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLimitsResponseDTO from a JSON string
payment_limits_response_dto_instance = PaymentLimitsResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLimitsResponseDTO.to_json())

# convert the object into a dict
payment_limits_response_dto_dict = payment_limits_response_dto_instance.to_dict()
# create an instance of PaymentLimitsResponseDTO from a dict
payment_limits_response_dto_from_dict = PaymentLimitsResponseDTO.from_dict(payment_limits_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
