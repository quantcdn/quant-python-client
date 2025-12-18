# V2CrawlerRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Crawler name | [optional] 
**domain** | **str** | Domain to crawl | 
**browser_mode** | **bool** | Enable browser mode | [optional] [default to False]
**urls** | **List[str]** | URLs to crawl | [optional] 
**start_urls** | **List[str]** | Starting URLs for crawl | [optional] 
**headers** | **Dict[str, str]** | Custom headers | [optional] 
**exclude** | **List[str]** | URL patterns to exclude (regex) | [optional] 
**include** | **List[str]** | URL patterns to include (regex) | [optional] 
**webhook_url** | **str** | Webhook URL for notifications | [optional] 
**webhook_auth_header** | **str** | Authorization header for webhook | [optional] 
**webhook_extra_vars** | **str** | Extra variables for webhook | [optional] 
**workers** | **int** | Number of concurrent workers (default: 2, non-default requires verification) | [optional] 
**delay** | **float** | Delay between requests in seconds (default: 4, non-default requires verification) | [optional] 
**depth** | **int** | Maximum crawl depth, -1 for unlimited | [optional] 
**max_hits** | **int** | Maximum total requests, 0 for unlimited (default: 0, non-default requires verification) | [optional] 
**max_html** | **int** | Maximum HTML pages, 0 for unlimited (default: org limit, non-default requires verification) | [optional] 
**status_ok** | **List[int]** | HTTP status codes that will result in content being captured and pushed to Quant | [optional] 
**sitemap** | [**List[V2CrawlerSitemapInner]**](V2CrawlerSitemapInner.md) | Sitemap configuration | [optional] 
**allowed_domains** | **List[str]** | Allowed domains for multi-domain crawling, automatically enables merge_domains | [optional] 
**user_agent** | **str** | Custom user agent, only when browser_mode is false | [optional] 
**assets** | [**V2CrawlerAssets**](V2CrawlerAssets.md) |  | [optional] 
**max_errors** | **int** | Maximum errors before stopping crawl | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_request import V2CrawlerRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerRequest from a JSON string
v2_crawler_request_instance = V2CrawlerRequest.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerRequest.to_json())

# convert the object into a dict
v2_crawler_request_dict = v2_crawler_request_instance.to_dict()
# create an instance of V2CrawlerRequest from a dict
v2_crawler_request_from_dict = V2CrawlerRequest.from_dict(v2_crawler_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


