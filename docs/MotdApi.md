# portainer_ce_api.MotdApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**motd_get**](MotdApi.md#motd_get) | **GET** /motd | fetches the message of the day


# **motd_get**
> MotdMotdResponse motd_get()

fetches the message of the day

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
api_instance = portainer_ce_api.MotdApi(portainer_ce_api.ApiClient(configuration))

try:
    # fetches the message of the day
    api_response = api_instance.motd_get()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MotdApi->motd_get: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MotdMotdResponse**](MotdMotdResponse.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

