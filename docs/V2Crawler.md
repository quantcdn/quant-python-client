# V2Crawler


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Crawler ID | 
**name** | **str** | Crawler name | [optional] 
**project_id** | **int** | Project ID | 
**uuid** | **str** | Crawler UUID | 
**config** | **str** | Crawler configuration (YAML) | 
**domain** | **str** | Crawler domain | 
**domain_verified** | **int** | Domain verification status | [optional] [default to 0]
**urls_list** | **str** | URLs list (YAML) | [optional] 
**webhook_url** | **str** | Webhook URL for notifications | [optional] 
**webhook_auth_header** | **str** | Authorization header for webhook | [optional] 
**webhook_extra_vars** | **str** | Extra variables for webhook | [optional] 
**browser_mode** | **bool** | Browser mode enabled | [optional] 
**workers** | **int** | Number of concurrent workers | [optional] 
**delay** | **float** | Delay between requests in seconds | [optional] 
**depth** | **int** | Maximum crawl depth | [optional] 
**max_hits** | **int** | Maximum total requests | [optional] 
**max_html** | **int** | Maximum HTML pages | [optional] 
**status_ok** | **List[int]** | HTTP status codes for content capture | [optional] 
**user_agent** | **str** | Custom user agent | [optional] 
**max_errors** | **int** | Maximum errors before stopping | [optional] 
**start_urls** | **List[str]** | Starting URLs | [optional] 
**urls** | **List[str]** | URLs list | [optional] 
**headers** | **Dict[str, str]** | Custom headers | [optional] 
**exclude** | **List[str]** | URL patterns to exclude | [optional] 
**include** | **List[str]** | URL patterns to include | [optional] 
**sitemap** | [**List[V2CrawlerSitemapInner]**](V2CrawlerSitemapInner.md) | Sitemap configuration | [optional] 
**allowed_domains** | **List[str]** | Allowed domains | [optional] 
**assets** | [**V2CrawlerAssets**](V2CrawlerAssets.md) |  | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 
**deleted_at** | **datetime** | Deletion timestamp | [optional] 

## Example

```python
from quantcdn.models.v2_crawler import V2Crawler

# TODO update the JSON string below
json = "{}"
# create an instance of V2Crawler from a JSON string
v2_crawler_instance = V2Crawler.from_json(json)
# print the JSON string representation of the object
print(V2Crawler.to_json())

# convert the object into a dict
v2_crawler_dict = v2_crawler_instance.to_dict()
# create an instance of V2Crawler from a dict
v2_crawler_from_dict = V2Crawler.from_dict(v2_crawler_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


