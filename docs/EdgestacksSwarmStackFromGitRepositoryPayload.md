# EdgestacksSwarmStackFromGitRepositoryPayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**compose_file_path_in_repository** | **str** | Path to the Stack file inside the Git repository | [optional] [default to 'docker-compose.yml']
**edge_groups** | **list[int]** | List of identifiers of EdgeGroups | [optional] 
**name** | **str** | Name of the stack | 
**repository_authentication** | **bool** | Use basic authentication to clone the Git repository | [optional] 
**repository_password** | **str** | Password used in basic authentication. Required when RepositoryAuthentication is true. | [optional] 
**repository_reference_name** | **str** | Reference name of a Git repository hosting the Stack file | [optional] 
**repository_url** | **str** | URL of a Git repository hosting the Stack file | 
**repository_username** | **str** | Username used in basic authentication. Required when RepositoryAuthentication is true. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


