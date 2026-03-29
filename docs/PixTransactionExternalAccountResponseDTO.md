# PixTransactionExternalAccountResponseDTO

Informações sobre o recebedor

## Properties

| Name                 | Type                                                                                                                    | Description                               | Notes      |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- | ---------- |
| **ispb**             | **str**                                                                                                                 | Identificador da Instituição de Pagamento | [optional] |
| **ispb_name**        | **str**                                                                                                                 | Nome da Instituição de pagamento          | [optional] |
| **name**             | **str**                                                                                                                 | Nome do recebedor                         | [optional] |
| **cpf_cnpj**         | **str**                                                                                                                 | Cpf ou Cnpj do recebedor                  | [optional] |
| **address_key**      | **str**                                                                                                                 | Chave Pix                                 | [optional] |
| **address_key_type** | [**PixTransactionExternalAccountResponsePixAddressKeyType**](PixTransactionExternalAccountResponsePixAddressKeyType.md) |                                           | [optional] |

## Example

```python
from asaas.models.pix_transaction_external_account_response_dto import PixTransactionExternalAccountResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTransactionExternalAccountResponseDTO from a JSON string
pix_transaction_external_account_response_dto_instance = PixTransactionExternalAccountResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixTransactionExternalAccountResponseDTO.to_json())

# convert the object into a dict
pix_transaction_external_account_response_dto_dict = pix_transaction_external_account_response_dto_instance.to_dict()
# create an instance of PixTransactionExternalAccountResponseDTO from a dict
pix_transaction_external_account_response_dto_from_dict = PixTransactionExternalAccountResponseDTO.from_dict(pix_transaction_external_account_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
