# CreditCardRequestDTO

Informações do cartão de crédito

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**holder_name** | **str** | Nome impresso no cartão | 
**number** | **str** | Número do cartão | 
**expiry_month** | **str** | Mês de expiração com 2 dígitos | 
**expiry_year** | **str** | Ano de expiração com 4 dígitos | 
**ccv** | **str** | Código de segurança | 

## Example

```python
from asaas.models.credit_card_request_dto import CreditCardRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditCardRequestDTO from a JSON string
credit_card_request_dto_instance = CreditCardRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CreditCardRequestDTO.to_json())

# convert the object into a dict
credit_card_request_dto_dict = credit_card_request_dto_instance.to_dict()
# create an instance of CreditCardRequestDTO from a dict
credit_card_request_dto_from_dict = CreditCardRequestDTO.from_dict(credit_card_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


