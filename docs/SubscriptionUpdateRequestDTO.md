# SubscriptionUpdateRequestDTO

## Properties

| Name                        | Type                                                                                              | Description                                                                        | Notes      |
| --------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------- |
| **billing_type**            | [**SubscriptionUpdateRequestBillingType**](SubscriptionUpdateRequestBillingType.md)               |                                                                                    | [optional] |
| **status**                  | [**SubscriptionUpdateRequestSubscriptionStatus**](SubscriptionUpdateRequestSubscriptionStatus.md) |                                                                                    | [optional] |
| **next_due_date**           | **date**                                                                                          | Vencimento da primeira cobrança                                                    | [optional] |
| **discount**                | [**PaymentDiscountDTO**](PaymentDiscountDTO.md)                                                   |                                                                                    | [optional] |
| **interest**                | [**PaymentInterestRequestDTO**](PaymentInterestRequestDTO.md)                                     |                                                                                    | [optional] |
| **fine**                    | [**PaymentFineRequestDTO**](PaymentFineRequestDTO.md)                                             |                                                                                    | [optional] |
| **cycle**                   | [**SubscriptionUpdateRequestCycle**](SubscriptionUpdateRequestCycle.md)                           |                                                                                    | [optional] |
| **description**             | **str**                                                                                           | Descrição da assinatura (máx. 500 caracteres)                                      | [optional] |
| **end_date**                | **date**                                                                                          | Data limite para vencimento das cobranças                                          | [optional] |
| **update_pending_payments** | **bool**                                                                                          | true para atualizar as propriedades possíveis de cobranças pendentes já existentes | [optional] |
| **external_reference**      | **str**                                                                                           | Identificador da assinatura no seu sistema                                         | [optional] |
| **split**                   | [**List[SubscriptionSplitRequestDTO]**](SubscriptionSplitRequestDTO.md)                           | Informações de split                                                               | [optional] |
| **callback**                | [**PaymentCallbackRequestDTO**](PaymentCallbackRequestDTO.md)                                     |                                                                                    | [optional] |

## Example

```python
from asaas.models.subscription_update_request_dto import SubscriptionUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionUpdateRequestDTO from a JSON string
subscription_update_request_dto_instance = SubscriptionUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(SubscriptionUpdateRequestDTO.to_json())

# convert the object into a dict
subscription_update_request_dto_dict = subscription_update_request_dto_instance.to_dict()
# create an instance of SubscriptionUpdateRequestDTO from a dict
subscription_update_request_dto_from_dict = SubscriptionUpdateRequestDTO.from_dict(subscription_update_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
