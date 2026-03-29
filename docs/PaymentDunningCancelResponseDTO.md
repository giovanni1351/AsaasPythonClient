# PaymentDunningCancelResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Identificador único da negativação no Asaas | [optional] 
**dunning_number** | **int** | Número da negativação | [optional] 
**status** | [**PaymentDunningCancelResponsePaymentDunningStatus**](PaymentDunningCancelResponsePaymentDunningStatus.md) |  | [optional] 
**type** | [**PaymentDunningCancelResponsePaymentDunningType**](PaymentDunningCancelResponsePaymentDunningType.md) |  | [optional] 
**payment** | **str** | Identificador único da cobrança a ser recuperada no Asaas | [optional] 
**request_date** | **date** | Data de solicitação | [optional] 
**description** | **str** | Descrição da negativação | [optional] 
**value** | **float** | Valor da cobrança | [optional] 
**fee_value** | **float** | Custo e/ou taxa da negativação | [optional] 
**net_value** | **float** | Valor líquido a ser recuperado | [optional] 
**received_in_cash_fee_value** | **float** | Taxa de recebimento em dinheiro | [optional] 
**denial_reason** | **str** | Motivo da negação da negativação | [optional] 
**cancellation_fee_value** | **float** | Taxa cobrada em caso de cancelamento | [optional] 
**can_be_cancelled** | **bool** | Se a negativação pode ser cancelada | [optional] [default to True]
**cannot_be_cancelled_reason** | **str** | Motivo de não ser possível solicitar o cancelamento | [optional] 
**is_necessary_resend_documentation** | **bool** | Determina se é preciso reenviar a documentação | [optional] 

## Example

```python
from asaas.models.payment_dunning_cancel_response_dto import PaymentDunningCancelResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningCancelResponseDTO from a JSON string
payment_dunning_cancel_response_dto_instance = PaymentDunningCancelResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningCancelResponseDTO.to_json())

# convert the object into a dict
payment_dunning_cancel_response_dto_dict = payment_dunning_cancel_response_dto_instance.to_dict()
# create an instance of PaymentDunningCancelResponseDTO from a dict
payment_dunning_cancel_response_dto_from_dict = PaymentDunningCancelResponseDTO.from_dict(payment_dunning_cancel_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


