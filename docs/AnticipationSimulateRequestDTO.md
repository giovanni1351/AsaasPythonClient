# AnticipationSimulateRequestDTO

## Properties

| Name            | Type    | Description                         | Notes      |
| --------------- | ------- | ----------------------------------- | ---------- |
| **installment** | **str** | ID do parcelamento a ser antecipado | [optional] |
| **payment**     | **str** | ID da cobrança a ser antecipada     | [optional] |

## Example

```python
from asaas.models.anticipation_simulate_request_dto import AnticipationSimulateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of AnticipationSimulateRequestDTO from a JSON string
anticipation_simulate_request_dto_instance = AnticipationSimulateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(AnticipationSimulateRequestDTO.to_json())

# convert the object into a dict
anticipation_simulate_request_dto_dict = anticipation_simulate_request_dto_instance.to_dict()
# create an instance of AnticipationSimulateRequestDTO from a dict
anticipation_simulate_request_dto_from_dict = AnticipationSimulateRequestDTO.from_dict(anticipation_simulate_request_dto_dict)
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
