# SubscriptionGetResponseDTO

## Properties

| Name                   | Type                                                                                          | Description                                                             | Notes      |
| ---------------------- | --------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ---------- |
| **object**             | **str**                                                                                       | Tipo do objeto                                                          | [optional] |
| **id**                 | **str**                                                                                       | Identificador único da assinatura no Asaas                              | [optional] |
| **date_created**       | **date**                                                                                      | Data de criação da assinatura                                           | [optional] |
| **customer**           | **str**                                                                                       | Identificador único do cliente                                          | [optional] |
| **payment_link**       | **str**                                                                                       | Identificador único do link de pagamentos ao qual a assinatura pertence | [optional] |
| **billing_type**       | [**SubscriptionGetResponseBillingType**](SubscriptionGetResponseBillingType.md)               |                                                                         | [optional] |
| **cycle**              | [**SubscriptionGetResponseCycle**](SubscriptionGetResponseCycle.md)                           |                                                                         | [optional] |
| **value**              | **float**                                                                                     | Valor da assinatura                                                     | [optional] |
| **next_due_date**      | **date**                                                                                      | Vencimento do próximo pagamento a ser gerado                            | [optional] |
| **end_date**           | **date**                                                                                      | Data limite para vencimento das cobranças                               | [optional] |
| **description**        | **str**                                                                                       | Descrição da assinatura                                                 | [optional] |
| **status**             | [**SubscriptionGetResponseSubscriptionStatus**](SubscriptionGetResponseSubscriptionStatus.md) |                                                                         | [optional] |
| **discount**           | [**PaymentDiscountDTO**](PaymentDiscountDTO.md)                                               |                                                                         | [optional] |
| **fine**               | [**PaymentFineResponseDTO**](PaymentFineResponseDTO.md)                                       |                                                                         | [optional] |
| **interest**           | [**PaymentInterestResponseDTO**](PaymentInterestResponseDTO.md)                               |                                                                         | [optional] |
| **deleted**            | **bool**                                                                                      | Informa se a assinatura foi removida                                    | [optional] |
| **max_payments**       | **int**                                                                                       | Número máximo de cobranças a serem geradas para esta assinatura         | [optional] |
| **external_reference** | **str**                                                                                       | Identificador da assinatura no seu sistema                              | [optional] |
| **checkout_session**   | **str**                                                                                       | Identificador único do checkout                                         | [optional] |
| **split**              | [**List[SubscriptionSplitResponseDTO]**](SubscriptionSplitResponseDTO.md)                     | Informações de split                                                    | [optional] |

## Example

```python
from asaas.models.subscription_get_response_dto import SubscriptionGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionGetResponseDTO from a JSON string
subscription_get_response_dto_instance = SubscriptionGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionGetResponseDTO.to_json())

# convert the object into a dict
subscription_get_response_dto_dict = subscription_get_response_dto_instance.to_dict()
# create an instance of SubscriptionGetResponseDTO from a dict
subscription_get_response_dto_from_dict = SubscriptionGetResponseDTO.from_dict(subscription_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
