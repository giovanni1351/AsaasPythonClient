# CreditCardPreAuthorizationConfigResponseDTO

## Properties

| Name               | Type    | Description                                          | Notes |
| ------------------ | ------- | ---------------------------------------------------- | ----- |
| **days_to_expire** | **int** | Quantidade de dias para expiração da pré-autorização |

## Example

```python
from asaas.models.credit_card_pre_authorization_config_response_dto import CreditCardPreAuthorizationConfigResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of CreditCardPreAuthorizationConfigResponseDTO from a JSON string
credit_card_pre_authorization_config_response_dto_instance = CreditCardPreAuthorizationConfigResponseDTO.from_json(json)
# print the JSON string representation of the object
print(CreditCardPreAuthorizationConfigResponseDTO.to_json())

# convert the object into a dict
credit_card_pre_authorization_config_response_dto_dict = credit_card_pre_authorization_config_response_dto_instance.to_dict()
# create an instance of CreditCardPreAuthorizationConfigResponseDTO from a dict
credit_card_pre_authorization_config_response_dto_from_dict = CreditCardPreAuthorizationConfigResponseDTO.from_dict(credit_card_pre_authorization_config_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
