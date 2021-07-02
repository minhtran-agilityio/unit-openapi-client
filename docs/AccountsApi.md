# openapi_client.AccountsApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_deposit_account**](AccountsApi.md#create_deposit_account) | **POST** /accounts | Create Deposit Account
[**get4**](AccountsApi.md#get4) | **GET** /accounts/10034 | Get
[**getallby_customer_id**](AccountsApi.md#getallby_customer_id) | **GET** /accounts | Get all by Customer Id


# **create_deposit_account**
> create_deposit_account(content_type, body)

Create Deposit Account

Remove 'balance' and 'hold' from the request

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import accounts_api
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
    api_instance = accounts_api.AccountsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
    "data": {
        "type": "depositAccount",
        "attributes": {
            "depositProduct": "revenue_bank",
            "tags": {
                "purpose": "checking"
            }
        },
        "relationships": {
            "customer": {
            	"data": {
                	"type": "customer",
                	"id": "10389"
            	}
            }
        }
    }
}''' # str | Remove 'balance' and 'hold' from the request

    # example passing only required values which don't have defaults set
    try:
        # Create Deposit Account
        api_instance.create_deposit_account(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling AccountsApi->create_deposit_account: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **content_type** | **str**|  |
 **body** | **str**| Remove &#39;balance&#39; and &#39;hold&#39; from the request |

### Return type

void (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/vnd.api+json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get4**
> get4()

Get

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import accounts_api
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
    api_instance = accounts_api.AccountsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get
        api_instance.get4()
    except openapi_client.ApiException as e:
        print("Exception when calling AccountsApi->get4: %s\n" % e)
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

# **getallby_customer_id**
> getallby_customer_id(filter_customer_id)

Get all by Customer Id

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import accounts_api
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
    api_instance = accounts_api.AccountsApi(api_client)
    filter_customer_id = 3.14 # float | 

    # example passing only required values which don't have defaults set
    try:
        # Get all by Customer Id
        api_instance.getallby_customer_id(filter_customer_id)
    except openapi_client.ApiException as e:
        print("Exception when calling AccountsApi->getallby_customer_id: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter_customer_id** | **float**|  |

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

