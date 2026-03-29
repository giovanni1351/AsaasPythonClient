# AnticipationLimitsInfoResponseDTO

Limites de antecipação de cartão de crédito

## Properties

| Name          | Type      | Description                             | Notes      |
| ------------- | --------- | --------------------------------------- | ---------- |
| **total**     | **float** | Limite de antecipação liberado na conta | [optional] |
| **available** | **float** | Limite disponível para antecipar        | [optional] |

## Example

```python
from asaas.models.anticipation_limits_info_response_dto import AnticipationLimitsInfoResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationLimitsInfoResponseDTO from a JSON string
anticipation_limits_info_response_dto_instance = AnticipationLimitsInfoResponseDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationLimitsInfoResponseDTO.to_json())

# convert the object into a dict
anticipation_limits_info_response_dto_dict = anticipation_limits_info_response_dto_instance.to_dict()
# create an instance of AnticipationLimitsInfoResponseDTO from a dict
anticipation_limits_info_response_dto_from_dict = AnticipationLimitsInfoResponseDTO.from_dict(anticipation_limits_info_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
