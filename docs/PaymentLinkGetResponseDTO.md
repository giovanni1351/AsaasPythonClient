# PaymentLinkGetResponseDTO

## Properties

| Name                      | Type                                                                          | Description                                                                                                            | Notes      |
| ------------------------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------- |
| **id**                    | **str**                                                                       | Identificador único do seu link de pagamentos no Asaas                                                                 | [optional] |
| **name**                  | **str**                                                                       | Nome do link de pagamentos                                                                                             | [optional] |
| **value**                 | **float**                                                                     | Valor do link de pagamentos, caso não informado o pagador poderá informar o quanto deseja pagar                        | [optional] |
| **active**                | **bool**                                                                      | Se o link de pagamentos esta ativo                                                                                     | [optional] |
| **charge_type**           | [**PaymentLinkGetResponseChargeType**](PaymentLinkGetResponseChargeType.md)   |                                                                                                                        | [optional] |
| **url**                   | **str**                                                                       | Link de acesso do link de pagamentos                                                                                   | [optional] |
| **billing_type**          | [**PaymentLinkGetResponseBillingType**](PaymentLinkGetResponseBillingType.md) |                                                                                                                        | [optional] |
| **subscription_cycle**    | [**PaymentLinkGetResponseCycle**](PaymentLinkGetResponseCycle.md)             |                                                                                                                        | [optional] |
| **description**           | **str**                                                                       | Descrição do link de pagamentos                                                                                        | [optional] |
| **end_date**              | **date**                                                                      | Data de encerramento                                                                                                   | [optional] |
| **deleted**               | **bool**                                                                      | Indica se o link de pagamento foi removido                                                                             | [optional] |
| **view_count**            | **int**                                                                       | A quantidade de visualizações do seu link de pagamentos                                                                | [optional] |
| **max_installment_count** | **int**                                                                       | Quantidade máxima de parcelas que seu cliente poderá parcelar o valor do link de pagamentos, caso seja Parcelamento.   | [optional] |
| **due_date_limit_days**   | **int**                                                                       | Quantidade de dias úteis que o seu cliente poderá pagar após o boleto ser gerado (Para forma de pagamento como Boleto) | [optional] |
| **notification_enabled**  | **bool**                                                                      | Define se os clientes cadastrados pelo link de pagamentos terão as notificações habilitadas                            | [optional] |
| **is_address_required**   | **bool**                                                                      | Define se o preenchimento de endereço será obrigatório nas cobranças.                                                  | [optional] |
| **external_reference**    | **str**                                                                       | Campo livre para busca                                                                                                 | [optional] |

## Example

```python
from asaas.models.payment_link_get_response_dto import PaymentLinkGetResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentLinkGetResponseDTO from a JSON string
payment_link_get_response_dto_instance = PaymentLinkGetResponseDTO.from_json(json)
# print the JSON string representation of the object
print(PaymentLinkGetResponseDTO.to_json())

# convert the object into a dict
payment_link_get_response_dto_dict = payment_link_get_response_dto_instance.to_dict()
# create an instance of PaymentLinkGetResponseDTO from a dict
payment_link_get_response_dto_from_dict = PaymentLinkGetResponseDTO.from_dict(payment_link_get_response_dto_dict)
```

[[Back to Model list]](index.md#documentation-for-models) [[Back to API list]](index.md#documentation-for-api-endpoints) [[Back to README]](index.md)
