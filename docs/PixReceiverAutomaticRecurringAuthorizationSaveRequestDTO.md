# PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**frequency** | [**PixReceiverAutomaticRecurringAuthorizationSaveRequestPixAutomaticRecurringFrequency**](PixReceiverAutomaticRecurringAuthorizationSaveRequestPixAutomaticRecurringFrequency.md) |  | 
**contract_id** | **str** | Número, identificador, ou código que representa o objeto da autorização | 
**start_date** | **date** | Inicio da vigência da autorização e dos pagamentos | 
**finish_date** | **date** | Fim da vigência da autorização. Opcional caso o Pix Automático seja de prazo indeterminado | [optional] 
**value** | **float** | Valor fixo para as cobranças periódicas. | [optional] 
**description** | **str** | Descrição | [optional] 
**customer_id** | **str** | Identificador único do cliente | 
**immediate_qr_code** | [**PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO**](PixReceiverAutomaticRecurringAuthorizationImmediateQrCodeRequestDTO.md) |  | 
**min_limit_value** | **float** | Se o usuário pagador atribuir um valor máximo para os pagamentos daquela autorização, ele não poderá ser inferior ao piso definido pelo usuário recebedor. Não pode ser preenchido nas autorizações de valor fixo, ou seja, com campo valor preenchido | [optional] 

## Example

```python
from asaas.models.pix_receiver_automatic_recurring_authorization_save_request_dto import PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO from a JSON string
pix_receiver_automatic_recurring_authorization_save_request_dto_instance = PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO.to_json())

# convert the object into a dict
pix_receiver_automatic_recurring_authorization_save_request_dto_dict = pix_receiver_automatic_recurring_authorization_save_request_dto_instance.to_dict()
# create an instance of PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO from a dict
pix_receiver_automatic_recurring_authorization_save_request_dto_from_dict = PixReceiverAutomaticRecurringAuthorizationSaveRequestDTO.from_dict(pix_receiver_automatic_recurring_authorization_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


