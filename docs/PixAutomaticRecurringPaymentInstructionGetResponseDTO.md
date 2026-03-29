# PixAutomaticRecurringPaymentInstructionGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da instrução de pagamento de Pix Automático no Asaas | [optional] 
**end_to_end_identifier** | **str** | Identificador fim a fim | [optional] 
**authorization** | [**PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO**](PixAutomaticRecurringPaymentInstructionAuthorizationResponseDTO.md) |  | [optional] 
**due_date** | **date** | Data de vencimento da instrução de pagamento | [optional] 
**status** | **str** | Status da instrução de pagamento | [optional] 
**payment_id** | **str** | Identificador único da cobrança vinculada | [optional] 
**refusal_reason** | **str** | Motivo pelo qual a instrução de pagamento foi recusada | [optional] 

## Example

```python
from asaas.models.pix_automatic_recurring_payment_instruction_get_response_dto import PixAutomaticRecurringPaymentInstructionGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixAutomaticRecurringPaymentInstructionGetResponseDTO from a JSON string
pix_automatic_recurring_payment_instruction_get_response_dto_instance = PixAutomaticRecurringPaymentInstructionGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixAutomaticRecurringPaymentInstructionGetResponseDTO.to_json())

# convert the object into a dict
pix_automatic_recurring_payment_instruction_get_response_dto_dict = pix_automatic_recurring_payment_instruction_get_response_dto_instance.to_dict()
# create an instance of PixAutomaticRecurringPaymentInstructionGetResponseDTO from a dict
pix_automatic_recurring_payment_instruction_get_response_dto_from_dict = PixAutomaticRecurringPaymentInstructionGetResponseDTO.from_dict(pix_automatic_recurring_payment_instruction_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


