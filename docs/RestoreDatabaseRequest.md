# RestoreDatabaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup_id** | **str** | The backup ID to restore (must match path param) | 
**acknowledge_dataloss** | **bool** | Must be true to confirm existing data will be overwritten | 

## Example

```python
from quantcdn.models.restore_database_request import RestoreDatabaseRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreDatabaseRequest from a JSON string
restore_database_request_instance = RestoreDatabaseRequest.from_json(json)
# print the JSON string representation of the object
print(RestoreDatabaseRequest.to_json())

# convert the object into a dict
restore_database_request_dict = restore_database_request_instance.to_dict()
# create an instance of RestoreDatabaseRequest from a dict
restore_database_request_from_dict = RestoreDatabaseRequest.from_dict(restore_database_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


