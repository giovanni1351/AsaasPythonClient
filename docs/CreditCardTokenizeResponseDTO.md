# CreditCardTokenizeResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**credit_card_number** | **str** | Últimos 4 dígitos do cartão utilizado | [optional] 
**credit_card_brand** | [**CreditCardTokenizeResponseCreditCardBrand**](CreditCardTokenizeResponseCreditCardBrand.md) |  | [optional] 
**credit_card_token** | **str** | Token do cartão de crédito que poderá ser enviado nas próximas transações sem a necessidade de informar novamente os dados de cartão e do titular | [optional] 

## Example

```python
from asaas.models.credit_card_tokenize_response_dto import CreditCardTokenizeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditCardTokenizeResponseDTO from a JSON string
credit_card_tokenize_response_dto_instance = CreditCardTokenizeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CreditCardTokenizeResponseDTO.to_json())

# convert the object into a dict
credit_card_tokenize_response_dto_dict = credit_card_tokenize_response_dto_instance.to_dict()
# create an instance of CreditCardTokenizeResponseDTO from a dict
credit_card_tokenize_response_dto_from_dict = CreditCardTokenizeResponseDTO.from_dict(credit_card_tokenize_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


