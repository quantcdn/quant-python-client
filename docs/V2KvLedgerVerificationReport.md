# V2KvLedgerVerificationReport

A verification record signed with the ledger key: signature is the base64 DER ECDSA P-256 signature over the SHA-256 of the UTF-8 bytes of json (the RFC 8785 form of report). The body is the KV service bytes unchanged; save it as is and check it offline (kv-ledger-verify verify-signed --doc report.json --public-key key.pem). Trust only json.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**report** | [**V2KvLedgerVerificationReportReport**](V2KvLedgerVerificationReportReport.md) |  | 
**var_json** | **str** | The exact signed text. | 
**signature** | **str** |  | 
**key_id** | **str** |  | 
**algorithm** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_verification_report import V2KvLedgerVerificationReport

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerVerificationReport from a JSON string
v2_kv_ledger_verification_report_instance = V2KvLedgerVerificationReport.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerVerificationReport.to_json())

# convert the object into a dict
v2_kv_ledger_verification_report_dict = v2_kv_ledger_verification_report_instance.to_dict()
# create an instance of V2KvLedgerVerificationReport from a dict
v2_kv_ledger_verification_report_from_dict = V2KvLedgerVerificationReport.from_dict(v2_kv_ledger_verification_report_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


