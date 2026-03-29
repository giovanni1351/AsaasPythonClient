# PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO

Simulação de solicitação de negativação para cada tipo de negativação disponível

## Properties

| Name                   | Type                                                                                                                                                                                          | Description                                                          | Notes                        |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ---------------------------- |
| **type**               | [**PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemPaymentDunningType**](PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemPaymentDunningType.md) |                                                                      | [optional]                   |
| **is_allowed**         | **bool**                                                                                                                                                                                      | Se é possível solicitar uma negativação deste tipo                   | [optional] [default to True] |
| **not_allowed_reason** | **str**                                                                                                                                                                                       | Motivo por não ser possível solicitar uma negativação para este tipo | [optional]                   |
| **fee_value**          | **float**                                                                                                                                                                                     | Custo e/ou taxa da negativação                                       | [optional]                   |
| **net_value**          | **float**                                                                                                                                                                                     | Valor líquido a ser recuperado                                       | [optional]                   |
| **start_date**         | **str**                                                                                                                                                                                       | Data prevista de inicio da negativação                               | [optional]                   |

## Example

```python
from asaas.models.payment_dunning_payments_available_for_dunning_response_data_type_simulation_item_dto import PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO from a JSON string
payment_dunning_payments_available_for_dunning_response_data_type_simulation_item_dto_instance = PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO.to_json())

# convert the object into a dict
payment_dunning_payments_available_for_dunning_response_data_type_simulation_item_dto_dict = payment_dunning_payments_available_for_dunning_response_data_type_simulation_item_dto_instance.to_dict()
# create an instance of PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO from a dict
payment_dunning_payments_available_for_dunning_response_data_type_simulation_item_dto_from_dict = PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO.from_dict(payment_dunning_payments_available_for_dunning_response_data_type_simulation_item_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
