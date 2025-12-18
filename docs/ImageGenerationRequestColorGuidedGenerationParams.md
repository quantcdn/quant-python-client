# ImageGenerationRequestColorGuidedGenerationParams

Parameters for COLOR_GUIDED_GENERATION task

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**colors** | **List[str]** |  | [optional] 
**reference_image** | **bytearray** |  | [optional] 
**text** | **str** |  | [optional] 
**negative_text** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.image_generation_request_color_guided_generation_params import ImageGenerationRequestColorGuidedGenerationParams

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequestColorGuidedGenerationParams from a JSON string
image_generation_request_color_guided_generation_params_instance = ImageGenerationRequestColorGuidedGenerationParams.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequestColorGuidedGenerationParams.to_json())

# convert the object into a dict
image_generation_request_color_guided_generation_params_dict = image_generation_request_color_guided_generation_params_instance.to_dict()
# create an instance of ImageGenerationRequestColorGuidedGenerationParams from a dict
image_generation_request_color_guided_generation_params_from_dict = ImageGenerationRequestColorGuidedGenerationParams.from_dict(image_generation_request_color_guided_generation_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


