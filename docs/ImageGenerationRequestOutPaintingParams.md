# ImageGenerationRequestOutPaintingParams

Parameters for OUTPAINTING task

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image** | **bytearray** |  | [optional] 
**mask_image** | **bytearray** |  | [optional] 
**mask_prompt** | **str** |  | [optional] 
**out_painting_mode** | **str** |  | [optional] [default to 'DEFAULT']
**text** | **str** |  | [optional] 
**negative_text** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.image_generation_request_out_painting_params import ImageGenerationRequestOutPaintingParams

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequestOutPaintingParams from a JSON string
image_generation_request_out_painting_params_instance = ImageGenerationRequestOutPaintingParams.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequestOutPaintingParams.to_json())

# convert the object into a dict
image_generation_request_out_painting_params_dict = image_generation_request_out_painting_params_instance.to_dict()
# create an instance of ImageGenerationRequestOutPaintingParams from a dict
image_generation_request_out_painting_params_from_dict = ImageGenerationRequestOutPaintingParams.from_dict(image_generation_request_out_painting_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


