# BillSimulateBankSlipInfoResponseDTO

Informações do boleto a ser pago

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identification_field** | **str** | Linha digitável | [optional] 
**value** | **float** | Valor do boleto | [optional] 
**due_date** | **date** | Data de vencimento | [optional] 
**company_name** | **str** | Empresa/Órgão emissor do boleto | [optional] 
**bank** | **str** | Código do banco emissor do boleto no sistema bancário | [optional] 
**beneficiary_cpf_cnpj** | **str** | CPF ou CNPJ do beneficiário | [optional] 
**beneficiary_name** | **str** | Nome do beneficiário | [optional] 
**allow_change_value** | **bool** | Se o valor pode ser alterado ou não | [optional] 
**min_value** | **float** | Valor mínimo que pode ser alterado | [optional] 
**max_value** | **float** | Valor máximo que pode ser alterado | [optional] 
**discount_value** | **float** | Valor dos descontos | [optional] 
**interest_value** | **float** | Valor do juros | [optional] 
**fine_value** | **float** | Valor da multa | [optional] 
**original_value** | **float** | Valor original do boleto | [optional] 
**total_discount_value** | **float** | Valor total de descontos e abatimentos | [optional] 
**total_additional_value** | **float** | Valor total de juros e multa | [optional] 
**is_overdue** | **bool** | Informa se o boleto está vencido | [optional] 

## Example

```python
from asaas.models.bill_simulate_bank_slip_info_response_dto import BillSimulateBankSlipInfoResponseDTO

# TODO update the JSON string below
json = "{}"
# create an instance of BillSimulateBankSlipInfoResponseDTO from a JSON string
bill_simulate_bank_slip_info_response_dto_instance = BillSimulateBankSlipInfoResponseDTO.from_json(json)
# print the JSON string representation of the object
print(BillSimulateBankSlipInfoResponseDTO.to_json())

# convert the object into a dict
bill_simulate_bank_slip_info_response_dto_dict = bill_simulate_bank_slip_info_response_dto_instance.to_dict()
# create an instance of BillSimulateBankSlipInfoResponseDTO from a dict
bill_simulate_bank_slip_info_response_dto_from_dict = BillSimulateBankSlipInfoResponseDTO.from_dict(bill_simulate_bank_slip_info_response_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


