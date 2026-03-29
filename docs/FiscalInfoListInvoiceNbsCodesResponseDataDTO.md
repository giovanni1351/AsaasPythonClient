# FiscalInfoListInvoiceNbsCodesResponseDataDTO

Lista de objetos

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**nbs_code** | **str** | Código NBS (Nomenclatura Brasileira de Serviços) | [optional] 
**code_description** | **str** | Código NBS e descrição | [optional] 

## Example

```python
from asaas.models.fiscal_info_list_invoice_nbs_codes_response_data_dto import FiscalInfoListInvoiceNbsCodesResponseDataDTO

# TODO update the JSON string below
json = "{}"
# create an instance of FiscalInfoListInvoiceNbsCodesResponseDataDTO from a JSON string
fiscal_info_list_invoice_nbs_codes_response_data_dto_instance = FiscalInfoListInvoiceNbsCodesResponseDataDTO.from_json(json)
# print the JSON string representation of the object
print(FiscalInfoListInvoiceNbsCodesResponseDataDTO.to_json())

# convert the object into a dict
fiscal_info_list_invoice_nbs_codes_response_data_dto_dict = fiscal_info_list_invoice_nbs_codes_response_data_dto_instance.to_dict()
# create an instance of FiscalInfoListInvoiceNbsCodesResponseDataDTO from a dict
fiscal_info_list_invoice_nbs_codes_response_data_dto_from_dict = FiscalInfoListInvoiceNbsCodesResponseDataDTO.from_dict(fiscal_info_list_invoice_nbs_codes_response_data_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


