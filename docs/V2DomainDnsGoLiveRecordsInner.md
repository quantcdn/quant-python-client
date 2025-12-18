# V2DomainDnsGoLiveRecordsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | DNS record type (CNAME, A, or ALIAS) | [optional] 
**name** | **str** | DNS record name/host (@ for apex/root domains, subdomain name for subdomains) | [optional] 
**value** | **str** | DNS record value (IP addresses for A records, domain name for CNAME/ALIAS) | [optional] 
**description** | **str** | Human-readable instructions for configuring this DNS record | [optional] 

## Example

```python
from quantcdn.models.v2_domain_dns_go_live_records_inner import V2DomainDnsGoLiveRecordsInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2DomainDnsGoLiveRecordsInner from a JSON string
v2_domain_dns_go_live_records_inner_instance = V2DomainDnsGoLiveRecordsInner.from_json(json)
# print the JSON string representation of the object
print(V2DomainDnsGoLiveRecordsInner.to_json())

# convert the object into a dict
v2_domain_dns_go_live_records_inner_dict = v2_domain_dns_go_live_records_inner_instance.to_dict()
# create an instance of V2DomainDnsGoLiveRecordsInner from a dict
v2_domain_dns_go_live_records_inner_from_dict = V2DomainDnsGoLiveRecordsInner.from_dict(v2_domain_dns_go_live_records_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


