# ListSkills200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**skills** | [**List[ListSkills200ResponseSkillsInner]**](ListSkills200ResponseSkillsInner.md) |  | [optional] 
**count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.list_skills200_response import ListSkills200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListSkills200Response from a JSON string
list_skills200_response_instance = ListSkills200Response.from_json(json)
# print the JSON string representation of the object
print(ListSkills200Response.to_json())

# convert the object into a dict
list_skills200_response_dict = list_skills200_response_instance.to_dict()
# create an instance of ListSkills200Response from a dict
list_skills200_response_from_dict = ListSkills200Response.from_dict(list_skills200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


