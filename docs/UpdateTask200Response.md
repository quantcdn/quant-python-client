# UpdateTask200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**updated_at** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.update_task200_response import UpdateTask200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateTask200Response from a JSON string
update_task200_response_instance = UpdateTask200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateTask200Response.to_json())

# convert the object into a dict
update_task200_response_dict = update_task200_response_instance.to_dict()
# create an instance of UpdateTask200Response from a dict
update_task200_response_from_dict = UpdateTask200Response.from_dict(update_task200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


