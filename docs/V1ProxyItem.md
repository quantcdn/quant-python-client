# V1ProxyItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**proxy_url** | **str** |  | 
**date_timestamp** | **str** |  | 
**published** | **str** |  | 
**revision_count** | **int** |  | 

## Example

```python
from quantcdn.models.v1_proxy_item import V1ProxyItem

# TODO update the JSON string below
json = "{}"
# create an instance of V1ProxyItem from a JSON string
v1_proxy_item_instance = V1ProxyItem.from_json(json)
# print the JSON string representation of the object
print(V1ProxyItem.to_json())

# convert the object into a dict
v1_proxy_item_dict = v1_proxy_item_instance.to_dict()
# create an instance of V1ProxyItem from a dict
v1_proxy_item_from_dict = V1ProxyItem.from_dict(v1_proxy_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


