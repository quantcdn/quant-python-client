# V2CrawlerBrowserConfig

Browser-mode behaviour. Only applies when browser_mode is true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**capture_api_responses** | **bool** | Store XHR/fetch responses as files, so a static copy can serve a site whose navigation or content is rendered client-side from a JSON endpoint | [optional] 
**wait_for_network_idle** | **int** | Wait for the network to settle before capture, in milliseconds. Useful for API-driven sites | [optional] 
**use_rendered_html** | **bool** | Store the JavaScript-modified DOM instead of the original HTML response | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_browser_config import V2CrawlerBrowserConfig

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerBrowserConfig from a JSON string
v2_crawler_browser_config_instance = V2CrawlerBrowserConfig.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerBrowserConfig.to_json())

# convert the object into a dict
v2_crawler_browser_config_dict = v2_crawler_browser_config_instance.to_dict()
# create an instance of V2CrawlerBrowserConfig from a dict
v2_crawler_browser_config_from_dict = V2CrawlerBrowserConfig.from_dict(v2_crawler_browser_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


