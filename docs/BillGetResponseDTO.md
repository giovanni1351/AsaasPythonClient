# BillGetResponseDTO

## Properties

| Name                        | Type                                                          | Description                                        | Notes      |
| --------------------------- | ------------------------------------------------------------- | -------------------------------------------------- | ---------- |
| **object**                  | **str**                                                       | Tipo de objeto                                     | [optional] |
| **id**                      | **str**                                                       | Identificador único do pagamento de conta no Asaas | [optional] |
| **status**                  | [**BillGetResponseBillStatus**](BillGetResponseBillStatus.md) |                                                    | [optional] |
| **value**                   | **float**                                                     | Valor a ser pago                                   | [optional] |
| **discount**                | **float**                                                     | Desconto atribuído ao pagamento                    | [optional] |
| **interest**                | **float**                                                     | Juros atribuído ao pagamento                       | [optional] |
| **fine**                    | **float**                                                     | Multa atribuída ao pagamento                       | [optional] |
| **identification_field**    | **str**                                                       | Linha digitável do boleto a ser pago               | [optional] |
| **due_date**                | **date**                                                      | Data de vencimento da cobrança                     | [optional] |
| **schedule_date**           | **date**                                                      | Data de agendamento do pagamento                   | [optional] |
| **payment_date**            | **date**                                                      | Data em que o pagamento foi efetivado              | [optional] |
| **fee**                     | **float**                                                     | Taxa do Asaas para o pagamento de conta            | [optional] |
| **description**             | **str**                                                       | Descrição do pagamento de conta                    | [optional] |
| **company_name**            | **str**                                                       | Empresa/Órgão emissor da cobrança                  | [optional] |
| **transaction_receipt_url** | **str**                                                       | Comprovante do pagamento de conta                  | [optional] |
| **can_be_cancelled**        | **bool**                                                      | Se o pagamento pode ser cancelado                  | [optional] |
| **external_reference**      | **str**                                                       | Identificador do boleto no seu sistema             | [optional] |
| **fail_reasons**            | **List[str]**                                                 | Lista com motivos de falha no pagamento            | [optional] |

## Example

```python
from asaas.models.bill_get_response_dto import BillGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of BillGetResponseDTO from a JSON string
bill_get_response_dto_instance = BillGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(BillGetResponseDTO.to_json())

# convert the object into a dict
bill_get_response_dto_dict = bill_get_response_dto_instance.to_dict()
# create an instance of BillGetResponseDTO from a dict
bill_get_response_dto_from_dict = BillGetResponseDTO.from_dict(bill_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
