# PixAddressKeySaveRequestDTO


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**PixAddressKeySaveRequestPixAddressKeyType**](PixAddressKeySaveRequestPixAddressKeyType.md) |  | 

## Example

```python
from asaas.models.pix_address_key_save_request_dto import PixAddressKeySaveRequestDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PixAddressKeySaveRequestDTO from a JSON string
pix_address_key_save_request_dto_instance = PixAddressKeySaveRequestDTO.from_json(json)
# print the JSON string representation of the object
print(PixAddressKeySaveRequestDTO.to_json())

# convert the object into a dict
pix_address_key_save_request_dto_dict = pix_address_key_save_request_dto_instance.to_dict()
# create an instance of PixAddressKeySaveRequestDTO from a dict
pix_address_key_save_request_dto_from_dict = PixAddressKeySaveRequestDTO.from_dict(pix_address_key_save_request_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


