# AiAuditError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | 
**error** | **str** |  | 
**code** | **str** |  | [optional] 
**retryable** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.ai_audit_error import AiAuditError

# TODO update the JSON string below
json = "{}"
# create an instance of AiAuditError from a JSON string
ai_audit_error_instance = AiAuditError.from_json(json)
# print the JSON string representation of the object
print(AiAuditError.to_json())

# convert the object into a dict
ai_audit_error_dict = ai_audit_error_instance.to_dict()
# create an instance of AiAuditError from a dict
ai_audit_error_from_dict = AiAuditError.from_dict(ai_audit_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


