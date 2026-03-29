# PaymentDunningSimulateResponseTypeSimulationItemDTO

Simulação de solicitação de negativação para cada tipo de negativação disponível

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**PaymentDunningSimulateResponseTypeSimulationItemPaymentDunningType**](PaymentDunningSimulateResponseTypeSimulationItemPaymentDunningType.md) |  | [optional] 
**is_allowed** | **bool** | Se é possível solicitar uma negativação deste tipo | [optional] 
**not_allowed_reason** | **str** | Motivo por não ser possível solicitar uma negativação para este tipo | [optional] 
**fee_value** | **float** | Custo e/ou taxa da negativação | [optional] 
**net_value** | **float** | Valor líquido a ser recuperado | [optional] 
**start_date** | **str** | Data prevista de inicio da negativação | [optional] 

## Example

```python
from asaas.models.payment_dunning_simulate_response_type_simulation_item_dto import PaymentDunningSimulateResponseTypeSimulationItemDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningSimulateResponseTypeSimulationItemDTO from a JSON string
payment_dunning_simulate_response_type_simulation_item_dto_instance = PaymentDunningSimulateResponseTypeSimulationItemDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningSimulateResponseTypeSimulationItemDTO.to_json())

# convert the object into a dict
payment_dunning_simulate_response_type_simulation_item_dto_dict = payment_dunning_simulate_response_type_simulation_item_dto_instance.to_dict()
# create an instance of PaymentDunningSimulateResponseTypeSimulationItemDTO from a dict
payment_dunning_simulate_response_type_simulation_item_dto_from_dict = PaymentDunningSimulateResponseTypeSimulationItemDTO.from_dict(payment_dunning_simulate_response_type_simulation_item_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


