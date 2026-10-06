# DNSCreateRecordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name relative to the zone; @ denotes the apex | 
**type** | **str** |  | 
**value** | **str** |  | 
**ttl** | **int** |  | [optional] [default to 300]

## Example

```python
from quantcdn.models.dns_create_record_request import DNSCreateRecordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DNSCreateRecordRequest from a JSON string
dns_create_record_request_instance = DNSCreateRecordRequest.from_json(json)
# print the JSON string representation of the object
print(DNSCreateRecordRequest.to_json())

# convert the object into a dict
dns_create_record_request_dict = dns_create_record_request_instance.to_dict()
# create an instance of DNSCreateRecordRequest from a dict
dns_create_record_request_from_dict = DNSCreateRecordRequest.from_dict(dns_create_record_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


