# AiSearchIngestPagesRequestPagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**title** | **str** |  | 
**content** | **str** |  | 
**content_type** | **str** |  | [optional] 
**fetched_at** | **str** |  | [optional] 
**pre_processed** | **bool** |  | [optional] 
**summary** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**topics** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.ai_search_ingest_pages_request_pages_inner import AiSearchIngestPagesRequestPagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchIngestPagesRequestPagesInner from a JSON string
ai_search_ingest_pages_request_pages_inner_instance = AiSearchIngestPagesRequestPagesInner.from_json(json)
# print the JSON string representation of the object
print(AiSearchIngestPagesRequestPagesInner.to_json())

# convert the object into a dict
ai_search_ingest_pages_request_pages_inner_dict = ai_search_ingest_pages_request_pages_inner_instance.to_dict()
# create an instance of AiSearchIngestPagesRequestPagesInner from a dict
ai_search_ingest_pages_request_pages_inner_from_dict = AiSearchIngestPagesRequestPagesInner.from_dict(ai_search_ingest_pages_request_pages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


