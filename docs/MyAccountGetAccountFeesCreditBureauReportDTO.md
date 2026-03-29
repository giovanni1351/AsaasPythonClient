# MyAccountGetAccountFeesCreditBureauReportDTO

Taxas de consulta Serasa

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**natural_person_fee_value** | **float** | Taxa por consulta Serasa de pessoa física | [optional] 
**legal_person_fee_value** | **float** | Taxa por consulta Serasa de pessoa jurídica | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_credit_bureau_report_dto import MyAccountGetAccountFeesCreditBureauReportDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesCreditBureauReportDTO from a JSON string
my_account_get_account_fees_credit_bureau_report_dto_instance = MyAccountGetAccountFeesCreditBureauReportDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesCreditBureauReportDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_credit_bureau_report_dto_dict = my_account_get_account_fees_credit_bureau_report_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesCreditBureauReportDTO from a dict
my_account_get_account_fees_credit_bureau_report_dto_from_dict = MyAccountGetAccountFeesCreditBureauReportDTO.from_dict(my_account_get_account_fees_credit_bureau_report_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


