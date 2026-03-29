# PixRecurringTransactionGetItemResponseDTO

## Properties

| Name                           | Type                                                                                                                                                      | Description                                             | Notes      |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ---------- |
| **id**                         | **str**                                                                                                                                                   | Identificador único do item de uma recorrência no Asaas | [optional] |
| **status**                     | [**PixRecurringTransactionGetItemResponsePixRecurringTransactionItemStatus**](PixRecurringTransactionGetItemResponsePixRecurringTransactionItemStatus.md) |                                                         | [optional] |
| **scheduled_date**             | **date**                                                                                                                                                  | Data de agendamento do item de uma recorrência          | [optional] |
| **can_be_cancelled**           | **bool**                                                                                                                                                  | Indica se o item de uma recorrência pode ser cancelado  | [optional] |
| **recurrence_number**          | **int**                                                                                                                                                   | Número da recorrência                                   | [optional] |
| **quantity**                   | **int**                                                                                                                                                   | Quantidade de repetições                                | [optional] |
| **value**                      | **float**                                                                                                                                                 | Valor da recorrência                                    | [optional] |
| **refusal_reason_description** | **str**                                                                                                                                                   | Motivo pelo qual o item de uma recorrência foi recusado | [optional] |
| **external_account**           | [**PixRecurringTransactionExternalAccountDTO**](PixRecurringTransactionExternalAccountDTO.md)                                                             |                                                         | [optional] |

## Example

```python
from asaas.models.pix_recurring_transaction_get_item_response_dto import PixRecurringTransactionGetItemResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixRecurringTransactionGetItemResponseDTO from a JSON string
pix_recurring_transaction_get_item_response_dto_instance = PixRecurringTransactionGetItemResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixRecurringTransactionGetItemResponseDTO.to_json())

# convert the object into a dict
pix_recurring_transaction_get_item_response_dto_dict = pix_recurring_transaction_get_item_response_dto_instance.to_dict()
# create an instance of PixRecurringTransactionGetItemResponseDTO from a dict
pix_recurring_transaction_get_item_response_dto_from_dict = PixRecurringTransactionGetItemResponseDTO.from_dict(pix_recurring_transaction_get_item_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
