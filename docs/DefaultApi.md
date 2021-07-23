# portainer_ce_api.DefaultApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**team_update**](DefaultApi.md#team_update) | **PUT** /team/{id} | Update a team
[**user_admin_init**](DefaultApi.md#user_admin_init) | **POST** /users/admin/init | Initialize administrator account


# **team_update**
> PortainerTeam team_update(id, body)

Update a team

Update a team. **Access policy**: administrator

### Example
```python
from __future__ import print_function
import time
import portainer_ce_api
from portainer_ce_api.rest import ApiException
from pprint import pprint

# Configure API key authorization: jwt
configuration = portainer_ce_api.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = portainer_ce_api.DefaultApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Team identifier
body = portainer_ce_api.TeamsTeamUpdatePayload() # TeamsTeamUpdatePayload | Team details

try:
    # Update a team
    api_response = api_instance.team_update(id, body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->team_update: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Team identifier | 
 **body** | [**TeamsTeamUpdatePayload**](TeamsTeamUpdatePayload.md)| Team details | 

### Return type

[**PortainerTeam**](PortainerTeam.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **user_admin_init**
> PortainerUser user_admin_init(body)

Initialize administrator account

Initialize the 'admin' user account. **Access policy**: public

### Example
```python
from __future__ import print_function
import time
import portainer_ce_api
from portainer_ce_api.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = portainer_ce_api.DefaultApi()
body = portainer_ce_api.UsersAdminInitPayload() # UsersAdminInitPayload | User details

try:
    # Initialize administrator account
    api_response = api_instance.user_admin_init(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DefaultApi->user_admin_init: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**UsersAdminInitPayload**](UsersAdminInitPayload.md)| User details | 

### Return type

[**PortainerUser**](PortainerUser.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

