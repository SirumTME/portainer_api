# portainer_ce_api.EdgeTemplatesApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**edge_template_list**](EdgeTemplatesApi.md#edge_template_list) | **GET** /edge_templates | Fetches the list of Edge Templates


# **edge_template_list**
> list[PortainerTemplate] edge_template_list()

Fetches the list of Edge Templates

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
api_instance = portainer_ce_api.EdgeTemplatesApi(portainer_ce_api.ApiClient(configuration))

try:
    # Fetches the list of Edge Templates
    api_response = api_instance.edge_template_list()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EdgeTemplatesApi->edge_template_list: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[PortainerTemplate]**](PortainerTemplate.md)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

