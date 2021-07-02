# openapi_client.CounterpartiesApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_counterparty_bankdetails**](CounterpartiesApi.md#create_counterparty_bankdetails) | **POST** /counterparties | Create Counterparty - Bank details
[**delete_counterparty**](CounterpartiesApi.md#delete_counterparty) | **DELETE** /counterparties/1 | Delete Counterparty
[**getall2**](CounterpartiesApi.md#getall2) | **GET** /counterparties/ | Get all


# **create_counterparty_bankdetails**
> create_counterparty_bankdetails(content_type, body)

Create Counterparty - Bank details

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import counterparties_api
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
    api_instance = counterparties_api.CounterpartiesApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
    "data": {
        "type": "achCounterparty",
        "attributes": {
            "name": "Joe Doe",
            "routingNumber": "123456789",
            "accountNumber": "123",
            "accountType": "Checking",
            "type": "Person"
        },
        "relationships": {
            "customer": {
                "data": {
                    "type": "customer",
                    "id": "10000"
                }
            }
        }
    }
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Create Counterparty - Bank details
        api_instance.create_counterparty_bankdetails(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CounterpartiesApi->create_counterparty_bankdetails: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **content_type** | **str**|  |
 **body** | **str**|  |

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

# **delete_counterparty**
> delete_counterparty()

Delete Counterparty

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import counterparties_api
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
    api_instance = counterparties_api.CounterpartiesApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Delete Counterparty
        api_instance.delete_counterparty()
    except openapi_client.ApiException as e:
        print("Exception when calling CounterpartiesApi->delete_counterparty: %s\n" % e)
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

# **getall2**
> getall2(page_limit, page_offset)

Get all

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import counterparties_api
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
    api_instance = counterparties_api.CounterpartiesApi(api_client)
    page_limit = 3.14 # float | 
    page_offset = 3.14 # float | 

    # example passing only required values which don't have defaults set
    try:
        # Get all
        api_instance.getall2(page_limit, page_offset)
    except openapi_client.ApiException as e:
        print("Exception when calling CounterpartiesApi->getall2: %s\n" % e)
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

