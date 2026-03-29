# PaymentSimulateRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | Valor total do parcelamento ou da cobrança | 
**installment_count** | **int** | Quantidade de parcelas | [optional] 
**billing_types** | [**List[PaymentSimulateRequestBillingType]**](PaymentSimulateRequestBillingType.md) | Forma de pagamento | 

## Example

```python
from asaas.models.payment_simulate_request_dto import PaymentSimulateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSimulateRequestDTO from a JSON string
payment_simulate_request_dto_instance = PaymentSimulateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSimulateRequestDTO.to_json())

# convert the object into a dict
payment_simulate_request_dto_dict = payment_simulate_request_dto_instance.to_dict()
# create an instance of PaymentSimulateRequestDTO from a dict
payment_simulate_request_dto_from_dict = PaymentSimulateRequestDTO.from_dict(payment_simulate_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


