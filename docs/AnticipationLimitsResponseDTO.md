# AnticipationLimitsResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**credit_card** | [**AnticipationLimitsInfoResponseDTO**](AnticipationLimitsInfoResponseDTO.md) |  | [optional] 
**bank_slip** | [**AnticipationLimitsInfoResponseDTO**](AnticipationLimitsInfoResponseDTO.md) |  | [optional] 

## Example

```python
from asaas.models.anticipation_limits_response_dto import AnticipationLimitsResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationLimitsResponseDTO from a JSON string
anticipation_limits_response_dto_instance = AnticipationLimitsResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationLimitsResponseDTO.to_json())

# convert the object into a dict
anticipation_limits_response_dto_dict = anticipation_limits_response_dto_instance.to_dict()
# create an instance of AnticipationLimitsResponseDTO from a dict
anticipation_limits_response_dto_from_dict = AnticipationLimitsResponseDTO.from_dict(anticipation_limits_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


