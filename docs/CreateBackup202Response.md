# CreateBackup202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_backup202_response import CreateBackup202Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBackup202Response from a JSON string
create_backup202_response_instance = CreateBackup202Response.from_json(json)
# print the JSON string representation of the object
print(CreateBackup202Response.to_json())

# convert the object into a dict
create_backup202_response_dict = create_backup202_response_instance.to_dict()
# create an instance of CreateBackup202Response from a dict
create_backup202_response_from_dict = CreateBackup202Response.from_dict(create_backup202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


