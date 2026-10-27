# PutApplicationMetadata400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**errors** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.put_application_metadata400_response import PutApplicationMetadata400Response

# TODO update the JSON string below
json = "{}"
# create an instance of PutApplicationMetadata400Response from a JSON string
put_application_metadata400_response_instance = PutApplicationMetadata400Response.from_json(json)
# print the JSON string representation of the object
print(PutApplicationMetadata400Response.to_json())

# convert the object into a dict
put_application_metadata400_response_dict = put_application_metadata400_response_instance.to_dict()
# create an instance of PutApplicationMetadata400Response from a dict
put_application_metadata400_response_from_dict = PutApplicationMetadata400Response.from_dict(put_application_metadata400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


