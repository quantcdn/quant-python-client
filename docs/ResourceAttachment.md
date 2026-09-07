# ResourceAttachment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_name** | **str** |  | [optional] 
**env_name** | **str** |  | [optional] 
**env_var_prefix** | **str** | Namespaces every injected variable, so MEDIA yields MEDIA_S3_BUCKET | [optional] 
**access_key_id** | **str** | Object storage only. The secret half is written to the environment&#39;s secrets and never returned. | [optional] 
**cache_user_id** | **str** | Cache only. This environment&#39;s own RBAC user, limited to its CACHE_PREFIX with FLUSHALL and FLUSHDB denied, so it cannot touch another environment&#39;s keys. | [optional] 
**access_level** | **str** | Cache only. scoped: the environment holds its own RBAC user. admin: it holds the cache-wide credential and can read, write and flush every attached environment&#39;s keys. Absent on attachments made before access levels existed (treated as scoped). | [optional] 
**injected_keys** | **List[str]** | The exact variable names this attachment wrote, removed precisely on detach | [optional] 
**created_at** | **datetime** |  | [optional] 
**note** | **str** | When the credentials take effect | [optional] 

## Example

```python
from quantcdn.models.resource_attachment import ResourceAttachment

# TODO update the JSON string below
json = "{}"
# create an instance of ResourceAttachment from a JSON string
resource_attachment_instance = ResourceAttachment.from_json(json)
# print the JSON string representation of the object
print(ResourceAttachment.to_json())

# convert the object into a dict
resource_attachment_dict = resource_attachment_instance.to_dict()
# create an instance of ResourceAttachment from a dict
resource_attachment_from_dict = ResourceAttachment.from_dict(resource_attachment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


