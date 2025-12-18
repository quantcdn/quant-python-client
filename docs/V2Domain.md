# V2Domain


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Domain ID | 
**domain** | **str** | Domain name | 
**dns_engaged** | **int** | DNS engagement status. 1 indicates DNS is properly configured and engaged, 0 indicates DNS configuration is pending or incomplete. | 
**dns_validation_records** | [**List[V2DomainDnsValidationRecordsInner]**](V2DomainDnsValidationRecordsInner.md) | DNS validation records required for SSL certificate validation. Present for domains pending certificate validation. Each record contains the CNAME information needed to validate domain ownership. | [optional] 
**dns_go_live_records** | [**List[V2DomainDnsGoLiveRecordsInner]**](V2DomainDnsGoLiveRecordsInner.md) | DNS records required to route traffic to the CDN. These records differ based on domain type (apex vs subdomain). Present when the CDN is configured and ready to receive traffic. | [optional] 

## Example

```python
from quantcdn.models.v2_domain import V2Domain

# TODO update the JSON string below
json = "{}"
# create an instance of V2Domain from a JSON string
v2_domain_instance = V2Domain.from_json(json)
# print the JSON string representation of the object
print(V2Domain.to_json())

# convert the object into a dict
v2_domain_dict = v2_domain_instance.to_dict()
# create an instance of V2Domain from a dict
v2_domain_from_dict = V2Domain.from_dict(v2_domain_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


