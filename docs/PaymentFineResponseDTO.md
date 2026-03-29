# PaymentFineResponseDTO

Informações de multa para pagamento após o vencimento

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** | Valor da multa em porcentagem | [optional] 

## Example

```python
from asaas.models.payment_fine_response_dto import PaymentFineResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentFineResponseDTO from a JSON string
payment_fine_response_dto_instance = PaymentFineResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentFineResponseDTO.to_json())

# convert the object into a dict
payment_fine_response_dto_dict = payment_fine_response_dto_instance.to_dict()
# create an instance of PaymentFineResponseDTO from a dict
payment_fine_response_dto_from_dict = PaymentFineResponseDTO.from_dict(payment_fine_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


