# PaymentSimulateCreditCardResponseDTO

Taxas de cartão

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**net_value** | **float** | Valor liquido | [optional] 
**fee_percentage** | **float** | Taxa em porcentagem | [optional] 
**operation_fee** | **float** | Taxa de operação | [optional] 
**installment** | [**PaymentSimulateInstallmentResponseDTO**](PaymentSimulateInstallmentResponseDTO.md) |  | [optional] 

## Example

```python
from asaas.models.payment_simulate_credit_card_response_dto import PaymentSimulateCreditCardResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSimulateCreditCardResponseDTO from a JSON string
payment_simulate_credit_card_response_dto_instance = PaymentSimulateCreditCardResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSimulateCreditCardResponseDTO.to_json())

# convert the object into a dict
payment_simulate_credit_card_response_dto_dict = payment_simulate_credit_card_response_dto_instance.to_dict()
# create an instance of PaymentSimulateCreditCardResponseDTO from a dict
payment_simulate_credit_card_response_dto_from_dict = PaymentSimulateCreditCardResponseDTO.from_dict(payment_simulate_credit_card_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


