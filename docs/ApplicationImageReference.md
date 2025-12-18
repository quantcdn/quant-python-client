# ApplicationImageReference

Image reference information

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Image type | [optional] 
**identifier** | **str** | Image identifier | [optional] 

## Example

```python
from quantcdn.models.application_image_reference import ApplicationImageReference

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationImageReference from a JSON string
application_image_reference_instance = ApplicationImageReference.from_json(json)
# print the JSON string representation of the object
print(ApplicationImageReference.to_json())

# convert the object into a dict
application_image_reference_dict = application_image_reference_instance.to_dict()
# create an instance of ApplicationImageReference from a dict
application_image_reference_from_dict = ApplicationImageReference.from_dict(application_image_reference_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


