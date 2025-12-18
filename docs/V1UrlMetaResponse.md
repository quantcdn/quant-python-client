# V1UrlMetaResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**global_meta** | [**V1GlobalMetaResponseGlobalMeta**](V1GlobalMetaResponseGlobalMeta.md) |  | [optional] 

## Example

```python
from quantcdn.models.v1_url_meta_response import V1UrlMetaResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1UrlMetaResponse from a JSON string
v1_url_meta_response_instance = V1UrlMetaResponse.from_json(json)
# print the JSON string representation of the object
print(V1UrlMetaResponse.to_json())

# convert the object into a dict
v1_url_meta_response_dict = v1_url_meta_response_instance.to_dict()
# create an instance of V1UrlMetaResponse from a dict
v1_url_meta_response_from_dict = V1UrlMetaResponse.from_dict(v1_url_meta_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


