# portainer_ce_api.TeamsApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**team_create**](TeamsApi.md#team_create) | **POST** /team | Create a new team
[**team_delete**](TeamsApi.md#team_delete) | **DELETE** /teams/{id} | Remove a team
[**team_inspect**](TeamsApi.md#team_inspect) | **GET** /teams/{id} | Inspect a team
[**team_list**](TeamsApi.md#team_list) | **GET** /teams | List teams


# **team_create**
> PortainerTeam team_create(body)

Create a new team

Create a new team. **Access policy**: administrator

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
api_instance = portainer_ce_api.TeamsApi(portainer_ce_api.ApiClient(configuration))
body = portainer_ce_api.TeamsTeamCreatePayload() # TeamsTeamCreatePayload | details

try:
    # Create a new team
    api_response = api_instance.team_create(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->team_create: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TeamsTeamCreatePayload**](TeamsTeamCreatePayload.md)| details | 

### Return type

[**PortainerTeam**](PortainerTeam.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **team_delete**
> team_delete()

Remove a team

Remove a team. **Access policy**: administrator

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
api_instance = portainer_ce_api.TeamsApi(portainer_ce_api.ApiClient(configuration))

try:
    # Remove a team
    api_instance.team_delete()
except ApiException as e:
    print("Exception when calling TeamsApi->team_delete: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **team_inspect**
> PortainerTeam team_inspect(id)

Inspect a team

Retrieve details about a team. Access is only available for administrator and leaders of that team. **Access policy**: restricted

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
api_instance = portainer_ce_api.TeamsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Team identifier

try:
    # Inspect a team
    api_response = api_instance.team_inspect(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->team_inspect: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Team identifier | 

### Return type

[**PortainerTeam**](PortainerTeam.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **team_list**
> list[PortainerTeam] team_list()

List teams

List teams. For non-administrator users, will only list the teams they are member of. **Access policy**: restricted

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
api_instance = portainer_ce_api.TeamsApi(portainer_ce_api.ApiClient(configuration))

try:
    # List teams
    api_response = api_instance.team_list()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamsApi->team_list: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[PortainerTeam]**](PortainerTeam.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

