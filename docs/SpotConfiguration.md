# SpotConfiguration

Spot instance strategy configuration for controlling cost vs reliability. Spot instances provide significant cost savings (~70%) but may be interrupted by AWS. Available for non-production environments.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**strategy** | **str** | Spot instance strategy. &#39;off&#39; &#x3D; On-Demand only (highest reliability, no savings). &#39;spot-only&#39; &#x3D; 100% Spot instances (~70% savings, default for non-prod). &#39;mixed-safe&#39; &#x3D; 50% Spot instances (~35% savings, requires multiple instances). &#39;mixed-aggressive&#39; &#x3D; 80% Spot instances (~56% savings, requires multiple instances). | [default to 'spot-only']

## Example

```python
from quantcdn.models.spot_configuration import SpotConfiguration

# TODO update the JSON string below
json = "{}"
# create an instance of SpotConfiguration from a JSON string
spot_configuration_instance = SpotConfiguration.from_json(json)
# print the JSON string representation of the object
print(SpotConfiguration.to_json())

# convert the object into a dict
spot_configuration_dict = spot_configuration_instance.to_dict()
# create an instance of SpotConfiguration from a dict
spot_configuration_from_dict = SpotConfiguration.from_dict(spot_configuration_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


