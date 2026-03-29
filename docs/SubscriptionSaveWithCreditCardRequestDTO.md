# SubscriptionSaveWithCreditCardRequestDTO

## Properties

| Name                        | Type                                                                                                        | Description                                                                                                                                      | Notes      |
| --------------------------- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- |
| **customer**                | **str**                                                                                                     | Identificador único do cliente no Asaas                                                                                                          |
| **billing_type**            | [**SubscriptionSaveWithCreditCardRequestBillingType**](SubscriptionSaveWithCreditCardRequestBillingType.md) |                                                                                                                                                  |
| **value**                   | **float**                                                                                                   | Valor da assinatura                                                                                                                              |
| **next_due_date**           | **date**                                                                                                    | Vencimento da primeira cobrança                                                                                                                  |
| **discount**                | [**PaymentDiscountDTO**](PaymentDiscountDTO.md)                                                             |                                                                                                                                                  | [optional] |
| **interest**                | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md)                                               |                                                                                                                                                  | [optional] |
| **fine**                    | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md)                                                       |                                                                                                                                                  | [optional] |
| **cycle**                   | [**SubscriptionSaveWithCreditCardRequestCycle**](SubscriptionSaveWithCreditCardRequestCycle.md)             |                                                                                                                                                  |
| **description**             | **str**                                                                                                     | Descrição da assinatura (máx. 500 caracteres)                                                                                                    | [optional] |
| **end_date**                | **date**                                                                                                    | Data limite para vencimento das cobranças                                                                                                        | [optional] |
| **max_payments**            | **int**                                                                                                     | Número máximo de cobranças a serem geradas para esta assinatura                                                                                  | [optional] |
| **external_reference**      | **str**                                                                                                     | Identificador da assinatura no seu sistema                                                                                                       | [optional] |
| **split**                   | [**List[SubscriptionSplitRequestDTO]**](SubscriptionSplitRequestDTO.md)                                     | Informações de split                                                                                                                             | [optional] |
| **callback**                | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md)                                               |                                                                                                                                                  | [optional] |
| **credit_card**             | [**CreditCardRequestDTO**](CreditCardRequestDTO.md)                                                         |                                                                                                                                                  |
| **credit_card_holder_info** | [**CreditCardHolderInfoRequestDTO**](CreditCardHolderInfoRequestDTO.md)                                     |                                                                                                                                                  |
| **credit_card_token**       | **str**                                                                                                     | Token do cartão de crédito para uso da funcionalidade de tokenização de cartão de crédito. Caso informado, os campos acima não são obrigatórios. | [optional] |
| **remote_ip**               | **str**                                                                                                     | IP de onde o cliente está fazendo a compra. Não deve ser informado o IP do seu servidor.                                                         |

## Example

```python
from asaas.models.subscription_save_with_credit_card_request_dto import SubscriptionSaveWithCreditCardRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionSaveWithCreditCardRequestDTO from a JSON string
subscription_save_with_credit_card_request_dto_instance = SubscriptionSaveWithCreditCardRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionSaveWithCreditCardRequestDTO.to_json())

# convert the object into a dict
subscription_save_with_credit_card_request_dto_dict = subscription_save_with_credit_card_request_dto_instance.to_dict()
# create an instance of SubscriptionSaveWithCreditCardRequestDTO from a dict
subscription_save_with_credit_card_request_dto_from_dict = SubscriptionSaveWithCreditCardRequestDTO.from_dict(subscription_save_with_credit_card_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
