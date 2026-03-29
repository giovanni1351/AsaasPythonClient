# AnticipationConfigurationGetResponseDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**credit_card_automatic_enabled** | **bool** | Indica se a antecipação automática de cartão de crédito está habilitada | [optional] 

## Example

```python
from asaas.models.anticipation_configuration_get_response_dto import AnticipationConfigurationGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationConfigurationGetResponseDTO from a JSON string
anticipation_configuration_get_response_dto_instance = AnticipationConfigurationGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationConfigurationGetResponseDTO.to_json())

# convert the object into a dict
anticipation_configuration_get_response_dto_dict = anticipation_configuration_get_response_dto_instance.to_dict()
# create an instance of AnticipationConfigurationGetResponseDTO from a dict
anticipation_configuration_get_response_dto_from_dict = AnticipationConfigurationGetResponseDTO.from_dict(anticipation_configuration_get_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


