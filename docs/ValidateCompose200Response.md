# ValidateCompose200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**translated_compose_definition** | **object** | The translated internal compose definition format | 
**translation_warnings** | **List[str]** | Optional warnings encountered during translation | [optional] 

## Example

```python
from quantcdn.models.validate_compose200_response import ValidateCompose200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ValidateCompose200Response from a JSON string
validate_compose200_response_instance = ValidateCompose200Response.from_json(json)
# print the JSON string representation of the object
print(ValidateCompose200Response.to_json())

# convert the object into a dict
validate_compose200_response_dict = validate_compose200_response_instance.to_dict()
# create an instance of ValidateCompose200Response from a dict
validate_compose200_response_from_dict = ValidateCompose200Response.from_dict(validate_compose200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


