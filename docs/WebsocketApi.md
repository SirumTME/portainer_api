# portainer_ce_api.WebsocketApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**websocket_attach_get**](WebsocketApi.md#websocket_attach_get) | **GET** /websocket/attach | Attach a websocket
[**websocket_exec_get**](WebsocketApi.md#websocket_exec_get) | **GET** /websocket/exec | Execute a websocket
[**websocket_pod_get**](WebsocketApi.md#websocket_pod_get) | **GET** /websocket/pod | Execute a websocket on pod


# **websocket_attach_get**
> websocket_attach_get(endpoint_id, token, node_name=node_name)

Attach a websocket

If the nodeName query parameter is present, the request will be proxied to the underlying agent endpoint. If the nodeName query parameter is not specified, the request will be upgraded to the websocket protocol and an AttachStart operation HTTP request will be created and hijacked. Authentication and access is controlled via the mandatory token query parameter.

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
api_instance = portainer_ce_api.WebsocketApi(portainer_ce_api.ApiClient(configuration))
endpoint_id = 56 # int | endpoint ID of the endpoint where the resource is located
token = 'token_example' # str | JWT token used for authentication against this endpoint
node_name = 'node_name_example' # str | node name (optional)

try:
    # Attach a websocket
    api_instance.websocket_attach_get(endpoint_id, token, node_name=node_name)
except ApiException as e:
    print("Exception when calling WebsocketApi->websocket_attach_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint_id** | **int**| endpoint ID of the endpoint where the resource is located | 
 **token** | **str**| JWT token used for authentication against this endpoint | 
 **node_name** | **str**| node name | [optional] 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **websocket_exec_get**
> websocket_exec_get(endpoint_id, token, node_name=node_name)

Execute a websocket

If the nodeName query parameter is present, the request will be proxied to the underlying agent endpoint. If the nodeName query parameter is not specified, the request will be upgraded to the websocket protocol and an ExecStart operation HTTP request will be created and hijacked. Authentication and access is controlled via the mandatory token query parameter.

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
api_instance = portainer_ce_api.WebsocketApi(portainer_ce_api.ApiClient(configuration))
endpoint_id = 56 # int | endpoint ID of the endpoint where the resource is located
token = 'token_example' # str | JWT token used for authentication against this endpoint
node_name = 'node_name_example' # str | node name (optional)

try:
    # Execute a websocket
    api_instance.websocket_exec_get(endpoint_id, token, node_name=node_name)
except ApiException as e:
    print("Exception when calling WebsocketApi->websocket_exec_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint_id** | **int**| endpoint ID of the endpoint where the resource is located | 
 **token** | **str**| JWT token used for authentication against this endpoint | 
 **node_name** | **str**| node name | [optional] 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **websocket_pod_get**
> websocket_pod_get(endpoint_id, namespace, pod_name, container_name, command, token)

Execute a websocket on pod

The request will be upgraded to the websocket protocol. Authentication and access is controlled via the mandatory token query parameter.

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
api_instance = portainer_ce_api.WebsocketApi(portainer_ce_api.ApiClient(configuration))
endpoint_id = 56 # int | endpoint ID of the endpoint where the resource is located
namespace = 'namespace_example' # str | namespace where the container is located
pod_name = 'pod_name_example' # str | name of the pod containing the container
container_name = 'container_name_example' # str | name of the container
command = 'command_example' # str | command to execute in the container
token = 'token_example' # str | JWT token used for authentication against this endpoint

try:
    # Execute a websocket on pod
    api_instance.websocket_pod_get(endpoint_id, namespace, pod_name, container_name, command, token)
except ApiException as e:
    print("Exception when calling WebsocketApi->websocket_pod_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint_id** | **int**| endpoint ID of the endpoint where the resource is located | 
 **namespace** | **str**| namespace where the container is located | 
 **pod_name** | **str**| name of the pod containing the container | 
 **container_name** | **str**| name of the container | 
 **command** | **str**| command to execute in the container | 
 **token** | **str**| JWT token used for authentication against this endpoint | 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

