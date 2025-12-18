# V1PingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**config** | **object** | Configuration associated with a project | [optional] 
**project** | **str** | The project machine name | [optional] 

## Example

```python
from quantcdn.models.v1_ping_response import V1PingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1PingResponse from a JSON string
v1_ping_response_instance = V1PingResponse.from_json(json)
# print the JSON string representation of the object
print(V1PingResponse.to_json())

# convert the object into a dict
v1_ping_response_dict = v1_ping_response_instance.to_dict()
# create an instance of V1PingResponse from a dict
v1_ping_response_from_dict = V1PingResponse.from_dict(v1_ping_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


