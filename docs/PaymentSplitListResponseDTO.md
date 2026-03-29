# PaymentSplitListResponseDTO

## Properties

| Name            | Type                                                                          | Description                                                    | Notes      |
| --------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------- | ---------- |
| **object**      | **str**                                                                       | Tipo de objeto                                                 | [optional] |
| **has_more**    | **bool**                                                                      | Indica se há mais uma página a ser buscada                     | [optional] |
| **total_count** | **int**                                                                       | Quantidade total de itens para os filtros informados           | [optional] |
| **limit**       | **int**                                                                       | Quantidade de objetos por página                               | [optional] |
| **offset**      | **int**                                                                       | Posição do objeto a partir do qual a página deve ser carregada | [optional] |
| **data**        | [**List[PaymentSplitGetFullResponseDTO]**](PaymentSplitGetFullResponseDTO.md) | Lista de objetos                                               | [optional] |

## Example

```python
from asaas.models.payment_split_list_response_dto import PaymentSplitListResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentSplitListResponseDTO from a JSON string
payment_split_list_response_dto_instance = PaymentSplitListResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentSplitListResponseDTO.to_json())

# convert the object into a dict
payment_split_list_response_dto_dict = payment_split_list_response_dto_instance.to_dict()
# create an instance of PaymentSplitListResponseDTO from a dict
payment_split_list_response_dto_from_dict = PaymentSplitListResponseDTO.from_dict(payment_split_list_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
