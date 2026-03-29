# PixTransactionSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**qr_code** | [**PixTransactionQrCodeSaveRequestDTO**](PixTransactionQrCodeSaveRequestDTO.md) |  | 
**value** | **float** | Valor a ser pago | 
**description** | **str** | Descrição do pagamento | [optional] 
**schedule_date** | **date** | Utilizada para realizar agendamento do pagamento | [optional] 

## Example

```python
from asaas.models.pix_transaction_save_request_dto import PixTransactionSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTransactionSaveRequestDTO from a JSON string
pix_transaction_save_request_dto_instance = PixTransactionSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixTransactionSaveRequestDTO.to_json())

# convert the object into a dict
pix_transaction_save_request_dto_dict = pix_transaction_save_request_dto_instance.to_dict()
# create an instance of PixTransactionSaveRequestDTO from a dict
pix_transaction_save_request_dto_from_dict = PixTransactionSaveRequestDTO.from_dict(pix_transaction_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


