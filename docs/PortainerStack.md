# PortainerStack

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint_id** | **int** | Endpoint identifier. Reference the endpoint that will be used for deployment | [optional] 
**entry_point** | **str** | Path to the Stack file | [optional] 
**env** | [**list[PortainerPair]**](PortainerPair.md) | A list of environment variables used during stack deployment | [optional] 
**id** | **int** | Stack Identifier | [optional] 
**name** | **str** | Stack name | [optional] 
**resource_control** | [**PortainerResourceControl**](PortainerResourceControl.md) |  | [optional] 
**status** | **int** | Stack status (1 - active, 2 - inactive) | [optional] 
**swarm_id** | **str** | Cluster identifier of the Swarm cluster where the stack is deployed | [optional] 
**type** | **int** | Stack type. 1 for a Swarm stack, 2 for a Compose stack | [optional] 
**created_by** | **str** | The username which created this stack | [optional] 
**creation_date** | **int** | The date in unix time when stack was created | [optional] 
**git_config** | [**GittypesRepoConfig**](GittypesRepoConfig.md) | The git config of this stack | [optional] 
**project_path** | **str** | Path on disk to the repository hosting the Stack file | [optional] 
**update_date** | **int** | The date in unix time when stack was last updated | [optional] 
**updated_by** | **str** | The username which last updated this stack | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


