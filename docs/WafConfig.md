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
**notify_slack** | **str** | Slack webhook URL for notifications. The deprecated write alias notify_slack_webhook is still accepted | [optional] 
**notify_slack_hits_rpm** | **int** | Minimum hits per minute to trigger Slack notification. Send a positive integer. 0, null or an empty string turns it off (reads back null). Other values return 400. The deprecated write alias notify_slack_rpm is still accepted | [optional] 
**notify_email** | **List[str]** | Email addresses for notifications | [optional] 
**httpbl** | [**WafConfigHttpbl**](WafConfigHttpbl.md) |  | [optional] 
**block_lists** | [**WafConfigBlockLists**](WafConfigBlockLists.md) |  | [optional] 
**thresholds** | [**List[WafConfigThresholdsInner]**](WafConfigThresholdsInner.md) | Rate limiting thresholds. Entries are merged by type on update: only the listed types change. A request without thresholds keeps the stored ones. To turn a limit off, send its type with mode disabled. rps, hits and minutes are integers of 1 or more; cooldown is 0 or more. Invalid values return 400. An empty list changes nothing. A request that sets notify_slack copies that webhook into every threshold that the same request does not give its own notify_slack. Deprecated write aliases, still accepted: ip_ratelimit_rps, ip_ratelimit_cooldown, ip_ratelimit_mode, header_ratelimit_rps, header_ratelimit_cooldown, header_ratelimit_value, header_ratelimit_mode, hit_ratelimit_hits, hit_ratelimit_minutes, hit_ratelimit_cooldown, hit_ratelimit_mode. When thresholds and an alias set the same value, thresholds wins. | [optional] 

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


