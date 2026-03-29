# PaymentViewingInfoResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_viewed_date** | **datetime** | Data e hora da visualização da fatura | [optional] 
**boleto_viewed_date** | **datetime** | Data e hora da visualização do boleto | [optional] 

## Example

```python
from asaas.models.payment_viewing_info_response_dto import PaymentViewingInfoResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentViewingInfoResponseDTO from a JSON string
payment_viewing_info_response_dto_instance = PaymentViewingInfoResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentViewingInfoResponseDTO.to_json())

# convert the object into a dict
payment_viewing_info_response_dto_dict = payment_viewing_info_response_dto_instance.to_dict()
# create an instance of PaymentViewingInfoResponseDTO from a dict
payment_viewing_info_response_dto_from_dict = PaymentViewingInfoResponseDTO.from_dict(payment_viewing_info_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


