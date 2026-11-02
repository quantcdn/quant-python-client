# AiAuditRecordRow


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | 
**error** | **bool** | Error flag | 
**key** | **str** |  | 
**var_date** | **date** |  | 
**summary** | [**AiAuditRecordSummary**](AiAuditRecordSummary.md) |  | 
**record** | **Dict[str, object]** | The stored record. prompt and response are present only when the record has promptStored or responseStored true. | [optional] 
**omitted** | **str** | too-large: read the record with aiAuditRecordGet. | [optional] 

## Example

```python
from quantcdn.models.ai_audit_record_row import AiAuditRecordRow

# TODO update the JSON string below
json = "{}"
# create an instance of AiAuditRecordRow from a JSON string
ai_audit_record_row_instance = AiAuditRecordRow.from_json(json)
# print the JSON string representation of the object
print(AiAuditRecordRow.to_json())

# convert the object into a dict
ai_audit_record_row_dict = ai_audit_record_row_instance.to_dict()
# create an instance of AiAuditRecordRow from a dict
ai_audit_record_row_from_dict = AiAuditRecordRow.from_dict(ai_audit_record_row_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


