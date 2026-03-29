# PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO

Autorização do Pix Automático vinculada

## Properties

| Name                      | Type    | Description                                                        | Notes      |
| ------------------------- | ------- | ------------------------------------------------------------------ | ---------- |
| **id**                    | **str** | Identificador único da autorização do Pix Automático vinculada     | [optional] |
| **end_to_end_identifier** | **str** | Identificador fim a fim da autorização do Pix Automático vinculada | [optional] |
| **customer_id**           | **str** | Identificador único do cliente                                     | [optional] |

## Example

```python
from asaas.models.pix_automatic_recurring_payment_instruction_authorization_response_dto import PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO from a JSON string
pix_automatic_recurring_payment_instruction_authorization_response_dto_instance = PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO.to_json())

# convert the object into a dict
pix_automatic_recurring_payment_instruction_authorization_response_dto_dict = pix_automatic_recurring_payment_instruction_authorization_response_dto_instance.to_dict()
# create an instance of PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO from a dict
pix_automatic_recurring_payment_instruction_authorization_response_dto_from_dict = PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO.from_dict(pix_automatic_recurring_payment_instruction_authorization_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
