# MyAccountGetAccountFeesResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment** | [**MyAccountGetAccountFeesPaymentDTO**](MyAccountGetAccountFeesPaymentDTO.md) |  | [optional] 
**transfer** | [**MyAccountGetAccountFeesTransferDTO**](MyAccountGetAccountFeesTransferDTO.md) |  | [optional] 
**notification** | [**MyAccountGetAccountFeesNotificationDTO**](MyAccountGetAccountFeesNotificationDTO.md) |  | [optional] 
**credit_bureau_report** | [**MyAccountGetAccountFeesCreditBureauReportDTO**](MyAccountGetAccountFeesCreditBureauReportDTO.md) |  | [optional] 
**payment_dunning** | [**MyAccountGetAccountFeesPaymentDunningDTO**](MyAccountGetAccountFeesPaymentDunningDTO.md) |  | [optional] 
**invoice** | [**MyAccountGetAccountFeesInvoiceDTO**](MyAccountGetAccountFeesInvoiceDTO.md) |  | [optional] 
**anticipation** | [**MyAccountGetAccountFeesAnticipationDTO**](MyAccountGetAccountFeesAnticipationDTO.md) |  | [optional] 

## Example

```python
from asaas.models.my_account_get_account_fees_response_dto import MyAccountGetAccountFeesResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of MyAccountGetAccountFeesResponseDTO from a JSON string
my_account_get_account_fees_response_dto_instance = MyAccountGetAccountFeesResponseDTO.from_json(json)
# print the JSON string representation of the object
print(MyAccountGetAccountFeesResponseDTO.to_json())

# convert the object into a dict
my_account_get_account_fees_response_dto_dict = my_account_get_account_fees_response_dto_instance.to_dict()
# create an instance of MyAccountGetAccountFeesResponseDTO from a dict
my_account_get_account_fees_response_dto_from_dict = MyAccountGetAccountFeesResponseDTO.from_dict(my_account_get_account_fees_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


