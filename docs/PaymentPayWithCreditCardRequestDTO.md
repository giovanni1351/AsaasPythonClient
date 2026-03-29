# PaymentPayWithCreditCardRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**credit_card** | [**CreditCardRequestDTO**](CreditCardRequestDTO.md) |  | 
**credit_card_holder_info** | [**CreditCardHolderInfoRequestDTO**](CreditCardHolderInfoRequestDTO.md) |  | 
**credit_card_token** | **str** | Token do cartão de crédito para uso da funcionalidade de tokenização de cartão de crédito. Caso informado, os campos acima não são obrigatórios. | [optional] 

## Example

```python
from asaas.models.payment_pay_with_credit_card_request_dto import PaymentPayWithCreditCardRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentPayWithCreditCardRequestDTO from a JSON string
payment_pay_with_credit_card_request_dto_instance = PaymentPayWithCreditCardRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentPayWithCreditCardRequestDTO.to_json())

# convert the object into a dict
payment_pay_with_credit_card_request_dto_dict = payment_pay_with_credit_card_request_dto_instance.to_dict()
# create an instance of PaymentPayWithCreditCardRequestDTO from a dict
payment_pay_with_credit_card_request_dto_from_dict = PaymentPayWithCreditCardRequestDTO.from_dict(payment_pay_with_credit_card_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


