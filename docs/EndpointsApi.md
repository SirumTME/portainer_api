# portainer_ce_api.EndpointsApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**endpoint_create**](EndpointsApi.md#endpoint_create) | **POST** /endpoints | Create a new endpoint
[**endpoint_delete**](EndpointsApi.md#endpoint_delete) | **DELETE** /endpoints/{id} | Remove an endpoint
[**endpoint_inspect**](EndpointsApi.md#endpoint_inspect) | **GET** /endpoints/{id} | Inspect an endpoint
[**endpoint_list**](EndpointsApi.md#endpoint_list) | **GET** /endpoints | List endpoints
[**endpoint_settings_update**](EndpointsApi.md#endpoint_settings_update) | **PUT** /api/endpoints/:id/settings | Update settings for an endpoint
[**endpoint_snapshot**](EndpointsApi.md#endpoint_snapshot) | **POST** /endpoints/{id}/snapshot | Snapshots an endpoint
[**endpoint_snapshots**](EndpointsApi.md#endpoint_snapshots) | **POST** /endpoints/snapshot | Snapshot all endpoints
[**endpoint_status_inspect**](EndpointsApi.md#endpoint_status_inspect) | **GET** /endpoints/{id}/status | Get endpoint status
[**endpoint_update**](EndpointsApi.md#endpoint_update) | **PUT** /endpoints/{id} | Update an endpoint
[**endpoints_id_edge_jobs_job_id_logs_post**](EndpointsApi.md#endpoints_id_edge_jobs_job_id_logs_post) | **POST** /endpoints/{id}/edge/jobs/{jobID}/logs | Inspect an EdgeJob Log
[**endpoints_id_edge_stacks_stack_id_get**](EndpointsApi.md#endpoints_id_edge_stacks_stack_id_get) | **GET** /endpoints/{id}/edge/stacks/{stackId} | Inspect an Edge Stack for an Endpoint


# **endpoint_create**
> PortainerEndpoint endpoint_create(name, endpoint_creation_type, url=url, public_url=public_url, group_id=group_id, tls=tls, tls_skip_verify=tls_skip_verify, tls_skip_client_verify=tls_skip_client_verify, tlsca_cert_file=tlsca_cert_file, tls_cert_file=tls_cert_file, tls_key_file=tls_key_file, azure_application_id=azure_application_id, azure_tenant_id=azure_tenant_id, azure_authentication_key=azure_authentication_key, tag_i_ds=tag_i_ds, edge_checkin_interval=edge_checkin_interval)

Create a new endpoint

Create a new endpoint that will be used to manage an environment. **Access policy**: administrator

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
name = 'name_example' # str | Name that will be used to identify this endpoint (example: my-endpoint)
endpoint_creation_type = 56 # int | Environment type. Value must be one of: 1 (Local Docker environment), 2 (Agent environment), 3 (Azure environment), 4 (Edge agent environment) or 5 (Local Kubernetes Environment
url = 'url_example' # str | URL or IP address of a Docker host (example: docker.mydomain.tld:2375). Defaults to local if not specified (Linux: /var/run/docker.sock, Windows: //./pipe/docker_engine) (optional)
public_url = 'public_url_example' # str | URL or IP address where exposed containers will be reachable. Defaults to URL if not specified (example: docker.mydomain.tld:2375) (optional)
group_id = 56 # int | Endpoint group identifier. If not specified will default to 1 (unassigned). (optional)
tls = true # bool | Require TLS to connect against this endpoint (optional)
tls_skip_verify = true # bool | Skip server verification when using TLS (optional)
tls_skip_client_verify = true # bool | Skip client verification when using TLS (optional)
tlsca_cert_file = '/path/to/file.txt' # file | TLS CA certificate file (optional)
tls_cert_file = '/path/to/file.txt' # file | TLS client certificate file (optional)
tls_key_file = '/path/to/file.txt' # file | TLS client key file (optional)
azure_application_id = 'azure_application_id_example' # str | Azure application ID. Required if endpoint type is set to 3 (optional)
azure_tenant_id = 'azure_tenant_id_example' # str | Azure tenant ID. Required if endpoint type is set to 3 (optional)
azure_authentication_key = 'azure_authentication_key_example' # str | Azure authentication key. Required if endpoint type is set to 3 (optional)
tag_i_ds = [56] # list[int] | List of tag identifiers to which this endpoint is associated (optional)
edge_checkin_interval = 56 # int | The check in interval for edge agent (in seconds) (optional)

try:
    # Create a new endpoint
    api_response = api_instance.endpoint_create(name, endpoint_creation_type, url=url, public_url=public_url, group_id=group_id, tls=tls, tls_skip_verify=tls_skip_verify, tls_skip_client_verify=tls_skip_client_verify, tlsca_cert_file=tlsca_cert_file, tls_cert_file=tls_cert_file, tls_key_file=tls_key_file, azure_application_id=azure_application_id, azure_tenant_id=azure_tenant_id, azure_authentication_key=azure_authentication_key, tag_i_ds=tag_i_ds, edge_checkin_interval=edge_checkin_interval)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_create: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| Name that will be used to identify this endpoint (example: my-endpoint) | 
 **endpoint_creation_type** | **int**| Environment type. Value must be one of: 1 (Local Docker environment), 2 (Agent environment), 3 (Azure environment), 4 (Edge agent environment) or 5 (Local Kubernetes Environment | 
 **url** | **str**| URL or IP address of a Docker host (example: docker.mydomain.tld:2375). Defaults to local if not specified (Linux: /var/run/docker.sock, Windows: //./pipe/docker_engine) | [optional] 
 **public_url** | **str**| URL or IP address where exposed containers will be reachable. Defaults to URL if not specified (example: docker.mydomain.tld:2375) | [optional] 
 **group_id** | **int**| Endpoint group identifier. If not specified will default to 1 (unassigned). | [optional] 
 **tls** | **bool**| Require TLS to connect against this endpoint | [optional] 
 **tls_skip_verify** | **bool**| Skip server verification when using TLS | [optional] 
 **tls_skip_client_verify** | **bool**| Skip client verification when using TLS | [optional] 
 **tlsca_cert_file** | **file**| TLS CA certificate file | [optional] 
 **tls_cert_file** | **file**| TLS client certificate file | [optional] 
 **tls_key_file** | **file**| TLS client key file | [optional] 
 **azure_application_id** | **str**| Azure application ID. Required if endpoint type is set to 3 | [optional] 
 **azure_tenant_id** | **str**| Azure tenant ID. Required if endpoint type is set to 3 | [optional] 
 **azure_authentication_key** | **str**| Azure authentication key. Required if endpoint type is set to 3 | [optional] 
 **tag_i_ds** | [**list[int]**](int.md)| List of tag identifiers to which this endpoint is associated | [optional] 
 **edge_checkin_interval** | **int**| The check in interval for edge agent (in seconds) | [optional] 

### Return type

[**PortainerEndpoint**](PortainerEndpoint.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_delete**
> endpoint_delete(id)

Remove an endpoint

Remove an endpoint. **Access policy**: administrator

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Endpoint identifier

try:
    # Remove an endpoint
    api_instance.endpoint_delete(id)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_delete: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Endpoint identifier | 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_inspect**
> PortainerEndpoint endpoint_inspect(id)

Inspect an endpoint

Retrieve details about an endpoint. **Access policy**: restricted

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Endpoint identifier

try:
    # Inspect an endpoint
    api_response = api_instance.endpoint_inspect(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_inspect: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Endpoint identifier | 

### Return type

[**PortainerEndpoint**](PortainerEndpoint.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_list**
> list[PortainerEndpoint] endpoint_list(start=start, search=search, group_id=group_id, limit=limit, type=type, tag_ids=tag_ids, tags_partial_match=tags_partial_match, endpoint_ids=endpoint_ids)

List endpoints

List all endpoints based on the current user authorizations. Will return all endpoints if using an administrator account otherwise it will only return authorized endpoints. **Access policy**: restricted

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
start = 56 # int | Start searching from (optional)
search = 'search_example' # str | Search query (optional)
group_id = 56 # int | List endpoints of this group (optional)
limit = 56 # int | Limit results to this value (optional)
type = 56 # int | List endpoints of this type (optional)
tag_ids = [56] # list[int] | search endpoints with these tags (depends on tagsPartialMatch) (optional)
tags_partial_match = true # bool | If true, will return endpoint which has one of tagIds, if false (or missing) will return only endpoints that has all the tags (optional)
endpoint_ids = [56] # list[int] | will return only these endpoints (optional)

try:
    # List endpoints
    api_response = api_instance.endpoint_list(start=start, search=search, group_id=group_id, limit=limit, type=type, tag_ids=tag_ids, tags_partial_match=tags_partial_match, endpoint_ids=endpoint_ids)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **int**| Start searching from | [optional] 
 **search** | **str**| Search query | [optional] 
 **group_id** | **int**| List endpoints of this group | [optional] 
 **limit** | **int**| Limit results to this value | [optional] 
 **type** | **int**| List endpoints of this type | [optional] 
 **tag_ids** | [**list[int]**](int.md)| search endpoints with these tags (depends on tagsPartialMatch) | [optional] 
 **tags_partial_match** | **bool**| If true, will return endpoint which has one of tagIds, if false (or missing) will return only endpoints that has all the tags | [optional] 
 **endpoint_ids** | [**list[int]**](int.md)| will return only these endpoints | [optional] 

### Return type

[**list[PortainerEndpoint]**](PortainerEndpoint.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_settings_update**
> PortainerEndpoint endpoint_settings_update(id, body)

Update settings for an endpoint

Update settings for an endpoint. **Access policy**: administrator

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Endpoint identifier
body = portainer_ce_api.EndpointsEndpointSettingsUpdatePayload() # EndpointsEndpointSettingsUpdatePayload | Endpoint details

try:
    # Update settings for an endpoint
    api_response = api_instance.endpoint_settings_update(id, body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_settings_update: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Endpoint identifier | 
 **body** | [**EndpointsEndpointSettingsUpdatePayload**](EndpointsEndpointSettingsUpdatePayload.md)| Endpoint details | 

### Return type

[**PortainerEndpoint**](PortainerEndpoint.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_snapshot**
> endpoint_snapshot(id)

Snapshots an endpoint

Snapshots an endpoint **Access policy**: restricted

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Endpoint identifier

try:
    # Snapshots an endpoint
    api_instance.endpoint_snapshot(id)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_snapshot: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Endpoint identifier | 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_snapshots**
> endpoint_snapshots()

Snapshot all endpoints

Snapshot all endpoints **Access policy**: administrator

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))

try:
    # Snapshot all endpoints
    api_instance.endpoint_snapshots()
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_snapshots: %s\n" % e)
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

# **endpoint_status_inspect**
> EndpointsEndpointStatusInspectResponse endpoint_status_inspect(id)

Get endpoint status

Endpoint for edge agent to check status of environment **Access policy**: restricted only to Edge endpoints

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Endpoint identifier

try:
    # Get endpoint status
    api_response = api_instance.endpoint_status_inspect(id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_status_inspect: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Endpoint identifier | 

### Return type

[**EndpointsEndpointStatusInspectResponse**](EndpointsEndpointStatusInspectResponse.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoint_update**
> PortainerEndpoint endpoint_update(id, body)

Update an endpoint

Update an endpoint. **Access policy**: administrator

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
api_instance = portainer_ce_api.EndpointsApi(portainer_ce_api.ApiClient(configuration))
id = 56 # int | Endpoint identifier
body = portainer_ce_api.EndpointsEndpointUpdatePayload() # EndpointsEndpointUpdatePayload | Endpoint details

try:
    # Update an endpoint
    api_response = api_instance.endpoint_update(id, body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoint_update: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Endpoint identifier | 
 **body** | [**EndpointsEndpointUpdatePayload**](EndpointsEndpointUpdatePayload.md)| Endpoint details | 

### Return type

[**PortainerEndpoint**](PortainerEndpoint.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoints_id_edge_jobs_job_id_logs_post**
> endpoints_id_edge_jobs_job_id_logs_post(id, job_id)

Inspect an EdgeJob Log

### Example
```python
from __future__ import print_function
import time
import portainer_ce_api
from portainer_ce_api.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = portainer_ce_api.EndpointsApi()
id = 'id_example' # str | Endpoint Id
job_id = 'job_id_example' # str | Job Id

try:
    # Inspect an EdgeJob Log
    api_instance.endpoints_id_edge_jobs_job_id_logs_post(id, job_id)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoints_id_edge_jobs_job_id_logs_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Endpoint Id | 
 **job_id** | **str**| Job Id | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **endpoints_id_edge_stacks_stack_id_get**
> EndpointedgeConfigResponse endpoints_id_edge_stacks_stack_id_get(id, stack_id)

Inspect an Edge Stack for an Endpoint

### Example
```python
from __future__ import print_function
import time
import portainer_ce_api
from portainer_ce_api.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = portainer_ce_api.EndpointsApi()
id = 'id_example' # str | Endpoint Id
stack_id = 'stack_id_example' # str | EdgeStack Id

try:
    # Inspect an Edge Stack for an Endpoint
    api_response = api_instance.endpoints_id_edge_stacks_stack_id_get(id, stack_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EndpointsApi->endpoints_id_edge_stacks_stack_id_get: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Endpoint Id | 
 **stack_id** | **str**| EdgeStack Id | 

### Return type

[**EndpointedgeConfigResponse**](EndpointedgeConfigResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

