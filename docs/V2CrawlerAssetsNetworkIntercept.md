# V2CrawlerAssetsNetworkIntercept

Network intercept configuration for asset collection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Enable network intercept | [optional] 
**timeout** | **int** | Request timeout in seconds | [optional] 
**execute_js** | **bool** | Execute JavaScript during asset collection | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_assets_network_intercept import V2CrawlerAssetsNetworkIntercept

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerAssetsNetworkIntercept from a JSON string
v2_crawler_assets_network_intercept_instance = V2CrawlerAssetsNetworkIntercept.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerAssetsNetworkIntercept.to_json())

# convert the object into a dict
v2_crawler_assets_network_intercept_dict = v2_crawler_assets_network_intercept_instance.to_dict()
# create an instance of V2CrawlerAssetsNetworkIntercept from a dict
v2_crawler_assets_network_intercept_from_dict = V2CrawlerAssetsNetworkIntercept.from_dict(v2_crawler_assets_network_intercept_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


