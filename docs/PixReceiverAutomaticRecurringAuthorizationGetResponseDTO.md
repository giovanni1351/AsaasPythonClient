# PixReceiverAutomaticRecurringAuthorizationGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da autorização de Pix Automático no Asaas | [optional] 
**min_limit_value** | **float** | Se o usuário pagador atribuir um valor máximo para os pagamentos daquela autorização, ele não poderá ser inferior ao piso definido pelo usuário recebedor. Não pode ser preenchido nas autorizações de valor fixo, ou seja, com campo valor preenchido | [optional] 
**cancellation_date** | **date** | Data de cancelamento da autorização | [optional] 
**cancellation_reason** | **str** | Motivo do cancelamento | [optional] 
**contract_id** | **str** | Número, identificador, ou código que representa o objeto da autorização | [optional] 
**customer_id** | **str** | Identificador único do cliente | [optional] 
**description** | **str** | Descrição da autorização | [optional] 
**finish_date** | **date** | Fim da vigência da autorização | [optional] 
**frequency** | [**PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringFrequency**](PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringFrequency.md) |  | [optional] 
**end_to_end_identifier** | **str** | Identificador fim a fim | [optional] 
**start_date** | **date** | Inicio da vigência da autorização e dos pagamentos | [optional] 
**status** | [**PixReceiverAutomaticRecurringAuthorizationGetResponsePixReceiverAutomaticRecurringAuthorizationStatus**](PixReceiverAutomaticRecurringAuthorizationGetResponsePixReceiverAutomaticRecurringAuthorizationStatus.md) |  | [optional] 
**value** | **float** | Valor fixo para as cobranças periódicas | [optional] 
**payload** | **str** | Payload do QR Code | [optional] 
**encoded_image** | **str** | Imagem do QR Code em base64 | [optional] 
**immediate_qr_code** | [**PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO**](PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeResponseDTO.md) |  | [optional] 
**origin_type** | [**PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringOriginType**](PixReceiverAutomaticRecurringAuthorizationGetResponsePixAutomaticRecurringOriginType.md) |  | [optional] 
**subscription_id** | **str** | Identificador único da assinatura vinculada | [optional] 

## Example

```python
from asaas.models.pix_receiver_automatic_recurring_authorization_get_response_dto import PixReceiverAutomaticRecurringAuthorizationGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixReceiverAutomaticRecurringAuthorizationGetResponseDTO from a JSON string
pix_receiver_automatic_recurring_authorization_get_response_dto_instance = PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.to_json())

# convert the object into a dict
pix_receiver_automatic_recurring_authorization_get_response_dto_dict = pix_receiver_automatic_recurring_authorization_get_response_dto_instance.to_dict()
# create an instance of PixReceiverAutomaticRecurringAuthorizationGetResponseDTO from a dict
pix_receiver_automatic_recurring_authorization_get_response_dto_from_dict = PixReceiverAutomaticRecurringAuthorizationGetResponseDTO.from_dict(pix_receiver_automatic_recurring_authorization_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


