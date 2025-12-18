# V2CrawlerSitemapInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Sitemap URL | [optional] 
**recursive** | **bool** | Recursively follow sitemap links | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_sitemap_inner import V2CrawlerSitemapInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerSitemapInner from a JSON string
v2_crawler_sitemap_inner_instance = V2CrawlerSitemapInner.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerSitemapInner.to_json())

# convert the object into a dict
v2_crawler_sitemap_inner_dict = v2_crawler_sitemap_inner_instance.to_dict()
# create an instance of V2CrawlerSitemapInner from a dict
v2_crawler_sitemap_inner_from_dict = V2CrawlerSitemapInner.from_dict(v2_crawler_sitemap_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


