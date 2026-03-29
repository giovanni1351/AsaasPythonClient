# PixQrCodeDecodeReceiverDTO

Informações sobre o recebedor

## Properties

| Name             | Type                                                                                  | Description                      | Notes      |
| ---------------- | ------------------------------------------------------------------------------------- | -------------------------------- | ---------- |
| **ispb**         | **str**                                                                               | Código da instituição financeira | [optional] |
| **ispb_name**    | **str**                                                                               | Nome da instituição financeira   | [optional] |
| **name**         | **str**                                                                               | Nome do Recebedor                | [optional] |
| **trading_name** | **str**                                                                               | Nome fantasia do recebedor       | [optional] |
| **cpf_cnpj**     | **str**                                                                               | CPF ou CNPJ do recebedor         | [optional] |
| **person_type**  | [**PixQrCodeDecodeReceiverPersonType**](PixQrCodeDecodeReceiverPersonType.md)         |                                  | [optional] |
| **account_type** | [**PixQrCodeDecodeReceiverPixAccountType**](PixQrCodeDecodeReceiverPixAccountType.md) |                                  | [optional] |

## Example

```python
from asaas.models.pix_qr_code_decode_receiver_dto import PixQrCodeDecodeReceiverDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixQrCodeDecodeReceiverDTO from a JSON string
pix_qr_code_decode_receiver_dto_instance = PixQrCodeDecodeReceiverDTO.from_json(json)
# print the JSON string representation of the object
print(PixQrCodeDecodeReceiverDTO.to_json())

# convert the object into a dict
pix_qr_code_decode_receiver_dto_dict = pix_qr_code_decode_receiver_dto_instance.to_dict()
# create an instance of PixQrCodeDecodeReceiverDTO from a dict
pix_qr_code_decode_receiver_dto_from_dict = PixQrCodeDecodeReceiverDTO.from_dict(pix_qr_code_decode_receiver_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
