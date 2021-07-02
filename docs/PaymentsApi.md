# openapi_client.PaymentsApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ach_payment_inlinecounterparty**](PaymentsApi.md#create_ach_payment_inlinecounterparty) | **POST** /payments | Create ACH Payment - Inline counterparty
[**get5**](PaymentsApi.md#get5) | **GET** /payments/1 | Get
[**getall4**](PaymentsApi.md#getall4) | **GET** /payments | Get all


# **create_ach_payment_inlinecounterparty**
> create_ach_payment_inlinecounterparty(content_type, body)

Create ACH Payment - Inline counterparty

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import payments_api
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
    api_instance = payments_api.PaymentsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"achPayment",
		"attributes": {
			"amount": 15000,
			"direction": "Credit",
			"description": "ACH PYMT",
            "counterparty": {
                "name": "April Oniel",
                "routingNumber": "812345678",
                "accountNumber": "1000000001",
                "accountType": "Checking"
            },
            "tags": {
                "by": "Igal"
            }
		},
		"relationships": {
			"account": {
				"data": {
					"type": "depositAccount",
					"id": "10000"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Create ACH Payment - Inline counterparty
        api_instance.create_ach_payment_inlinecounterparty(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling PaymentsApi->create_ach_payment_inlinecounterparty: %s\n" % e)
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

# **get5**
> get5()

Get

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import payments_api
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
    api_instance = payments_api.PaymentsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get
        api_instance.get5()
    except openapi_client.ApiException as e:
        print("Exception when calling PaymentsApi->get5: %s\n" % e)
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

# **getall4**
> getall4()

Get all

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import payments_api
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
    api_instance = payments_api.PaymentsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get all
        api_instance.getall4()
    except openapi_client.ApiException as e:
        print("Exception when calling PaymentsApi->getall4: %s\n" % e)
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

