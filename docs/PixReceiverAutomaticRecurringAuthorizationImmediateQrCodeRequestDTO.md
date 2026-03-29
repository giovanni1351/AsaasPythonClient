# PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO

Cobrança imediata atrelada a ativação da autorização

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pix_key** | **str** | Chave Pix atrelada a primeira cobrança | [optional] 
**expiration_seconds** | **int** | Tempo de expiração em segundos para a primeira cobrança | 
**original_value** | **float** | Valor original da primeira cobrança | 
**description** | **str** | Descrição da primeira cobrança | [optional] 

## Example

```python
from asaas.models.pix_receiver_automatic_recurring_authorization_immediate_qr_code_request_dto import PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO from a JSON string
pix_receiver_automatic_recurring_authorization_immediate_qr_code_request_dto_instance = PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO.to_json())

# convert the object into a dict
pix_receiver_automatic_recurring_authorization_immediate_qr_code_request_dto_dict = pix_receiver_automatic_recurring_authorization_immediate_qr_code_request_dto_instance.to_dict()
# create an instance of PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO from a dict
pix_receiver_automatic_recurring_authorization_immediate_qr_code_request_dto_from_dict = PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO.from_dict(pix_receiver_automatic_recurring_authorization_immediate_qr_code_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


