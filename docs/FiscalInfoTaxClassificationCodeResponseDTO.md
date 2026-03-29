# FiscalInfoTaxClassificationCodeResponseDTO

Lista de objetos

## Properties

| Name                             | Type                                                                                  | Description                                 | Notes      |
| -------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------- | ---------- |
| **code**                         | **str**                                                                               | Código da classificação tributária          | [optional] |
| **description**                  | **str**                                                                               | Descrição                                   | [optional] |
| **effective_start_date**         | **str**                                                                               | Data de início da vigência                  | [optional] |
| **expiration_date**              | **str**                                                                               | Data de término da vigência                 | [optional] |
| **is_subject_regular_taxation**  | **bool**                                                                              | Defina se está sujeito à tributação regular | [optional] |
| **cbs_percentage**               | **float**                                                                             | Alíquota do CBS                             | [optional] |
| **municipal_ibs_tax_percentage** | **float**                                                                             | Alíquota municipal do IBS                   | [optional] |
| **state_ibs_tax_percentage**     | **float**                                                                             | Alíquota estadual do IBS                    | [optional] |
| **cbs_tax_reduction_percentage** | **float**                                                                             | Percentual de redução da alíquota do CBS    | [optional] |
| **ibs_tax_reduction_percentage** | **float**                                                                             | Percentual de redução da alíquota do IBS    | [optional] |
| **tax_regime_type**              | **str**                                                                               | Tipo do regime de tributação                | [optional] |
| **tax_situation**                | [**FiscalInfoTaxSituationCodeResponseDTO**](FiscalInfoTaxSituationCodeResponseDTO.md) |                                             | [optional] |

## Example

```python
from asaas.models.fiscal_info_tax_classification_code_response_dto import FiscalInfoTaxClassificationCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoTaxClassificationCodeResponseDTO from a JSON string
fiscal_info_tax_classification_code_response_dto_instance = FiscalInfoTaxClassificationCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoTaxClassificationCodeResponseDTO.to_json())

# convert the object into a dict
fiscal_info_tax_classification_code_response_dto_dict = fiscal_info_tax_classification_code_response_dto_instance.to_dict()
# create an instance of FiscalInfoTaxClassificationCodeResponseDTO from a dict
fiscal_info_tax_classification_code_response_dto_from_dict = FiscalInfoTaxClassificationCodeResponseDTO.from_dict(fiscal_info_tax_classification_code_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
