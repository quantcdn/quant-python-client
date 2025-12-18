# WafConfig

Web Application Firewall configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mode** | **str** | WAF operation mode | [optional] [default to 'report']
**paranoia_level** | **int** | OWASP paranoia level | [optional] [default to 1]
**allow_rules** | **List[str]** | WAF rule IDs to allow/whitelist | [optional] 
**allow_ip** | **List[str]** | IP addresses to allow | [optional] 
**block_ip** | **List[str]** | IP addresses to block | [optional] 
**block_asn** | **List[str]** | ASN numbers to block | [optional] 
**block_ua** | **List[str]** | User agent patterns to block | [optional] 
**block_referer** | **List[str]** | Referer patterns to block | [optional] 
**notify_slack** | **str** | Slack webhook URL for notifications | [optional] 
**notify_slack_hits_rpm** | **int** | Minimum hits per minute to trigger Slack notification | [optional] 
**notify_email** | **List[str]** | Email addresses for notifications | [optional] 
**httpbl** | [**WafConfigHttpbl**](WafConfigHttpbl.md) |  | [optional] 
**block_lists** | [**WafConfigBlockLists**](WafConfigBlockLists.md) |  | [optional] 
**thresholds** | [**List[WafConfigThresholdsInner]**](WafConfigThresholdsInner.md) | Rate limiting thresholds | [optional] 

## Example

```python
from quantcdn.models.waf_config import WafConfig

# TODO update the JSON string below
json = "{}"
# create an instance of WafConfig from a JSON string
waf_config_instance = WafConfig.from_json(json)
# print the JSON string representation of the object
print(WafConfig.to_json())

# convert the object into a dict
waf_config_dict = waf_config_instance.to_dict()
# create an instance of WafConfig from a dict
waf_config_from_dict = WafConfig.from_dict(waf_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


