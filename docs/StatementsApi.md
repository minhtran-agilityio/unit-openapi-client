# openapi_client.StatementsApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_statement_html**](StatementsApi.md#get_statement_html) | **GET** /statements/7/html | Get Statement HTML
[**getall0**](StatementsApi.md#getall0) | **GET** /statements/ | Get all


# **get_statement_html**
> get_statement_html()

Get Statement HTML

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import statements_api
from pprint import pprint
# Defining the host is optional and defaults to http://example.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://example.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearer
configuration = openapi_client.Configuration(
    access_token = 'YOUR_BEARER_TOKEN'
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = statements_api.StatementsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get Statement HTML
        api_instance.get_statement_html()
    except openapi_client.ApiException as e:
        print("Exception when calling StatementsApi->get_statement_html: %s\n" % e)
```


### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getall0**
> getall0(page_limit, page_offset)

Get all

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import statements_api
from pprint import pprint
# Defining the host is optional and defaults to http://example.com
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://example.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearer
configuration = openapi_client.Configuration(
    access_token = 'YOUR_BEARER_TOKEN'
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = statements_api.StatementsApi(api_client)
    page_limit = 3.14 # float | 
    page_offset = 3.14 # float | 

    # example passing only required values which don't have defaults set
    try:
        # Get all
        api_instance.getall0(page_limit, page_offset)
    except openapi_client.ApiException as e:
        print("Exception when calling StatementsApi->getall0: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_limit** | **float**|  |
 **page_offset** | **float**|  |

### Return type

void (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

