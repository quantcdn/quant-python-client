# OaiListModels200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**object** | **str** |  | [optional] 
**data** | [**List[OaiListModels200ResponseDataInner]**](OaiListModels200ResponseDataInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.oai_list_models200_response import OaiListModels200Response

# TODO update the JSON string below
json = "{}"
# create an instance of OaiListModels200Response from a JSON string
oai_list_models200_response_instance = OaiListModels200Response.from_json(json)
# print the JSON string representation of the object
print(OaiListModels200Response.to_json())

# convert the object into a dict
oai_list_models200_response_dict = oai_list_models200_response_instance.to_dict()
# create an instance of OaiListModels200Response from a dict
oai_list_models200_response_from_dict = OaiListModels200Response.from_dict(oai_list_models200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


