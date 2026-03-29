# PixQrCodeDecodeRequestDTO

## Properties

| Name                      | Type      | Description                             | Notes      |
| ------------------------- | --------- | --------------------------------------- | ---------- |
| **payload**               | **str**   | Payload do QRCode                       |
| **change_value**          | **float** | Valor do troco (para QRCode Troco)      | [optional] |
| **expected_payment_date** | **date**  | Data prevista para realizar o pagamento | [optional] |

## Example

```python
from asaas.models.pix_qr_code_decode_request_dto import PixQrCodeDecodeRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixQrCodeDecodeRequestDTO from a JSON string
pix_qr_code_decode_request_dto_instance = PixQrCodeDecodeRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixQrCodeDecodeRequestDTO.to_json())

# convert the object into a dict
pix_qr_code_decode_request_dto_dict = pix_qr_code_decode_request_dto_instance.to_dict()
# create an instance of PixQrCodeDecodeRequestDTO from a dict
pix_qr_code_decode_request_dto_from_dict = PixQrCodeDecodeRequestDTO.from_dict(pix_qr_code_decode_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
