# V2DomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** | Domain name | 

## Example

```python
from quantcdn.models.v2_domain_request import V2DomainRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2DomainRequest from a JSON string
v2_domain_request_instance = V2DomainRequest.from_json(json)
# print the JSON string representation of the object
print(V2DomainRequest.to_json())

# convert the object into a dict
v2_domain_request_dict = v2_domain_request_instance.to_dict()
# create an instance of V2DomainRequest from a dict
v2_domain_request_from_dict = V2DomainRequest.from_dict(v2_domain_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


