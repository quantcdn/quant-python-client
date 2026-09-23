# OaiGetModel200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**object** | **str** |  | [optional] 
**created** | **int** |  | [optional] 
**owned_by** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.oai_get_model200_response import OaiGetModel200Response

# TODO update the JSON string below
json = "{}"
# create an instance of OaiGetModel200Response from a JSON string
oai_get_model200_response_instance = OaiGetModel200Response.from_json(json)
# print the JSON string representation of the object
print(OaiGetModel200Response.to_json())

# convert the object into a dict
oai_get_model200_response_dict = oai_get_model200_response_instance.to_dict()
# create an instance of OaiGetModel200Response from a dict
oai_get_model200_response_from_dict = OaiGetModel200Response.from_dict(oai_get_model200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


