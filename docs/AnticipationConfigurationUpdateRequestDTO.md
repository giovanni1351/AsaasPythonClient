# AnticipationConfigurationUpdateRequestDTO

## Properties

| Name                              | Type     | Description                                    | Notes      |
| --------------------------------- | -------- | ---------------------------------------------- | ---------- |
| **credit_card_automatic_enabled** | **bool** | Definir configuração de antecipação automática | [optional] |

## Example

```python
from asaas.models.anticipation_configuration_update_request_dto import AnticipationConfigurationUpdateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationConfigurationUpdateRequestDTO from a JSON string
anticipation_configuration_update_request_dto_instance = AnticipationConfigurationUpdateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationConfigurationUpdateRequestDTO.to_json())

# convert the object into a dict
anticipation_configuration_update_request_dto_dict = anticipation_configuration_update_request_dto_instance.to_dict()
# create an instance of AnticipationConfigurationUpdateRequestDTO from a dict
anticipation_configuration_update_request_dto_from_dict = AnticipationConfigurationUpdateRequestDTO.from_dict(anticipation_configuration_update_request_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
