# FiscalInfoTaxSituationCodeResponseDTO

Lista de objetos

## Properties

| Name                                     | Type     | Description                                            | Notes      |
| ---------------------------------------- | -------- | ------------------------------------------------------ | ---------- |
| **code**                                 | **str**  | Código da situação tributária                          | [optional] |
| **description**                          | **str**  | Descrição                                              | [optional] |
| **is_subject_to_ibs_cbs_taxation**       | **bool** | Define se está sujeito à tributação IBS e CBS          | [optional] |
| **is_base_reduction_percent_applicable** | **bool** | Define se a porcentagem de redução da base é aplicável | [optional] |
| **is_deferment_applicable**              | **bool** | Define se aplica-se diferimento                        | [optional] |

## Example

```python
from asaas.models.fiscal_info_tax_situation_code_response_dto import FiscalInfoTaxSituationCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoTaxSituationCodeResponseDTO from a JSON string
fiscal_info_tax_situation_code_response_dto_instance = FiscalInfoTaxSituationCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoTaxSituationCodeResponseDTO.to_json())

# convert the object into a dict
fiscal_info_tax_situation_code_response_dto_dict = fiscal_info_tax_situation_code_response_dto_instance.to_dict()
# create an instance of FiscalInfoTaxSituationCodeResponseDTO from a dict
fiscal_info_tax_situation_code_response_dto_from_dict = FiscalInfoTaxSituationCodeResponseDTO.from_dict(fiscal_info_tax_situation_code_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
