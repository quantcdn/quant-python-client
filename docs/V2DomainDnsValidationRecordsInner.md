# V2DomainDnsValidationRecordsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | DNS record name (host/subdomain) | [optional] 
**type** | **str** | DNS record type (typically CNAME) | [optional] 
**value** | **str** | DNS record value to point to | [optional] 

## Example

```python
from quantcdn.models.v2_domain_dns_validation_records_inner import V2DomainDnsValidationRecordsInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2DomainDnsValidationRecordsInner from a JSON string
v2_domain_dns_validation_records_inner_instance = V2DomainDnsValidationRecordsInner.from_json(json)
# print the JSON string representation of the object
print(V2DomainDnsValidationRecordsInner.to_json())

# convert the object into a dict
v2_domain_dns_validation_records_inner_dict = v2_domain_dns_validation_records_inner_instance.to_dict()
# create an instance of V2DomainDnsValidationRecordsInner from a dict
v2_domain_dns_validation_records_inner_from_dict = V2DomainDnsValidationRecordsInner.from_dict(v2_domain_dns_validation_records_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


