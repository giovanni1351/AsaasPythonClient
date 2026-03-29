# BillSimulateResponseDTO

## Properties

| Name                      | Type                                                                              | Description                            | Notes      |
| ------------------------- | --------------------------------------------------------------------------------- | -------------------------------------- | ---------- |
| **minimum_schedule_date** | **date**                                                                          | Data mínima permitida para agendamento | [optional] |
| **fee**                   | **float**                                                                         | Taxa cobrada no pagamento da conta     | [optional] |
| **bank_slip_info**        | [**BillSimulateBankSlipInfoResponseDTO**](BillSimulateBankSlipInfoResponseDTO.md) |                                        | [optional] |

## Example

```python
from asaas.models.bill_simulate_response_dto import BillSimulateResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of BillSimulateResponseDTO from a JSON string
bill_simulate_response_dto_instance = BillSimulateResponseDTO.from_json(json)
# print the JSON string representation of the object
print(BillSimulateResponseDTO.to_json())

# convert the object into a dict
bill_simulate_response_dto_dict = bill_simulate_response_dto_instance.to_dict()
# create an instance of BillSimulateResponseDTO from a dict
bill_simulate_response_dto_from_dict = BillSimulateResponseDTO.from_dict(bill_simulate_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
