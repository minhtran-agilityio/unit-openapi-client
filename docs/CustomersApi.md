# openapi_client.CustomersApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_customer_bearer_token**](CustomersApi.md#create_customer_bearer_token) | **POST** /customers/10807/token | Create Customer Bearer Token
[**create_customer_bearer_token_verification**](CustomersApi.md#create_customer_bearer_token_verification) | **POST** /customers/10807/token/verification | Create Customer Bearer Token Verification
[**get1**](CustomersApi.md#get1) | **GET** /customers/10807 | Get
[**getall0**](CustomersApi.md#getall0) | **GET** /customers | Get all
[**patch_customer**](CustomersApi.md#patch_customer) | **PATCH** /customers/284 | Patch Customer


# **create_customer_bearer_token**
> create_customer_bearer_token(content_type, body)

Create Customer Bearer Token

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import customers_api
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
    api_instance = customers_api.CustomersApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"customerToken",
		"attributes": {
            "scope": "customers accounts payments payments-create counterparties counterparties-create",
            "verificationToken": "rahH2GBUTVKPCcpaBkQeenf1BflZ1O2Z4yhdgQEqFxLMU90IXkIWrAiUzxx54NxzKoOAWj6cNkenSTrEmapoOhIAAOzP/IKjy+4KMei0UnQlHxGrJXIvbbg2nPKeedBHdAmgF+eg7kNw4UO15d3ojC806sf67MNHnBSogHGNqw5CG+q0kkuGgfNWrXQ4ZMYZM27AUyV04aAHLdIhswukoL3L1JpLXsZy4cPWv5MnpBOmFWGO7Y6Y+XBmi3/SHs5LUZa8k5YLK2WT5nRECg==",
            "verificationCode": "177933"
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Create Customer Bearer Token
        api_instance.create_customer_bearer_token(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CustomersApi->create_customer_bearer_token: %s\n" % e)
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

# **create_customer_bearer_token_verification**
> create_customer_bearer_token_verification(content_type, body)

Create Customer Bearer Token Verification

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import customers_api
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
    api_instance = customers_api.CustomersApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"customerTokenVerification",
        "attributes": {
            "channel": "sms"
        },
        "relationships": {
            "org": {
                "data": {
                    "type": "org",
                    "id": "15"
                }
           }
        }
    }
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Create Customer Bearer Token Verification
        api_instance.create_customer_bearer_token_verification(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CustomersApi->create_customer_bearer_token_verification: %s\n" % e)
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

# **get1**
> get1()

Get

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import customers_api
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
    api_instance = customers_api.CustomersApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get
        api_instance.get1()
    except openapi_client.ApiException as e:
        print("Exception when calling CustomersApi->get1: %s\n" % e)
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
> getall0()

Get all

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import customers_api
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
    api_instance = customers_api.CustomersApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get all
        api_instance.getall0()
    except openapi_client.ApiException as e:
        print("Exception when calling CustomersApi->getall0: %s\n" % e)
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

# **patch_customer**
> patch_customer(content_type, body)

Patch Customer

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import customers_api
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
    api_instance = customers_api.CustomersApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type": "individualCustomer",
		"attributes": {
            "address": {
                "street": "5230 Newell Rd",
                "street2": null,
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94300",
                "country": "US"
            },
            "email": "richard2@piedpiper.com",
            "phone": {
                "countryCode": "1",
                "number": "1555555577"
            }
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Patch Customer
        api_instance.patch_customer(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CustomersApi->patch_customer: %s\n" % e)
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

