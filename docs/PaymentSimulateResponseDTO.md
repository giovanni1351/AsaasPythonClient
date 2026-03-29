# PaymentSimulateResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | Valor total do parcelamento ou da cobrança | [optional] 
**credit_card** | [**PaymentSimulateCreditCardResponseDTO**](PaymentSimulateCreditCardResponseDTO.md) |  | [optional] 
**bank_slip** | [**PaymentSimulateBankSlipResponseDTO**](PaymentSimulateBankSlipResponseDTO.md) |  | [optional] 
**pix** | [**PaymentSimulatePixResponseDTO**](PaymentSimulatePixResponseDTO.md) |  | [optional] 

## Example

```python
from asaas.models.payment_simulate_response_dto import PaymentSimulateResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSimulateResponseDTO from a JSON string
payment_simulate_response_dto_instance = PaymentSimulateResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSimulateResponseDTO.to_json())

# convert the object into a dict
payment_simulate_response_dto_dict = payment_simulate_response_dto_instance.to_dict()
# create an instance of PaymentSimulateResponseDTO from a dict
payment_simulate_response_dto_from_dict = PaymentSimulateResponseDTO.from_dict(payment_simulate_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


