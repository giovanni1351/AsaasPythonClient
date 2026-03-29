# CreditBureauReportSaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer** | **str** | Identificador único do cliente no Asaas | [optional] 
**cpf_cnpj** | **str** | CPF ou CNPJ do cliente. Informe este campo caso seu cliente não esteja cadastrado no Asaas | [optional] 

## Example

```python
from asaas.models.credit_bureau_report_save_request_dto import CreditBureauReportSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditBureauReportSaveRequestDTO from a JSON string
credit_bureau_report_save_request_dto_instance = CreditBureauReportSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(CreditBureauReportSaveRequestDTO.to_json())

# convert the object into a dict
credit_bureau_report_save_request_dto_dict = credit_bureau_report_save_request_dto_instance.to_dict()
# create an instance of CreditBureauReportSaveRequestDTO from a dict
credit_bureau_report_save_request_dto_from_dict = CreditBureauReportSaveRequestDTO.from_dict(credit_bureau_report_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


