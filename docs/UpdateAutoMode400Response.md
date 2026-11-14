# UpdateAutoMode400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | 
**eligible** | [**AIAutoModeEligibility**](AIAutoModeEligibility.md) |  | [optional] 

## Example

```python
from quantcdn.models.update_auto_mode400_response import UpdateAutoMode400Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAutoMode400Response from a JSON string
update_auto_mode400_response_instance = UpdateAutoMode400Response.from_json(json)
# print the JSON string representation of the object
print(UpdateAutoMode400Response.to_json())

# convert the object into a dict
update_auto_mode400_response_dict = update_auto_mode400_response_instance.to_dict()
# create an instance of UpdateAutoMode400Response from a dict
update_auto_mode400_response_from_dict = UpdateAutoMode400Response.from_dict(update_auto_mode400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


