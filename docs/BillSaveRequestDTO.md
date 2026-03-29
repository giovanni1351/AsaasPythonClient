# BillSaveRequestDTO

## Properties

| Name                     | Type      | Description                                                                                        | Notes      |
| ------------------------ | --------- | -------------------------------------------------------------------------------------------------- | ---------- |
| **identification_field** | **str**   | Linha digitável do boleto                                                                          |
| **schedule_date**        | **str**   | Data de agendamento do pagamento                                                                   | [optional] |
| **description**          | **str**   | Descrição do pagamento de conta                                                                    | [optional] |
| **discount**             | **float** | Desconto atribuído ao pagamento                                                                    | [optional] |
| **interest**             | **float** | Juros atribuído ao pagamento                                                                       | [optional] |
| **fine**                 | **float** | Multa atribuída ao pagamento                                                                       | [optional] |
| **due_date**             | **date**  | Data de vencimento da conta caso seja do tipo que não possui essa informação                       | [optional] |
| **value**                | **float** | Valor da conta caso seja do tipo que não possui essa informação (Ex: faturas de cartão de crédito) | [optional] |
| **external_reference**   | **str**   | Identificador do boleto no seu sistema                                                             | [optional] |

## Example

```python
from asaas.models.bill_save_request_dto import BillSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of BillSaveRequestDTO from a JSON string
bill_save_request_dto_instance = BillSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(BillSaveRequestDTO.to_json())

# convert the object into a dict
bill_save_request_dto_dict = bill_save_request_dto_instance.to_dict()
# create an instance of BillSaveRequestDTO from a dict
bill_save_request_dto_from_dict = BillSaveRequestDTO.from_dict(bill_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
