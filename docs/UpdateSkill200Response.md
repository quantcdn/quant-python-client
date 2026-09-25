# UpdateSkill200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**skill** | **object** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.update_skill200_response import UpdateSkill200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSkill200Response from a JSON string
update_skill200_response_instance = UpdateSkill200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateSkill200Response.to_json())

# convert the object into a dict
update_skill200_response_dict = update_skill200_response_instance.to_dict()
# create an instance of UpdateSkill200Response from a dict
update_skill200_response_from_dict = UpdateSkill200Response.from_dict(update_skill200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


