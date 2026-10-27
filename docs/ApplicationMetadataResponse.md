# ApplicationMetadataResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | **Dict[str, str]** | Free-form key/value metadata. Maximum 50 pairs. Keys are 1-128 characters, values 0-256 characters. Letters, digits, space and + - &#x3D; . _ : / @ only. Keys starting with &#39;quant:&#39; are reserved. | 

## Example

```python
from quantcdn.models.application_metadata_response import ApplicationMetadataResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationMetadataResponse from a JSON string
application_metadata_response_instance = ApplicationMetadataResponse.from_json(json)
# print the JSON string representation of the object
print(ApplicationMetadataResponse.to_json())

# convert the object into a dict
application_metadata_response_dict = application_metadata_response_instance.to_dict()
# create an instance of ApplicationMetadataResponse from a dict
application_metadata_response_from_dict = ApplicationMetadataResponse.from_dict(application_metadata_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


