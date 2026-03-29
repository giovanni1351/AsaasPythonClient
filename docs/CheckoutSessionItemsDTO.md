# CheckoutSessionItemsDTO

Lista de itens no checkout

## Properties

| Name                   | Type      | Description                                | Notes      |
| ---------------------- | --------- | ------------------------------------------ | ---------- |
| **external_reference** | **str**   | Identificador único do item no seu sistema | [optional] |
| **description**        | **str**   | Descrição do item                          | [optional] |
| **image_base64**       | **str**   | Imagem do item em Base64                   |
| **name**               | **str**   | Nome do item                               |
| **quantity**           | **int**   | Quantidade do item                         |
| **value**              | **float** | Valor do item                              |

## Example

```python
from asaas.models.checkout_session_items_dto import CheckoutSessionItemsDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSessionItemsDTO from a JSON string
checkout_session_items_dto_instance = CheckoutSessionItemsDTO.from_json(json)
# print the JSON string representation of the object
print(CheckoutSessionItemsDTO.to_json())

# convert the object into a dict
checkout_session_items_dto_dict = checkout_session_items_dto_instance.to_dict()
# create an instance of CheckoutSessionItemsDTO from a dict
checkout_session_items_dto_from_dict = CheckoutSessionItemsDTO.from_dict(checkout_session_items_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
