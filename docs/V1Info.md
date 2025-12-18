# V1Info


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**author_user** | **str** |  | [optional] 
**author_name** | **str** |  | [optional] 
**author_email** | **str** |  | [optional] 
**log** | **str** |  | [optional] 
**custom_1** | **str** |  | [optional] 
**custom_2** | **str** |  | [optional] 
**source** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.v1_info import V1Info

# TODO update the JSON string below
json = "{}"
# create an instance of V1Info from a JSON string
v1_info_instance = V1Info.from_json(json)
# print the JSON string representation of the object
print(V1Info.to_json())

# convert the object into a dict
v1_info_dict = v1_info_instance.to_dict()
# create an instance of V1Info from a dict
v1_info_from_dict = V1Info.from_dict(v1_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


