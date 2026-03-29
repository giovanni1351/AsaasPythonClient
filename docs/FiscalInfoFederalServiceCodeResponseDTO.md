# FiscalInfoFederalServiceCodeResponseDTO

Lista de objetos

## Properties

| Name            | Type    | Description       | Notes      |
| --------------- | ------- | ----------------- | ---------- |
| **code**        | **str** | Código tributário | [optional] |
| **description** | **str** | Descrição         | [optional] |

## Example

```python
from asaas.models.fiscal_info_federal_service_code_response_dto import FiscalInfoFederalServiceCodeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoFederalServiceCodeResponseDTO from a JSON string
fiscal_info_federal_service_code_response_dto_instance = FiscalInfoFederalServiceCodeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoFederalServiceCodeResponseDTO.to_json())

# convert the object into a dict
fiscal_info_federal_service_code_response_dto_dict = fiscal_info_federal_service_code_response_dto_instance.to_dict()
# create an instance of FiscalInfoFederalServiceCodeResponseDTO from a dict
fiscal_info_federal_service_code_response_dto_from_dict = FiscalInfoFederalServiceCodeResponseDTO.from_dict(fiscal_info_federal_service_code_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
