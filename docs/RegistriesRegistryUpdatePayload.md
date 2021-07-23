# RegistriesRegistryUpdatePayload

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authentication** | **bool** | Is authentication against this registry enabled | 
**name** | **str** | Name that will be used to identify this registry | 
**password** | **str** | Password used to authenticate against this registry. required when Authentication is true | [optional] 
**quay** | [**PortainerQuayRegistryData**](PortainerQuayRegistryData.md) |  | [optional] 
**team_access_policies** | [**PortainerTeamAccessPolicies**](PortainerTeamAccessPolicies.md) |  | [optional] 
**url** | **str** | URL or IP address of the Docker registry | 
**user_access_policies** | [**PortainerUserAccessPolicies**](PortainerUserAccessPolicies.md) |  | [optional] 
**username** | **str** | Username used to authenticate against this registry. Required when Authentication is true | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


