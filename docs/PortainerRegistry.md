# PortainerRegistry

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authentication** | **bool** | Is authentication against this registry enabled | [optional] 
**authorized_teams** | **list[int]** |  | [optional] 
**authorized_users** | **list[int]** | Deprecated fields Deprecated in DBVersion &#x3D;&#x3D; 18 | [optional] 
**gitlab** | [**PortainerGitlabRegistryData**](PortainerGitlabRegistryData.md) |  | [optional] 
**id** | **int** | Registry Identifier | [optional] 
**management_configuration** | [**PortainerRegistryManagementConfiguration**](PortainerRegistryManagementConfiguration.md) |  | [optional] 
**name** | **str** | Registry Name | [optional] 
**password** | **str** | Password used to authenticate against this registry | [optional] 
**quay** | [**PortainerQuayRegistryData**](PortainerQuayRegistryData.md) |  | [optional] 
**team_access_policies** | [**PortainerTeamAccessPolicies**](PortainerTeamAccessPolicies.md) |  | [optional] 
**type** | **int** | Registry Type (1 - Quay, 2 - Azure, 3 - Custom, 4 - Gitlab) | [optional] 
**url** | **str** | URL or IP address of the Docker registry | [optional] 
**user_access_policies** | [**PortainerUserAccessPolicies**](PortainerUserAccessPolicies.md) |  | [optional] 
**username** | **str** | Username used to authenticate against this registry | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


