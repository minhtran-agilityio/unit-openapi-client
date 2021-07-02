# openapi_client.ApplicationsApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_business**](ApplicationsApi.md#create_business) | **POST** /applications | Create Business
[**get**](ApplicationsApi.md#get) | **GET** /applications/8 | Get
[**getall**](ApplicationsApi.md#getall) | **GET** /applications | Get all
[**upload_document**](ApplicationsApi.md#upload_document) | **PUT** /applications/5/documents/2 | Upload Document
[**upload_document_back**](ApplicationsApi.md#upload_document_back) | **PUT** /applications/5/documents/2/back | Upload Document Back


# **create_business**
> Model200 create_business(content_type, body)

Create Business

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import applications_api
from openapi_client.model.model200 import Model200
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
    api_instance = applications_api.ApplicationsApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
  "data": {
    "type": "businessApplication",
    "attributes": {
      "name": "Acme Inc.",
      "address": {
        "street": "1600 Pennsylvania Avenue Northwest",
        "city": "Washington",
        "state": "CA",
        "postalCode": "20500",
        "country": "US"
      },
      "phone": {
        "countryCode": "1",
        "number": "9294723497"
      },
      "stateOfIncorporation": "CA",
      "entityType": "Corporation",
      "ein": "123456789",
      "officer": {
        "fullName": {
          "first": "Jone",
          "last": "Doe"
        },
        "dateOfBirth": "2012-05-05",
        "ssn": "000000005",
        "email": "jone.doe@unit-finance.com",
        "phone": {
          "countryCode": "1",
          "number": "2025550108"
        },
        "address": {
          "street": "950 Allerton Street",
          "city": "Redwood City",
          "state": "CA",
          "postalCode": "94063",
          "country": "US"
        }
      },
      "contact": {
        "fullName": {
          "first": "Jone",
          "last": "Doe"
        },
        "email": "jone.doe@unit-finance.com",
        "phone": {
          "countryCode": "1",
          "number": "2025550108"
        }
      },
      "beneficialOwners": [
        {
          "fullName": {
            "first": "James",
            "last": "Smith"
          },
          "dateOfBirth": "2012-04-05",
          "ssn": "574567625",
          "email": "james@unit-finance.com",
          "phone": {
            "countryCode": "1",
            "number": "2025550127"
          },
          "address": {
            "street": "650 Allerton Street",
            "city": "Redwood City",
            "state": "CA",
            "postalCode": "94063",
            "country": "US"
          }
        },
        {
          "fullName": {
            "first": "Richard",
            "last": "Hendricks"
          },
          "dateOfBirth": "2012-04-03",
          "ssn": "574572795",
          "email": "richard@unit-finance.com",
          "phone": {
            "countryCode": "1",
            "number": "2025550158"
          },
          "address": {
            "street": "470 Allerton Street",
            "city": "Redwood City",
            "state": "CA",
            "postalCode": "94063",
            "country": "US"
          }
        }
      ]
    }
  }
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Create Business
        api_response = api_instance.create_business(content_type, body)
        pprint(api_response)
    except openapi_client.ApiException as e:
        print("Exception when calling ApplicationsApi->create_business: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **content_type** | **str**|  |
 **body** | **str**|  |

### Return type

[**Model200**](Model200.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/vnd.api+json
 - **Accept**: application/vnd.api+json; charset=utf-8


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Create Business |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get**
> get()

Get

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import applications_api
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
    api_instance = applications_api.ApplicationsApi(api_client)

    # example, this endpoint has no required or optional parameters
    try:
        # Get
        api_instance.get()
    except openapi_client.ApiException as e:
        print("Exception when calling ApplicationsApi->get: %s\n" % e)
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

# **getall**
> getall(page_limit, page_offset, include)

Get all

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import applications_api
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
    api_instance = applications_api.ApplicationsApi(api_client)
    page_limit = 3.14 # float | 
    page_offset = 3.14 # float | 
    include = "org" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Get all
        api_instance.getall(page_limit, page_offset, include)
    except openapi_client.ApiException as e:
        print("Exception when calling ApplicationsApi->getall: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_limit** | **float**|  |
 **page_offset** | **float**|  |
 **include** | **str**|  |

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

# **upload_document**
> upload_document(file)

Upload Document

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import applications_api
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
    api_instance = applications_api.ApplicationsApi(api_client)
    file = open('/path/to/file', 'rb') # file_type | 

    # example passing only required values which don't have defaults set
    try:
        # Upload Document
        api_instance.upload_document(file)
    except openapi_client.ApiException as e:
        print("Exception when calling ApplicationsApi->upload_document: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **file_type**|  |

### Return type

void (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_document_back**
> upload_document_back(file)

Upload Document Back

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import applications_api
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
    api_instance = applications_api.ApplicationsApi(api_client)
    file = open('/path/to/file', 'rb') # file_type | 

    # example passing only required values which don't have defaults set
    try:
        # Upload Document Back
        api_instance.upload_document_back(file)
    except openapi_client.ApiException as e:
        print("Exception when calling ApplicationsApi->upload_document_back: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **file_type**|  |

### Return type

void (empty response body)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

