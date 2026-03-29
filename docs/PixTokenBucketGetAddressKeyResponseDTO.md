# PixTokenBucketGetAddressKeyResponseDTO

## Properties

| Name          | Type    | Description                      | Notes      |
| ------------- | ------- | -------------------------------- | ---------- |
| **capacity**  | **int** | Capacidade máxima de fichas      | [optional] |
| **remaining** | **int** | Quantidade de fichas disponíveis | [optional] |

## Example

```python
from asaas.models.pix_token_bucket_get_address_key_response_dto import PixTokenBucketGetAddressKeyResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixTokenBucketGetAddressKeyResponseDTO from a JSON string
pix_token_bucket_get_address_key_response_dto_instance = PixTokenBucketGetAddressKeyResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PixTokenBucketGetAddressKeyResponseDTO.to_json())

# convert the object into a dict
pix_token_bucket_get_address_key_response_dto_dict = pix_token_bucket_get_address_key_response_dto_instance.to_dict()
# create an instance of PixTokenBucketGetAddressKeyResponseDTO from a dict
pix_token_bucket_get_address_key_response_dto_from_dict = PixTokenBucketGetAddressKeyResponseDTO.from_dict(pix_token_bucket_get_address_key_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
