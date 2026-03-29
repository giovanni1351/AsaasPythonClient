# PaymentSimulateInstallmentResponseDTO

Informações de parcelamento

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_net_value** | **float** | Valor líquido | [optional] 
**payment_value** | **float** | Valor total | [optional] 

## Example

```python
from asaas.models.payment_simulate_installment_response_dto import PaymentSimulateInstallmentResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSimulateInstallmentResponseDTO from a JSON string
payment_simulate_installment_response_dto_instance = PaymentSimulateInstallmentResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSimulateInstallmentResponseDTO.to_json())

# convert the object into a dict
payment_simulate_installment_response_dto_dict = payment_simulate_installment_response_dto_instance.to_dict()
# create an instance of PaymentSimulateInstallmentResponseDTO from a dict
payment_simulate_installment_response_dto_from_dict = PaymentSimulateInstallmentResponseDTO.from_dict(payment_simulate_installment_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


