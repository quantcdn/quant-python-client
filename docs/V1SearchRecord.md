# V1SearchRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**summary** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.v1_search_record import V1SearchRecord

# TODO update the JSON string below
json = "{}"
# create an instance of V1SearchRecord from a JSON string
v1_search_record_instance = V1SearchRecord.from_json(json)
# print the JSON string representation of the object
print(V1SearchRecord.to_json())

# convert the object into a dict
v1_search_record_dict = v1_search_record_instance.to_dict()
# create an instance of V1SearchRecord from a dict
v1_search_record_from_dict = V1SearchRecord.from_dict(v1_search_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


