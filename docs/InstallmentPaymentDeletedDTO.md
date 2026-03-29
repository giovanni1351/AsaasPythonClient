# InstallmentPaymentDeletedDTO

Lista das cobranças que foram removidas

## Properties

| Name                   | Type     | Description                              | Notes      |
| ---------------------- | -------- | ---------------------------------------- | ---------- |
| **id**                 | **str**  | Identificador único da cobrança no Asaas | [optional] |
| **installment_number** | **str**  | Número da parcela                        | [optional] |
| **deleted**            | **bool** | Determina se a cobrança foi removida     | [optional] |

## Example

```python
from asaas.models.installment_payment_deleted_dto import InstallmentPaymentDeletedDTO

# TODO update the JSON string below
json = "{}"
# create an instance of InstallmentPaymentDeletedDTO from a JSON string
installment_payment_deleted_dto_instance = InstallmentPaymentDeletedDTO.from_json(json)
# print the JSON string representation of the object
print(InstallmentPaymentDeletedDTO.to_json())

# convert the object into a dict
installment_payment_deleted_dto_dict = installment_payment_deleted_dto_instance.to_dict()
# create an instance of InstallmentPaymentDeletedDTO from a dict
installment_payment_deleted_dto_from_dict = InstallmentPaymentDeletedDTO.from_dict(installment_payment_deleted_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
