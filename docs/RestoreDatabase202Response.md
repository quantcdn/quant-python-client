# RestoreDatabase202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**restore_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.restore_database202_response import RestoreDatabase202Response

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreDatabase202Response from a JSON string
restore_database202_response_instance = RestoreDatabase202Response.from_json(json)
# print the JSON string representation of the object
print(RestoreDatabase202Response.to_json())

# convert the object into a dict
restore_database202_response_dict = restore_database202_response_instance.to_dict()
# create an instance of RestoreDatabase202Response from a dict
restore_database202_response_from_dict = RestoreDatabase202Response.from_dict(restore_database202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


