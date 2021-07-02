# openapi_client.CardsApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**close**](CardsApi.md#close) | **POST** /cards/41/close | Close
[**create_individual_debit_card**](CardsApi.md#create_individual_debit_card) | **POST** /cards | Create Individual Debit Card
[**freeze**](CardsApi.md#freeze) | **POST** /cards/41/freeze | Freeze
[**get12**](CardsApi.md#get12) | **GET** /cards/41 | Get
[**getall11**](CardsApi.md#getall11) | **GET** /cards/ | Get all
[**patch_busienss_debit_card**](CardsApi.md#patch_busienss_debit_card) | **PATCH** /cards/94 | Patch Busienss Debit Card
[**patch_individual_debit_card**](CardsApi.md#patch_individual_debit_card) | **PATCH** /cards/47 | Patch Individual Debit Card
[**report_lost**](CardsApi.md#report_lost) | **POST** /cards/41/report-lost | Report Lost
[**report_stolen**](CardsApi.md#report_stolen) | **POST** /cards/41/report-stolen | Report Stolen
[**unfreeze**](CardsApi.md#unfreeze) | **POST** /cards/41/unfreeze | Unfreeze


# **close**
> close(content_type, body)

Close

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Close
        api_instance.close(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->close: %s\n" % e)
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

# **create_individual_debit_card**
> create_individual_debit_card(content_type, body)

Create Individual Debit Card

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"individualDebitCard",
		"attributes": {
			"shippingAddress": {
                "street": "5230 Newell Rd",
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94303",
                "country": "US"
            }
		},
		"relationships": {
			"account": {
				"data": {
					"type": "depositAccount",
					"id": "10001"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Create Individual Debit Card
        api_instance.create_individual_debit_card(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->create_individual_debit_card: %s\n" % e)
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

# **freeze**
> freeze(content_type, body)

Freeze

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Freeze
        api_instance.freeze(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->freeze: %s\n" % e)
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

# **get12**
> get12()

Get

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get
        api_instance.get12()
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->get12: %s\n" % e)
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

# **getall11**
> getall11(page_limit, page_offset)

Get all

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    page_limit = 3.14 # float | 
    page_offset = 3.14 # float | 

    # example passing only required values which don't have defaults set
    try:
        # Get all
        api_instance.getall11(page_limit, page_offset)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->getall11: %s\n" % e)
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

# **patch_busienss_debit_card**
> patch_busienss_debit_card(content_type, body)

Patch Busienss Debit Card

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"businessDebitCard",
		"attributes": {
			"shippingAddress": {
                "street": "5230 Newell Rd",
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94301",
                "country": "US"
            },
            "address": {
                "street": "5231 Newell Rd",
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94301",
                "country": "US"
            },
            "email": "richard2@piedpiper.com",
            "phone": {
                "countryCode": "1",
                "number": "5555555566"
            }
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Patch Busienss Debit Card
        api_instance.patch_busienss_debit_card(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->patch_busienss_debit_card: %s\n" % e)
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

# **patch_individual_debit_card**
> patch_individual_debit_card(content_type, body)

Patch Individual Debit Card

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"individualDebitCard",
		"attributes": {
			"shippingAddress": {
                "street": "52351 Newell Rd",
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94304",
                "country": "US"
            }
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Patch Individual Debit Card
        api_instance.patch_individual_debit_card(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->patch_individual_debit_card: %s\n" % e)
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

# **report_lost**
> report_lost(content_type, body)

Report Lost

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Report Lost
        api_instance.report_lost(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->report_lost: %s\n" % e)
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

# **report_stolen**
> report_stolen(content_type, body)

Report Stolen

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Report Stolen
        api_instance.report_stolen(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->report_stolen: %s\n" % e)
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

# **unfreeze**
> unfreeze(content_type, body)

Unfreeze

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import cards_api
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
    api_instance = cards_api.CardsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Unfreeze
        api_instance.unfreeze(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling CardsApi->unfreeze: %s\n" % e)
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

