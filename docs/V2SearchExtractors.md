# V2SearchExtractors

XPath expressions that decide what each indexed page contributes to a search record. The defaults take the page body from the meta description, which indexes one sentence per page and matches nothing on body text, so a real deployment should set `content` to the page's main content region.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** | XPath for the record title | [optional] [default to '//h1[1]']
**content** | **str** | XPath for the record body | [optional] [default to '//meta[@name=\'description\'][1]/@content']
**summary** | **str** | XPath for the record summary | [optional] [default to '//meta[@name=\'description\'][1]/@content']
**image** | **str** | XPath for the record image | [optional] [default to '//meta[@property=\'og:image\'][1]/@content']

## Example

```python
from quantcdn.models.v2_search_extractors import V2SearchExtractors

# TODO update the JSON string below
json = "{}"
# create an instance of V2SearchExtractors from a JSON string
v2_search_extractors_instance = V2SearchExtractors.from_json(json)
# print the JSON string representation of the object
print(V2SearchExtractors.to_json())

# convert the object into a dict
v2_search_extractors_dict = v2_search_extractors_instance.to_dict()
# create an instance of V2SearchExtractors from a dict
v2_search_extractors_from_dict = V2SearchExtractors.from_dict(v2_search_extractors_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


