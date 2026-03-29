# PixRecurringTransactionListResponseDTO

## Properties

| Name            | Type                                                                                        | Description                                                    | Notes      |
| --------------- | ------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ---------- |
| **object**      | **str**                                                                                     | Tipo de objeto                                                 | [optional] |
| **has_more**    | **bool**                                                                                    | Indica se há mais uma página a ser buscada                     | [optional] |
| **total_count** | **int**                                                                                     | Quantidade total de itens para os filtros informados           | [optional] |
| **limit**       | **int**                                                                                     | Quantidade de objetos por página                               | [optional] |
| **offset**      | **int**                                                                                     | Posição do objeto a partir do qual a página deve ser carregada | [optional] |
| **data**        | [**List[PixRecurringTransactionGetResponseDTO]**](PixRecurringTransactionGetResponseDTO.md) | Lista de objetos                                               | [optional] |

## Example

```python
from asaas.models.pix_recurring_transaction_list_response_dto import PixRecurringTransactionListResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixRecurringTransactionListResponseDTO from a JSON string
pix_recurring_transaction_list_response_dto_instance = PixRecurringTransactionListResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixRecurringTransactionListResponseDTO.to_json())

# convert the object into a dict
pix_recurring_transaction_list_response_dto_dict = pix_recurring_transaction_list_response_dto_instance.to_dict()
# create an instance of PixRecurringTransactionListResponseDTO from a dict
pix_recurring_transaction_list_response_dto_from_dict = PixRecurringTransactionListResponseDTO.from_dict(pix_recurring_transaction_list_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
