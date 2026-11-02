# AiAuditRecordsPage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | 
**error** | **bool** | Error flag | 
**org_id** | **str** |  | 
**start_date** | **date** |  | 
**end_date** | **date** |  | 
**count** | **int** |  | 
**records** | [**List[AiAuditRecordRow]**](AiAuditRecordRow.md) |  | 
**scanned** | **int** | Keys examined by this call | 
**skipped_archived** | **int** | Records older than 365 days (archived) that this call left out | 
**has_more** | **bool** |  | 
**next_cursor** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.ai_audit_records_page import AiAuditRecordsPage

# TODO update the JSON string below
json = "{}"
# create an instance of AiAuditRecordsPage from a JSON string
ai_audit_records_page_instance = AiAuditRecordsPage.from_json(json)
# print the JSON string representation of the object
print(AiAuditRecordsPage.to_json())

# convert the object into a dict
ai_audit_records_page_dict = ai_audit_records_page_instance.to_dict()
# create an instance of AiAuditRecordsPage from a dict
ai_audit_records_page_from_dict = AiAuditRecordsPage.from_dict(ai_audit_records_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


