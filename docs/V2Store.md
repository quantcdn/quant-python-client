# V2Store


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Store ID | 
**name** | **str** | Store name | 

## Example

```python
from quantcdn.models.v2_store import V2Store

# TODO update the JSON string below
json = "{}"
# create an instance of V2Store from a JSON string
v2_store_instance = V2Store.from_json(json)
# print the JSON string representation of the object
print(V2Store.to_json())

# convert the object into a dict
v2_store_dict = v2_store_instance.to_dict()
# create an instance of V2Store from a dict
v2_store_from_dict = V2Store.from_dict(v2_store_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


