# TransferRecurringSaveRequestDTO

Informações da recorrência. Somente para transferências Pix

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**frequency** | [**TransferRecurringSaveRequestRecurringCheckoutScheduleFrequency**](TransferRecurringSaveRequestRecurringCheckoutScheduleFrequency.md) |  | [optional] 
**quantity** | **int** | Quantidade de repetições. Esta transferência será incluída como a primeira transação da recorrência.  Para a frequência &#x60;WEEKLY&#x60; o máximo aceito é: &#x60;51&#x60;  Para a frequência &#x60;MONTHLY&#x60; o máximo aceito é: &#x60;11&#x60; | [optional] 

## Example

```python
from asaas.models.transfer_recurring_save_request_dto import TransferRecurringSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferRecurringSaveRequestDTO from a JSON string
transfer_recurring_save_request_dto_instance = TransferRecurringSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(TransferRecurringSaveRequestDTO.to_json())

# convert the object into a dict
transfer_recurring_save_request_dto_dict = transfer_recurring_save_request_dto_instance.to_dict()
# create an instance of TransferRecurringSaveRequestDTO from a dict
transfer_recurring_save_request_dto_from_dict = TransferRecurringSaveRequestDTO.from_dict(transfer_recurring_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


