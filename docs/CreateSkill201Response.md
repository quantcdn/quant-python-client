# CreateSkill201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**skill** | **object** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_skill201_response import CreateSkill201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSkill201Response from a JSON string
create_skill201_response_instance = CreateSkill201Response.from_json(json)
# print the JSON string representation of the object
print(CreateSkill201Response.to_json())

# convert the object into a dict
create_skill201_response_dict = create_skill201_response_instance.to_dict()
# create an instance of CreateSkill201Response from a dict
create_skill201_response_from_dict = CreateSkill201Response.from_dict(create_skill201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


