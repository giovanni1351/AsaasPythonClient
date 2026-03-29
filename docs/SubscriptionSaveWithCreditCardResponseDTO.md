# SubscriptionSaveWithCreditCardResponseDTO

## Properties

| Name                   | Type                                                                                                                        | Description                                                             | Notes      |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ---------- |
| **object**             | **str**                                                                                                                     | Tipo do objeto                                                          | [optional] |
| **id**                 | **str**                                                                                                                     | Identificador único da assinatura no Asaas                              | [optional] |
| **date_created**       | **date**                                                                                                                    | Data de criação da assinatura                                           | [optional] |
| **customer**           | **str**                                                                                                                     | Identificador único do cliente                                          | [optional] |
| **payment_link**       | **str**                                                                                                                     | Identificador único do link de pagamentos ao qual a assinatura pertence | [optional] |
| **billing_type**       | [**SubscriptionSaveWithCreditCardResponseBillingType**](SubscriptionSaveWithCreditCardResponseBillingType.md)               |                                                                         | [optional] |
| **cycle**              | [**SubscriptionSaveWithCreditCardResponseCycle**](SubscriptionSaveWithCreditCardResponseCycle.md)                           |                                                                         | [optional] |
| **value**              | **float**                                                                                                                   | Valor da assinatura                                                     | [optional] |
| **next_due_date**      | **date**                                                                                                                    | Vencimento do próximo pagamento a ser gerado                            | [optional] |
| **end_date**           | **date**                                                                                                                    | Data limite para vencimento das cobranças                               | [optional] |
| **description**        | **str**                                                                                                                     | Descrição da assinatura                                                 | [optional] |
| **status**             | [**SubscriptionSaveWithCreditCardResponseSubscriptionStatus**](SubscriptionSaveWithCreditCardResponseSubscriptionStatus.md) |                                                                         | [optional] |
| **discount**           | [**PaymentDiscountDTO**](PaymentDiscountDTO.md)                                                                             |                                                                         | [optional] |
| **fine**               | [**PaymentFineResponseDTO**](PaymentFineResponseDTO.md)                                                                     |                                                                         | [optional] |
| **interest**           | [**PaymentInterestResponseDTO**](PaymentInterestResponseDTO.md)                                                             |                                                                         | [optional] |
| **deleted**            | **bool**                                                                                                                    | Informa se a assinatura foi removida                                    | [optional] |
| **max_payments**       | **int**                                                                                                                     | Número máximo de cobranças a serem geradas para esta assinatura         | [optional] |
| **external_reference** | **str**                                                                                                                     | Identificador da assinatura no seu sistema                              | [optional] |
| **checkout_session**   | **str**                                                                                                                     | Identificador único do checkout                                         | [optional] |
| **split**              | [**List[SubscriptionSplitResponseDTO]**](SubscriptionSplitResponseDTO.md)                                                   | Informações de split                                                    | [optional] |
| **credit_card**        | [**PaymentSaveWithCreditCardCreditCardDTO**](PaymentSaveWithCreditCardCreditCardDTO.md)                                     |                                                                         | [optional] |

## Example

```python
from asaas.models.subscription_save_with_credit_card_response_dto import SubscriptionSaveWithCreditCardResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionSaveWithCreditCardResponseDTO from a JSON string
subscription_save_with_credit_card_response_dto_instance = SubscriptionSaveWithCreditCardResponseDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionSaveWithCreditCardResponseDTO.to_json())

# convert the object into a dict
subscription_save_with_credit_card_response_dto_dict = subscription_save_with_credit_card_response_dto_instance.to_dict()
# create an instance of SubscriptionSaveWithCreditCardResponseDTO from a dict
subscription_save_with_credit_card_response_dto_from_dict = SubscriptionSaveWithCreditCardResponseDTO.from_dict(subscription_save_with_credit_card_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
