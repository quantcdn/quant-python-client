# V2CrawlerAssets

Asset harvesting configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network_intercept** | [**V2CrawlerAssetsNetworkIntercept**](V2CrawlerAssetsNetworkIntercept.md) |  | [optional] 
**parser** | [**V2CrawlerAssetsParser**](V2CrawlerAssetsParser.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_assets import V2CrawlerAssets

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerAssets from a JSON string
v2_crawler_assets_instance = V2CrawlerAssets.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerAssets.to_json())

# convert the object into a dict
v2_crawler_assets_dict = v2_crawler_assets_instance.to_dict()
# create an instance of V2CrawlerAssets from a dict
v2_crawler_assets_from_dict = V2CrawlerAssets.from_dict(v2_crawler_assets_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


