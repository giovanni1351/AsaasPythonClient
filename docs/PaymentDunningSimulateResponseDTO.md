# PaymentDunningSimulateResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment** | **str** | Identificador único da cobrança a ser recuperada no Asaas | [optional] 
**value** | **float** | Valor da cobrança | [optional] 
**type_simulations** | [**List[PaymentDunningSimulateResponseTypeSimulationItemDTO]**](PaymentDunningSimulateResponseTypeSimulationItemDTO.md) | Simulação de solicitação de negativação para cada tipo de negativação disponível | [optional] 

## Example

```python
from asaas.models.payment_dunning_simulate_response_dto import PaymentDunningSimulateResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningSimulateResponseDTO from a JSON string
payment_dunning_simulate_response_dto_instance = PaymentDunningSimulateResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningSimulateResponseDTO.to_json())

# convert the object into a dict
payment_dunning_simulate_response_dto_dict = payment_dunning_simulate_response_dto_instance.to_dict()
# create an instance of PaymentDunningSimulateResponseDTO from a dict
payment_dunning_simulate_response_dto_from_dict = PaymentDunningSimulateResponseDTO.from_dict(payment_dunning_simulate_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


