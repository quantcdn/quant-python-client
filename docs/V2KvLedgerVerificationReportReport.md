# V2KvLedgerVerificationReportReport


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**v** | **int** |  | 
**type** | **str** |  | 
**org** | **str** |  | 
**store** | **str** |  | 
**ledger** | **str** |  | 
**id** | **str** |  | 
**at** | **datetime** |  | 
**started_at** | **datetime** |  | 
**trigger** | **str** |  | 
**scope** | **Dict[str, object]** |  | 
**complete** | **bool** |  | 
**ok** | **bool** |  | 
**entries** | **int** |  | 
**shards_failed** | **int** |  | 
**failures** | [**List[V2KvLedgerFailure]**](V2KvLedgerFailure.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_verification_report_report import V2KvLedgerVerificationReportReport

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerVerificationReportReport from a JSON string
v2_kv_ledger_verification_report_report_instance = V2KvLedgerVerificationReportReport.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerVerificationReportReport.to_json())

# convert the object into a dict
v2_kv_ledger_verification_report_report_dict = v2_kv_ledger_verification_report_report_instance.to_dict()
# create an instance of V2KvLedgerVerificationReportReport from a dict
v2_kv_ledger_verification_report_report_from_dict = V2KvLedgerVerificationReportReport.from_dict(v2_kv_ledger_verification_report_report_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


