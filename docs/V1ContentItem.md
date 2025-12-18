# V1ContentItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**date_timestamp** | **str** |  | 
**published** | **str** |  | 
**revision_count** | **int** |  | 
**desc** | **str** |  | [optional] 
**uuid** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.v1_content_item import V1ContentItem

# TODO update the JSON string below
json = "{}"
# create an instance of V1ContentItem from a JSON string
v1_content_item_instance = V1ContentItem.from_json(json)
# print the JSON string representation of the object
print(V1ContentItem.to_json())

# convert the object into a dict
v1_content_item_dict = v1_content_item_instance.to_dict()
# create an instance of V1ContentItem from a dict
v1_content_item_from_dict = V1ContentItem.from_dict(v1_content_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


