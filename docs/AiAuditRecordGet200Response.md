# AiAuditRecordGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**var_date** | **date** |  | 
**summary** | [**AiAuditRecordSummary**](AiAuditRecordSummary.md) |  | 
**record** | **Dict[str, object]** |  | 

## Example

```python
from quantcdn.models.ai_audit_record_get200_response import AiAuditRecordGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AiAuditRecordGet200Response from a JSON string
ai_audit_record_get200_response_instance = AiAuditRecordGet200Response.from_json(json)
# print the JSON string representation of the object
print(AiAuditRecordGet200Response.to_json())

# convert the object into a dict
ai_audit_record_get200_response_dict = ai_audit_record_get200_response_instance.to_dict()
# create an instance of AiAuditRecordGet200Response from a dict
ai_audit_record_get200_response_from_dict = AiAuditRecordGet200Response.from_dict(ai_audit_record_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


