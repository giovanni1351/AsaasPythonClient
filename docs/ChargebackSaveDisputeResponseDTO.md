# ChargebackSaveDisputeResponseDTO

## Properties

| Name              | Type                                                                                                                | Description                                                          | Notes      |
| ----------------- | ------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ---------- |
| **chargeback_id** | **str**                                                                                                             | Identificador único do chargeback para o qual a disputa será criada. | [optional] |
| **status**        | [**ChargebackSaveDisputeResponseChargebackDisputeStatus**](ChargebackSaveDisputeResponseChargebackDisputeStatus.md) |                                                                      | [optional] |
| **files**         | **List[str]**                                                                                                       | Nome dos arquivos enviados para a disputa.                           | [optional] |

## Example

```python
from asaas.models.chargeback_save_dispute_response_dto import ChargebackSaveDisputeResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of ChargebackSaveDisputeResponseDTO from a JSON string
chargeback_save_dispute_response_dto_instance = ChargebackSaveDisputeResponseDTO.from_json(json)
# print the JSON string representation of the object
print(ChargebackSaveDisputeResponseDTO.to_json())

# convert the object into a dict
chargeback_save_dispute_response_dto_dict = chargeback_save_dispute_response_dto_instance.to_dict()
# create an instance of ChargebackSaveDisputeResponseDTO from a dict
chargeback_save_dispute_response_dto_from_dict = ChargebackSaveDisputeResponseDTO.from_dict(chargeback_save_dispute_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
