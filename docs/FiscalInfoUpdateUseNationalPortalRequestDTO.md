# FiscalInfoUpdateUseNationalPortalRequestDTO

## Properties

| Name        | Type     | Description                                                                           | Notes |
| ----------- | -------- | ------------------------------------------------------------------------------------- | ----- |
| **enabled** | **bool** | Indica se a emissão de notas fiscais pelo portal nacional deve ser habilitada ou não. |

## Example

```python
from asaas.models.fiscal_info_update_use_national_portal_request_dto import FiscalInfoUpdateUseNationalPortalRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoUpdateUseNationalPortalRequestDTO from a JSON string
fiscal_info_update_use_national_portal_request_dto_instance = FiscalInfoUpdateUseNationalPortalRequestDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoUpdateUseNationalPortalRequestDTO.to_json())

# convert the object into a dict
fiscal_info_update_use_national_portal_request_dto_dict = fiscal_info_update_use_national_portal_request_dto_instance.to_dict()
# create an instance of FiscalInfoUpdateUseNationalPortalRequestDTO from a dict
fiscal_info_update_use_national_portal_request_dto_from_dict = FiscalInfoUpdateUseNationalPortalRequestDTO.from_dict(fiscal_info_update_use_national_portal_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
