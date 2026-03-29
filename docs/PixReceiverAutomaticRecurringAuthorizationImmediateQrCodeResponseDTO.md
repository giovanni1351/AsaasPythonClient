# PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO

Informações da cobrança imediata

## Properties

| Name                        | Type         | Description                            | Notes      |
| --------------------------- | ------------ | -------------------------------------- | ---------- |
| **conciliation_identifier** | **str**      | Identificador de conciliação           | [optional] |
| **expiration_date**         | **datetime** | Data de expiração da primeira cobrança | [optional] |

## Example

```python
from asaas.models.pix_receiver_automatic_recurring_authorization_immediate_qr_code_response_dto import PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO from a JSON string
pix_receiver_automatic_recurring_authorization_immediate_qr_code_response_dto_instance = PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO.to_json())

# convert the object into a dict
pix_receiver_automatic_recurring_authorization_immediate_qr_code_response_dto_dict = pix_receiver_automatic_recurring_authorization_immediate_qr_code_response_dto_instance.to_dict()
# create an instance of PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO from a dict
pix_receiver_automatic_recurring_authorization_immediate_qr_code_response_dto_from_dict = PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO.from_dict(pix_receiver_automatic_recurring_authorization_immediate_qr_code_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
