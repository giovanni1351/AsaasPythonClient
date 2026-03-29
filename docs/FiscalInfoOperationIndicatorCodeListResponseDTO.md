# FiscalInfoOperationIndicatorCodeListResponseDTO

## Properties

| Name            | Type                                                                                                    | Description                                                    | Notes      |
| --------------- | ------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ---------- |
| **object**      | **str**                                                                                                 | Tipo de objeto                                                 | [optional] |
| **has_more**    | **bool**                                                                                                | Indica se há mais uma página a ser buscada                     | [optional] |
| **total_count** | **int**                                                                                                 | Quantidade total de itens para os filtros informados           | [optional] |
| **limit**       | **int**                                                                                                 | Quantidade de objetos por página                               | [optional] |
| **offset**      | **int**                                                                                                 | Posição do objeto a partir do qual a página deve ser carregada | [optional] |
| **data**        | [**List[FiscalInfoOperationIndicatorCodeResponseDTO]**](FiscalInfoOperationIndicatorCodeResponseDTO.md) | Lista de objetos                                               | [optional] |

## Example

```python
from asaas.models.fiscal_info_operation_indicator_code_list_response_dto import FiscalInfoOperationIndicatorCodeListResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoOperationIndicatorCodeListResponseDTO from a JSON string
fiscal_info_operation_indicator_code_list_response_dto_instance = FiscalInfoOperationIndicatorCodeListResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoOperationIndicatorCodeListResponseDTO.to_json())

# convert the object into a dict
fiscal_info_operation_indicator_code_list_response_dto_dict = fiscal_info_operation_indicator_code_list_response_dto_instance.to_dict()
# create an instance of FiscalInfoOperationIndicatorCodeListResponseDTO from a dict
fiscal_info_operation_indicator_code_list_response_dto_from_dict = FiscalInfoOperationIndicatorCodeListResponseDTO.from_dict(fiscal_info_operation_indicator_code_list_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
