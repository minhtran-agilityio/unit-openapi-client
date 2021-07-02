# openapi_client.BatchReleaseApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**batch_release**](BatchReleaseApi.md#batch_release) | **POST** /batch-release | Batch Release


# **batch_release**
> batch_release(content_type, body)

Batch Release

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import batch_release_api
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
    api_instance = batch_release_api.BatchReleaseApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
 	"data":[
         {
		"type":"batchRelease",
		"attributes": {
            "senderName": "Richard Hendricks",
            "senderAccountNumber": "123456798",
            "amount": 3000,
            "description": "BATCH PYMT",
            "senderAddress": {
                "street": "5230 Newell Rd",
                "street2": null,
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94303",
                "country": "US"
            }
		},
		"relationships": {
            "batchAccount": {
                "data": {
                    "type": "batchAccount",
                    "id": "10096"
                }
			},
			"receiver": {
				"data": {
					"type": "depositAccount",
					"id": "10097"
				}
			}
		}
	},
    {
		"type":"batchRelease",
		"attributes": {
            "senderName": "Richard Hendricks",
            "senderAccountNumber": "123456798",
            "amount": 2000,
            "description": "BATCH PYMT",
            "senderAddress": {
                "street": "5230 Newell Rd",
                "street2": null,
                "city": "Palo Alto",
                "state": "CA",
                "postalCode": "94303",
                "country": "US"
            }
		},
		"relationships": {
            "batchAccount": {
                "data": {
                    "type": "batchAccount",
                    "id": "10096"
                }
			},
			"receiver": {
				"data": {
					"type": "depositAccount",
					"id": "10017"
				}
			}
		}
	}]  
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # Batch Release
        api_instance.batch_release(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling BatchReleaseApi->batch_release: %s\n" % e)
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

