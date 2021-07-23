# portainer_ce_api.BackupApi

All URIs are relative to *http://localhost/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**backup**](BackupApi.md#backup) | **POST** /backup | Creates an archive with a system data snapshot that could be used to restore the system.
[**restore**](BackupApi.md#restore) | **POST** /restore | Triggers a system restore using provided backup file


# **backup**
> backup(password=password)

Creates an archive with a system data snapshot that could be used to restore the system.

Creates an archive with a system data snapshot that could be used to restore the system. **Access policy**: admin

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
api_instance = portainer_ce_api.BackupApi(portainer_ce_api.ApiClient(configuration))
password = 'password_example' # str | Password to encrypt the backup with (optional)

try:
    # Creates an archive with a system data snapshot that could be used to restore the system.
    api_instance.backup(password=password)
except ApiException as e:
    print("Exception when calling BackupApi->backup: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **password** | **str**| Password to encrypt the backup with | [optional] 

### Return type

void (empty response body)

### Authorization

[jwt](../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore**
> restore(file_content, file_name, password=password)

Triggers a system restore using provided backup file

Triggers a system restore using provided backup file **Access policy**: public

### Example
```python
from __future__ import print_function
import time
import portainer_ce_api
from portainer_ce_api.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = portainer_ce_api.BackupApi()
file_content = [portainer_ce_api.list[int]()] # list[int] | Content of the backup
file_name = 'file_name_example' # str | File name
password = 'password_example' # str | Password to decrypt the backup with (optional)

try:
    # Triggers a system restore using provided backup file
    api_instance.restore(file_content, file_name, password=password)
except ApiException as e:
    print("Exception when calling BackupApi->restore: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_content** | **list[int]**| Content of the backup | 
 **file_name** | **str**| File name | 
 **password** | **str**| Password to decrypt the backup with | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

