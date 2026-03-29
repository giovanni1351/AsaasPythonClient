# TransferSaveInternalTransferResponseDTO

## Properties

| Name                        | Type                                                                                                            | Description                                                                                       | Notes      |
| --------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------- |
| **object**                  | **str**                                                                                                         | Tipo de objeto                                                                                    | [optional] |
| **id**                      | **str**                                                                                                         | Identificador único da transferência no Asaas                                                     | [optional] |
| **type**                    | **str**                                                                                                         | Tipo de transferência                                                                             | [optional] |
| **date_created**            | **date**                                                                                                        | Data de solicitação da transferência                                                              | [optional] |
| **value**                   | **float**                                                                                                       | Valor da transferência                                                                            | [optional] |
| **net_value**               | **float**                                                                                                       | Valor líquido descontada a taxa de transferência                                                  | [optional] |
| **status**                  | [**TransferSaveInternalTransferResponseTransferStatus**](TransferSaveInternalTransferResponseTransferStatus.md) |                                                                                                   | [optional] |
| **transfer_fee**            | **float**                                                                                                       | Taxa de transferência                                                                             | [optional] |
| **effective_date**          | **date**                                                                                                        | Data de efetivação                                                                                | [optional] |
| **schedule_date**           | **date**                                                                                                        | Data de agendamento                                                                               | [optional] |
| **end_to_end_identifier**   | **str**                                                                                                         | Identificador único da transação Pix no Banco Central                                             | [optional] |
| **authorized**              | **bool**                                                                                                        | &#x60;false&#x60; quando aguarda autorização através do Token SMS                                 | [optional] |
| **fail_reason**             | **str**                                                                                                         | Motivo da falha da transferência                                                                  | [optional] |
| **external_reference**      | **str**                                                                                                         | Identificador da transferência no seu sistema                                                     | [optional] |
| **transaction_receipt_url** | **str**                                                                                                         | Comprovante de transferência, estará disponível após a transferência ser confirmada               | [optional] |
| **operation_type**          | [**TransferSaveInternalTransferResponseTransferType**](TransferSaveInternalTransferResponseTransferType.md)     |                                                                                                   | [optional] |
| **description**             | **str**                                                                                                         | Descrição da transferência                                                                        | [optional] |
| **recurring**               | **str**                                                                                                         | Identificador único da recorrência no Asaas                                                       | [optional] |
| **wallet_id**               | **str**                                                                                                         | Identificador único da carteira para fazer split de cobranças ou transferência entre contas Asaas | [optional] |
| **account**                 | [**TransferSaveInternalTransferAccountDTO**](TransferSaveInternalTransferAccountDTO.md)                         |                                                                                                   | [optional] |

## Example

```python
from asaas.models.transfer_save_internal_transfer_response_dto import TransferSaveInternalTransferResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of TransferSaveInternalTransferResponseDTO from a JSON string
transfer_save_internal_transfer_response_dto_instance = TransferSaveInternalTransferResponseDTO.from_json(json)
# print the JSON string representation of the object
print(TransferSaveInternalTransferResponseDTO.to_json())

# convert the object into a dict
transfer_save_internal_transfer_response_dto_dict = transfer_save_internal_transfer_response_dto_instance.to_dict()
# create an instance of TransferSaveInternalTransferResponseDTO from a dict
transfer_save_internal_transfer_response_dto_from_dict = TransferSaveInternalTransferResponseDTO.from_dict(transfer_save_internal_transfer_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
