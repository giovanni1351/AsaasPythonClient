# BillSimulateRequestDTO

## Properties

| Name                     | Type    | Description                | Notes      |
| ------------------------ | ------- | -------------------------- | ---------- |
| **identification_field** | **str** | Linha digitável do boleto  | [optional] |
| **bar_code**             | **str** | Código de barras do boleto | [optional] |

## Example

```python
from asaas.models.bill_simulate_request_dto import BillSimulateRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of BillSimulateRequestDTO from a JSON string
bill_simulate_request_dto_instance = BillSimulateRequestDTO.from_json(json)
# print the JSON string representation of the object
print(BillSimulateRequestDTO.to_json())

# convert the object into a dict
bill_simulate_request_dto_dict = bill_simulate_request_dto_instance.to_dict()
# create an instance of BillSimulateRequestDTO from a dict
bill_simulate_request_dto_from_dict = BillSimulateRequestDTO.from_dict(bill_simulate_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
