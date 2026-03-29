# PaymentDunningPaymentsAvailableForDunningResponseDataDTO

Lista de objetos

## Properties

| Name                 | Type                                                                                                                                                                  | Description                                                                      | Notes      |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ---------- |
| **payment**          | **str**                                                                                                                                                               | Identificador único da cobrança a ser recuperada no Asaas                        | [optional] |
| **customer**         | **str**                                                                                                                                                               | Identificador único do cliente                                                   | [optional] |
| **value**            | **float**                                                                                                                                                             | Valor da cobrança                                                                | [optional] |
| **status**           | [**PaymentDunningPaymentsAvailableForDunningResponseDataPaymentStatus**](PaymentDunningPaymentsAvailableForDunningResponseDataPaymentStatus.md)                       |                                                                                  | [optional] |
| **billing_type**     | [**PaymentDunningPaymentsAvailableForDunningResponseDataBillingType**](PaymentDunningPaymentsAvailableForDunningResponseDataBillingType.md)                           |                                                                                  | [optional] |
| **due_date**         | **str**                                                                                                                                                               | Data de vencimento                                                               | [optional] |
| **type_simulations** | [**List[PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO]**](PaymentDunningPaymentsAvailableForDunningResponseDataTypeSimulationItemDTO.md) | Simulação de solicitação de negativação para cada tipo de negativação disponível | [optional] |

## Example

```python
from asaas.models.payment_dunning_payments_available_for_dunning_response_data_dto import PaymentDunningPaymentsAvailableForDunningResponseDataDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDunningPaymentsAvailableForDunningResponseDataDTO from a JSON string
payment_dunning_payments_available_for_dunning_response_data_dto_instance = PaymentDunningPaymentsAvailableForDunningResponseDataDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDunningPaymentsAvailableForDunningResponseDataDTO.to_json())

# convert the object into a dict
payment_dunning_payments_available_for_dunning_response_data_dto_dict = payment_dunning_payments_available_for_dunning_response_data_dto_instance.to_dict()
# create an instance of PaymentDunningPaymentsAvailableForDunningResponseDataDTO from a dict
payment_dunning_payments_available_for_dunning_response_data_dto_from_dict = PaymentDunningPaymentsAvailableForDunningResponseDataDTO.from_dict(payment_dunning_payments_available_for_dunning_response_data_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
