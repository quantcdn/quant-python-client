# V1RedirectItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | * @OA\\Schema(   schema&#x3D;\&quot;V1RedirectItem\&quot;,   type&#x3D;\&quot;object\&quot;,   required&#x3D;{\&quot;url\&quot;,\&quot;redirect_url\&quot;,\&quot;redirect_http_code\&quot;,\&quot;date_timestamp\&quot;,\&quot;published\&quot;,\&quot;revision_count\&quot;}, | 
**redirect_url** | **str** |  | 
**redirect_http_code** | **int** |  | 
**date_timestamp** | **str** |  | 
**published** | **str** |  | 
**revision_count** | **int** |  | 

## Example

```python
from quantcdn.models.v1_redirect_item import V1RedirectItem

# TODO update the JSON string below
json = "{}"
# create an instance of V1RedirectItem from a JSON string
v1_redirect_item_instance = V1RedirectItem.from_json(json)
# print the JSON string representation of the object
print(V1RedirectItem.to_json())

# convert the object into a dict
v1_redirect_item_dict = v1_redirect_item_instance.to_dict()
# create an instance of V1RedirectItem from a dict
v1_redirect_item_from_dict = V1RedirectItem.from_dict(v1_redirect_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


