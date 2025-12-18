# ApplicationDatabase

Database configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rds_instance_identifier** | **str** | RDS instance identifier | [optional] 
**rds_instance_endpoint** | **str** | RDS instance endpoint address | [optional] 
**rds_instance_engine** | **str** | Database engine | [optional] 
**rds_instance_status** | **str** | RDS instance status | [optional] 

## Example

```python
from quantcdn.models.application_database import ApplicationDatabase

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationDatabase from a JSON string
application_database_instance = ApplicationDatabase.from_json(json)
# print the JSON string representation of the object
print(ApplicationDatabase.to_json())

# convert the object into a dict
application_database_dict = application_database_instance.to_dict()
# create an instance of ApplicationDatabase from a dict
application_database_from_dict = ApplicationDatabase.from_dict(application_database_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


