# CrawlersRunRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**urls** | **List[str]** | URLs to crawl | [optional] 

## Example

```python
from quantcdn.models.crawlers_run_request import CrawlersRunRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CrawlersRunRequest from a JSON string
crawlers_run_request_instance = CrawlersRunRequest.from_json(json)
# print the JSON string representation of the object
print(CrawlersRunRequest.to_json())

# convert the object into a dict
crawlers_run_request_dict = crawlers_run_request_instance.to_dict()
# create an instance of CrawlersRunRequest from a dict
crawlers_run_request_from_dict = CrawlersRunRequest.from_dict(crawlers_run_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


