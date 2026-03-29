# PaymentIdentificationFieldResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identification_field** | **str** | Linha digitável do boleto | [optional] 
**nosso_numero** | **str** | Número de identificação do boleto | [optional] 
**bar_code** | **str** | Código de barras do boleto | [optional] 

## Example

```python
from asaas.models.payment_identification_field_response_dto import PaymentIdentificationFieldResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentIdentificationFieldResponseDTO from a JSON string
payment_identification_field_response_dto_instance = PaymentIdentificationFieldResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentIdentificationFieldResponseDTO.to_json())

# convert the object into a dict
payment_identification_field_response_dto_dict = payment_identification_field_response_dto_instance.to_dict()
# create an instance of PaymentIdentificationFieldResponseDTO from a dict
payment_identification_field_response_dto_from_dict = PaymentIdentificationFieldResponseDTO.from_dict(payment_identification_field_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


