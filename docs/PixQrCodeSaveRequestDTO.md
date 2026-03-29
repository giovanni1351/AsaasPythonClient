# PixQrCodeSaveRequestDTO

## Properties

| Name                         | Type         | Description                                                                                 | Notes      |
| ---------------------------- | ------------ | ------------------------------------------------------------------------------------------- | ---------- |
| **address_key**              | **str**      | Chave que receberá os pagamentos do QR Code                                                 | [optional] |
| **description**              | **str**      | Descrição do QrCode                                                                         | [optional] |
| **value**                    | **float**    | Valor do QrCode, caso não informado o pagador poderá escolher o valor                       | [optional] |
| **format**                   | **str**      | Formato do QR Code                                                                          | [optional] |
| **expiration_date**          | **datetime** | Data/Hora de expiração do QR Code, após desta data todos os pagamentos serão recusados.     | [optional] |
| **expiration_seconds**       | **int**      | Determina a data de expiração em segundos.                                                  | [optional] |
| **allows_multiple_payments** | **bool**     | Define se o QrCode pode ser pago múltiplas vezes, caso não informado o valor padrão é true. | [optional] |
| **external_reference**       | **str**      | Campo livre para busca                                                                      | [optional] |

## Example

```python
from asaas.models.pix_qr_code_save_request_dto import PixQrCodeSaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixQrCodeSaveRequestDTO from a JSON string
pix_qr_code_save_request_dto_instance = PixQrCodeSaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixQrCodeSaveRequestDTO.to_json())

# convert the object into a dict
pix_qr_code_save_request_dto_dict = pix_qr_code_save_request_dto_instance.to_dict()
# create an instance of PixQrCodeSaveRequestDTO from a dict
pix_qr_code_save_request_dto_from_dict = PixQrCodeSaveRequestDTO.from_dict(pix_qr_code_save_request_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
