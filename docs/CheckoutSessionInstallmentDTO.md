# CheckoutSessionInstallmentDTO

Detalhes do parcelamento. Caso informado, será obrigatório incluir o chargeType `INSTALLMENT`

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**max_installment_count** | **int** | Número máximo de parcelas | [optional] 

## Example

```python
from asaas.models.checkout_session_installment_dto import CheckoutSessionInstallmentDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionInstallmentDTO from a JSON string
checkout_session_installment_dto_instance = CheckoutSessionInstallmentDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionInstallmentDTO.to_json())

# convert the object into a dict
checkout_session_installment_dto_dict = checkout_session_installment_dto_instance.to_dict()
# create an instance of CheckoutSessionInstallmentDTO from a dict
checkout_session_installment_dto_from_dict = CheckoutSessionInstallmentDTO.from_dict(checkout_session_installment_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


