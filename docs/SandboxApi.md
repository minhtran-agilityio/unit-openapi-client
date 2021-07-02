# openapi_client.SandboxApi

All URIs are relative to *http://example.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**_sandbox_activate_card**](SandboxApi.md#_sandbox_activate_card) | **POST** /sandbox/cards/8/activate | (Sandbox) Activate Card
[**_sandbox_approve_application**](SandboxApi.md#_sandbox_approve_application) | **POST** /sandbox/applications/10061/approve | (Sandbox) Approve Application
[**_sandbox_approve_document**](SandboxApi.md#_sandbox_approve_document) | **POST** /sandbox/applications/10061/documents/10/approve | (Sandbox) Approve Document
[**_sandbox_clear_ach_payment**](SandboxApi.md#_sandbox_clear_ach_payment) | **POST** /sandbox/ach/clear | (Sandbox) Clear ACH Payment
[**_sandbox_deny_application**](SandboxApi.md#_sandbox_deny_application) | **POST** /sandbox/applications/10061/deny | (Sandbox) Deny Application
[**_sandbox_reject_document**](SandboxApi.md#_sandbox_reject_document) | **POST** /sandbox/applications/10015/documents/8/reject | (Sandbox) Reject Document
[**_sandbox_return_ach_payment**](SandboxApi.md#_sandbox_return_ach_payment) | **POST** /sandbox/ach/return | (Sandbox) Return ACH Payment
[**_sandbox_simulate_atm_withdrawal**](SandboxApi.md#_sandbox_simulate_atm_withdrawal) | **POST** /sandbox/atm-withdrawals | (Sandbox) Simulate ATM Withdrawal
[**_sandbox_simulate_authorization**](SandboxApi.md#_sandbox_simulate_authorization) | **POST** /sandbox/authorizations | (Sandbox) Simulate Authorization
[**_sandbox_simulate_incoming_ach_payment**](SandboxApi.md#_sandbox_simulate_incoming_ach_payment) | **POST** /sandbox/payments | (Sandbox) Simulate Incoming ACH Payment
[**_sandbox_simulate_incoming_wire_payment**](SandboxApi.md#_sandbox_simulate_incoming_wire_payment) | **POST** /sandbox/wire-payments | (Sandbox) Simulate Incoming Wire Payment
[**_sandbox_simulate_purchase**](SandboxApi.md#_sandbox_simulate_purchase) | **POST** /sandbox/purchases | (Sandbox) Simulate Purchase
[**_sandbox_simulate_purchase_reversal**](SandboxApi.md#_sandbox_simulate_purchase_reversal) | **POST** /sandbox/reversals | (Sandbox) Simulate Purchase Reversal
[**_sandbox_transmit_ach_payment**](SandboxApi.md#_sandbox_transmit_ach_payment) | **POST** /sandbox/ach/transmit | (Sandbox) Transmit ACH Payment


# **_sandbox_activate_card**
> _sandbox_activate_card(content_type, body)

(Sandbox) Activate Card

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Activate Card
        api_instance._sandbox_activate_card(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_activate_card: %s\n" % e)
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

# **_sandbox_approve_application**
> _sandbox_approve_application(content_type, body)

(Sandbox) Approve Application

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
    "data": {
        "type": "applicationApprove",
        "attributes": {
            "reason": "sandbox"
        }
    }
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Approve Application
        api_instance._sandbox_approve_application(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_approve_application: %s\n" % e)
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

# **_sandbox_approve_document**
> _sandbox_approve_document(content_type, body)

(Sandbox) Approve Document

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = "" # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Approve Document
        api_instance._sandbox_approve_document(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_approve_document: %s\n" % e)
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

# **_sandbox_clear_ach_payment**
> _sandbox_clear_ach_payment(content_type, body)

(Sandbox) Clear ACH Payment

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"clearAchPayment",
		"relationships": {
			"payment": {
				"data": {
					"type": "achPayment",
					"id": "12"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Clear ACH Payment
        api_instance._sandbox_clear_ach_payment(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_clear_ach_payment: %s\n" % e)
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

# **_sandbox_deny_application**
> _sandbox_deny_application(content_type, body)

(Sandbox) Deny Application

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
    "data": {
        "type": "applicationDeny",
        "attributes": {
            "reason": "sandbox"
        }
    }
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Deny Application
        api_instance._sandbox_deny_application(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_deny_application: %s\n" % e)
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

# **_sandbox_reject_document**
> _sandbox_reject_document(content_type, body)

(Sandbox) Reject Document

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
    "data": {
        "type": "documentReject",
        "attributes": {
            "reasonCode": "PoorQuality",
            "reason": "other"
        }
    }
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Reject Document
        api_instance._sandbox_reject_document(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_reject_document: %s\n" % e)
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

# **_sandbox_return_ach_payment**
> _sandbox_return_ach_payment(content_type, body)

(Sandbox) Return ACH Payment

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"returnAchPayment",
		"relationships": {
			"payment": {
				"data": {
					"type": "achPayment",
					"id": "10"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Return ACH Payment
        api_instance._sandbox_return_ach_payment(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_return_ach_payment: %s\n" % e)
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

# **_sandbox_simulate_atm_withdrawal**
> _sandbox_simulate_atm_withdrawal(content_type, body)

(Sandbox) Simulate ATM Withdrawal

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"atmTransaction",
		"attributes": {
			"amount": 2500,
            "atmName": "HOME FED SAV BK",
            "atmLocation": "Cupertino, CA, US"
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
        # (Sandbox) Simulate ATM Withdrawal
        api_instance._sandbox_simulate_atm_withdrawal(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_simulate_atm_withdrawal: %s\n" % e)
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

# **_sandbox_simulate_authorization**
> _sandbox_simulate_authorization(content_type, body)

(Sandbox) Simulate Authorization

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"authorization",
		"attributes": {
			"amount": 2500,
            "cardLast4Digits": "0019",
			"merchantName": "Apple Inc.",
            "merchantType": 1000,
            "merchantLocation": "Cupertino, CA"
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
        # (Sandbox) Simulate Authorization
        api_instance._sandbox_simulate_authorization(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_simulate_authorization: %s\n" % e)
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

# **_sandbox_simulate_incoming_ach_payment**
> _sandbox_simulate_incoming_ach_payment(content_type, body)

(Sandbox) Simulate Incoming ACH Payment

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"achPayment",
		"attributes": {
			"amount": 500000,
			"direction": "Credit",
			"description": "Wrong Transaction"
		},
		"relationships": {
			"account": {
				"data": {
					"type": "depositAccount",
					"id": "10840"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Simulate Incoming ACH Payment
        api_instance._sandbox_simulate_incoming_ach_payment(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_simulate_incoming_ach_payment: %s\n" % e)
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

# **_sandbox_simulate_incoming_wire_payment**
> _sandbox_simulate_incoming_wire_payment(content_type, body)

(Sandbox) Simulate Incoming Wire Payment

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"wirePayment",
		"attributes": {
			"amount": 520000,
			"description": "Wire Payment from Sandbox"
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
        # (Sandbox) Simulate Incoming Wire Payment
        api_instance._sandbox_simulate_incoming_wire_payment(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_simulate_incoming_wire_payment: %s\n" % e)
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

# **_sandbox_simulate_purchase**
> _sandbox_simulate_purchase(content_type, body)

(Sandbox) Simulate Purchase

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"purchaseTransaction",
		"attributes": {
			"amount": 2500,
			"direction": "Debit",
			"merchantName": "Apple Inc.",
            "merchantType": 1000,
            "merchantLocation": "Cupertino, CA",
			"coordinates": {
				"longitude": 121.323,
				"latitude": -33.33323
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
        # (Sandbox) Simulate Purchase
        api_instance._sandbox_simulate_purchase(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_simulate_purchase: %s\n" % e)
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

# **_sandbox_simulate_purchase_reversal**
> _sandbox_simulate_purchase_reversal(content_type, body)

(Sandbox) Simulate Purchase Reversal

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"cardReversalTransaction",
		"attributes": {
			"amount": 2500
        },
		"relationships": {
			"account": {
				"data": {
					"type": "depositAccount",
					"id": "10001"
				}
			},
            "relatedTransaction": {
				"data": {
					"type": "transaction",
					"id": "150"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Simulate Purchase Reversal
        api_instance._sandbox_simulate_purchase_reversal(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_simulate_purchase_reversal: %s\n" % e)
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

# **_sandbox_transmit_ach_payment**
> _sandbox_transmit_ach_payment(content_type, body)

(Sandbox) Transmit ACH Payment

### Example

* Bearer Authentication (bearer):
```python
import time
import openapi_client
from openapi_client.api import sandbox_api
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
    api_instance = sandbox_api.SandboxApi(api_client)
    content_type = "application/vnd.api+json" # str | 
    body = '''{
	"data":{
		"type":"transmitAchPayment",
		"relationships": {
			"payment": {
				"data": {
					"type": "achPayment",
					"id": "14"
				}
			}
		}
	}
}''' # str | 

    # example passing only required values which don't have defaults set
    try:
        # (Sandbox) Transmit ACH Payment
        api_instance._sandbox_transmit_ach_payment(content_type, body)
    except openapi_client.ApiException as e:
        print("Exception when calling SandboxApi->_sandbox_transmit_ach_payment: %s\n" % e)
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

