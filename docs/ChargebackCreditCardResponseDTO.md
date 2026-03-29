# ChargebackCreditCardResponseDTO

Informações do cartão de crédito

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**number** | **str** | Últimos 4 dígitos do cartão utilizado | [optional] 
**brand** | [**ChargebackCreditCardResponseCreditCardBrand**](ChargebackCreditCardResponseCreditCardBrand.md) |  | [optional] 

## Example

```python
from asaas.models.chargeback_credit_card_response_dto import ChargebackCreditCardResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of ChargebackCreditCardResponseDTO from a JSON string
chargeback_credit_card_response_dto_instance = ChargebackCreditCardResponseDTO.from_json(json)
# print the JSON string representation of the object
print(ChargebackCreditCardResponseDTO.to_json())

# convert the object into a dict
chargeback_credit_card_response_dto_dict = chargeback_credit_card_response_dto_instance.to_dict()
# create an instance of ChargebackCreditCardResponseDTO from a dict
chargeback_credit_card_response_dto_from_dict = ChargebackCreditCardResponseDTO.from_dict(chargeback_credit_card_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


