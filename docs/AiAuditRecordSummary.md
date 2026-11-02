# AiAuditRecordSummary

Normalised fields of any record type. A field with an unexpected type is left out.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | 
**error** | **bool** | Error flag | 
**record_type** | **str** | inference for a record without recordType; tool_denied, tool_proposal, tool_decision, tool_outcome, slack_bot_api, audit_access, ...; unknown for an unreadable object | 
**timestamp** | **datetime** |  | [optional] 
**user_id** | **str** |  | [optional] 
**token_id** | **str** |  | [optional] 
**model_id** | **str** |  | [optional] 
**interface** | **str** |  | [optional] 
**tools** | **List[str]** |  | 
**decision** | **str** |  | [optional] 
**outcome** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.ai_audit_record_summary import AiAuditRecordSummary

# TODO update the JSON string below
json = "{}"
# create an instance of AiAuditRecordSummary from a JSON string
ai_audit_record_summary_instance = AiAuditRecordSummary.from_json(json)
# print the JSON string representation of the object
print(AiAuditRecordSummary.to_json())

# convert the object into a dict
ai_audit_record_summary_dict = ai_audit_record_summary_instance.to_dict()
# create an instance of AiAuditRecordSummary from a dict
ai_audit_record_summary_from_dict = AiAuditRecordSummary.from_dict(ai_audit_record_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


