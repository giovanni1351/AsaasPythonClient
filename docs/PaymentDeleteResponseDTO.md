# PaymentDeleteResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** | Indica se a cobrança foi removida | [optional] 
**id** | **str** | Identificador único da cobrança no Asaas | [optional] 

## Example

```python
from asaas.models.payment_delete_response_dto import PaymentDeleteResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentDeleteResponseDTO from a JSON string
payment_delete_response_dto_instance = PaymentDeleteResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentDeleteResponseDTO.to_json())

# convert the object into a dict
payment_delete_response_dto_dict = payment_delete_response_dto_instance.to_dict()
# create an instance of PaymentDeleteResponseDTO from a dict
payment_delete_response_dto_from_dict = PaymentDeleteResponseDTO.from_dict(payment_delete_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


