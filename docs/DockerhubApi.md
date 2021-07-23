# portainer_ce_api.DockerhubApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**docker_hub_inspect**](DockerhubApi.md#docker_hub_inspect) | **GET** /dockerhub | Retrieve DockerHub information
[**docker_hub_update**](DockerhubApi.md#docker_hub_update) | **PUT** /dockerhub | Update DockerHub information


# **docker_hub_inspect**
> PortainerDockerHub docker_hub_inspect()

Retrieve DockerHub information

Use this endpoint to retrieve the information used to connect to the DockerHub **Access policy**: authenticated

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
api_instance = portainer_ce_api.DockerhubApi(portainer_ce_api.ApiClient(configuration))

try:
    # Retrieve DockerHub information
    api_response = api_instance.docker_hub_inspect()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DockerhubApi->docker_hub_inspect: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PortainerDockerHub**](PortainerDockerHub.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **docker_hub_update**
> docker_hub_update(body)

Update DockerHub information

Use this endpoint to update the information used to connect to the DockerHub **Access policy**: administrator

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
api_instance = portainer_ce_api.DockerhubApi(portainer_ce_api.ApiClient(configuration))
body = portainer_ce_api.DockerhubDockerhubUpdatePayload() # DockerhubDockerhubUpdatePayload | DockerHub information

try:
    # Update DockerHub information
    api_instance.docker_hub_update(body)
except ApiException as e:
    print("Exception when calling DockerhubApi->docker_hub_update: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DockerhubDockerhubUpdatePayload**](DockerhubDockerhubUpdatePayload.md)| DockerHub information | 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

