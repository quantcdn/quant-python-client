# AiSearchIngestPagesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**job_id** | **str** |  | [optional] 
**pages** | [**List[AiSearchIngestPagesRequestPagesInner]**](AiSearchIngestPagesRequestPagesInner.md) |  | 

## Example

```python
from quantcdn.models.ai_search_ingest_pages_request import AiSearchIngestPagesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchIngestPagesRequest from a JSON string
ai_search_ingest_pages_request_instance = AiSearchIngestPagesRequest.from_json(json)
# print the JSON string representation of the object
print(AiSearchIngestPagesRequest.to_json())

# convert the object into a dict
ai_search_ingest_pages_request_dict = ai_search_ingest_pages_request_instance.to_dict()
# create an instance of AiSearchIngestPagesRequest from a dict
ai_search_ingest_pages_request_from_dict = AiSearchIngestPagesRequest.from_dict(ai_search_ingest_pages_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


