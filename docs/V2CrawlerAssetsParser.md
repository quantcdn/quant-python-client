# V2CrawlerAssetsParser

Parser configuration for asset extraction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Enable parser | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_assets_parser import V2CrawlerAssetsParser

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerAssetsParser from a JSON string
v2_crawler_assets_parser_instance = V2CrawlerAssetsParser.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerAssetsParser.to_json())

# convert the object into a dict
v2_crawler_assets_parser_dict = v2_crawler_assets_parser_instance.to_dict()
# create an instance of V2CrawlerAssetsParser from a dict
v2_crawler_assets_parser_from_dict = V2CrawlerAssetsParser.from_dict(v2_crawler_assets_parser_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


