# PixRecurringTransactionGetResponseDTO

## Properties

| Name                 | Type                                                                                                                                            | Description                                 | Notes      |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- | ---------- |
| **id**               | **str**                                                                                                                                         | Identificador único da recorrência no Asaas | [optional] |
| **status**           | [**PixRecurringTransactionGetResponsePixRecurringTransactionStatus**](PixRecurringTransactionGetResponsePixRecurringTransactionStatus.md)       |                                             | [optional] |
| **origin**           | [**PixRecurringTransactionGetResponsePixRecurringTransactionOrigin**](PixRecurringTransactionGetResponsePixRecurringTransactionOrigin.md)       |                                             | [optional] |
| **value**            | **float**                                                                                                                                       | Valor da recorrência                        | [optional] |
| **frequency**        | [**PixRecurringTransactionGetResponsePixRecurringTransactionFrequency**](PixRecurringTransactionGetResponsePixRecurringTransactionFrequency.md) |                                             | [optional] |
| **quantity**         | **int**                                                                                                                                         | Quantidade de repetições                    | [optional] |
| **start_date**       | **date**                                                                                                                                        | Data inicial da recorrência                 | [optional] |
| **finish_date**      | **date**                                                                                                                                        | Data final da recorrência                   | [optional] |
| **can_be_cancelled** | **bool**                                                                                                                                        | Indica se a recorrência pode ser cancelada  | [optional] |
| **external_account** | [**PixRecurringTransactionExternalAccountDTO**](PixRecurringTransactionExternalAccountDTO.md)                                                   |                                             | [optional] |

## Example

```python
from asaas.models.pix_recurring_transaction_get_response_dto import PixRecurringTransactionGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixRecurringTransactionGetResponseDTO from a JSON string
pix_recurring_transaction_get_response_dto_instance = PixRecurringTransactionGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixRecurringTransactionGetResponseDTO.to_json())

# convert the object into a dict
pix_recurring_transaction_get_response_dto_dict = pix_recurring_transaction_get_response_dto_instance.to_dict()
# create an instance of PixRecurringTransactionGetResponseDTO from a dict
pix_recurring_transaction_get_response_dto_from_dict = PixRecurringTransactionGetResponseDTO.from_dict(pix_recurring_transaction_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
