# portainer_ce_api.StatusApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**status_inspect**](StatusApi.md#status_inspect) | **GET** /status | Check Portainer status
[**status_inspect_version**](StatusApi.md#status_inspect_version) | **GET** /status/version | Check for portainer updates


# **status_inspect**
> PortainerStatus status_inspect()

Check Portainer status

Retrieve Portainer status **Access policy**: public

### Example
```python
from __future__ import print_function
import time
import portainer_ce_api
from portainer_ce_api.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = portainer_ce_api.StatusApi()

try:
    # Check Portainer status
    api_response = api_instance.status_inspect()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling StatusApi->status_inspect: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PortainerStatus**](PortainerStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **status_inspect_version**
> StatusInspectVersionResponse status_inspect_version()

Check for portainer updates

Check if portainer has an update available **Access policy**: authenticated

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
api_instance = portainer_ce_api.StatusApi(portainer_ce_api.ApiClient(configuration))

try:
    # Check for portainer updates
    api_response = api_instance.status_inspect_version()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling StatusApi->status_inspect_version: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**StatusInspectVersionResponse**](StatusInspectVersionResponse.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

