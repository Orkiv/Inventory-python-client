# InventoryClient.DefaultApi

All URIs are relative to *https://www.orkiv.com/i/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**all_get**](DefaultApi.md#all_get) | **GET** /all/ | 
[**categories_delete**](DefaultApi.md#categories_delete) | **DELETE** /categories/ | 
[**categories_post**](DefaultApi.md#categories_post) | **POST** /categories/ | 
[**categories_put**](DefaultApi.md#categories_put) | **PUT** /categories/ | 
[**item_add_post**](DefaultApi.md#item_add_post) | **POST** /item/add/ | 
[**item_addbulk_post**](DefaultApi.md#item_addbulk_post) | **POST** /item/addbulk/ | 
[**item_delete**](DefaultApi.md#item_delete) | **DELETE** /item/ | 
[**item_put**](DefaultApi.md#item_put) | **PUT** /item/ | 
[**items_count_post**](DefaultApi.md#items_count_post) | **POST** /items/count/ | 
[**items_post**](DefaultApi.md#items_post) | **POST** /items/ | 
[**itemsallfields_post**](DefaultApi.md#itemsallfields_post) | **POST** /items/?allfields | 
[**orders_post**](DefaultApi.md#orders_post) | **POST** /orders/ | 
[**query_post**](DefaultApi.md#query_post) | **POST** /query/ | 
[**queryallfields_post**](DefaultApi.md#queryallfields_post) | **POST** /query/?allfields | 
[**services_delete**](DefaultApi.md#services_delete) | **DELETE** /services/ | 
[**services_get**](DefaultApi.md#services_get) | **GET** /services/ | 
[**services_post**](DefaultApi.md#services_post) | **POST** /services/ | 
[**services_put**](DefaultApi.md#services_put) | **PUT** /services/ | 
[**write_delete**](DefaultApi.md#write_delete) | **DELETE** /write/ | 
[**write_post**](DefaultApi.md#write_post) | **POST** /write/ | 


# **all_get**
> list[InventoryGroup] all_get()



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()

try: 
    api_response = api_instance.all_get()
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->all_get: %s\n" % e
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[InventoryGroup]**](InventoryGroup.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **categories_delete**
> Response categories_delete(id)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | Id of category to remove

try: 
    api_response = api_instance.categories_delete(id)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->categories_delete: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Id of category to remove | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **categories_post**
> list[Category] categories_post(query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
query = InventoryClient.Dictionary() # Dictionary | Category to query against system (optional)

try: 
    api_response = api_instance.categories_post(query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->categories_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Dictionary**](Dictionary.md)| Category to query against system | [optional] 

### Return type

[**list[Category]**](Category.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **categories_put**
> Category categories_put(id, category)



If no ID is specified a new category will be created!

### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | category id to update.
category = InventoryClient.Category() # Category | New category information.

try: 
    api_response = api_instance.categories_put(id, category)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->categories_put: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| category id to update. | 
 **category** | [**Category**](Category.md)| New category information. | 

### Return type

[**Category**](Category.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **item_add_post**
> Item item_add_post(item)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
item = InventoryClient.Item() # Item | Item to create.

try: 
    api_response = api_instance.item_add_post(item)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->item_add_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **item** | [**Item**](Item.md)| Item to create. | 

### Return type

[**Item**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **item_addbulk_post**
> Response item_addbulk_post(items)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
items = [InventoryClient.Item()] # list[Item] | Items to create.

try: 
    api_response = api_instance.item_addbulk_post(items)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->item_addbulk_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **items** | [**list[Item]**](Item.md)| Items to create. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **item_delete**
> Response item_delete(id)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | item id to remove

try: 
    api_response = api_instance.item_delete(id)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->item_delete: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| item id to remove | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **item_put**
> Response item_put(id, item)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | item id to update.
item = InventoryClient.Dictionary() # Dictionary | New item information.

try: 
    api_response = api_instance.item_put(id, item)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->item_put: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| item id to update. | 
 **item** | [**Dictionary**](Dictionary.md)| New item information. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **items_count_post**
> float items_count_post(query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
query = InventoryClient.Dictionary() # Dictionary | Item to query against system. (optional)

try: 
    api_response = api_instance.items_count_post(query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->items_count_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Dictionary**](Dictionary.md)| Item to query against system. | [optional] 

### Return type

**float**

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **items_post**
> list[Item] items_post(query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
query = InventoryClient.Dictionary() # Dictionary | Item to query against system. (optional)

try: 
    api_response = api_instance.items_post(query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->items_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Dictionary**](Dictionary.md)| Item to query against system. | [optional] 

### Return type

[**list[Item]**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **itemsallfields_post**
> list[Dictionary] itemsallfields_post(query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
query = InventoryClient.Dictionary() # Dictionary | Item to query against system. (optional)

try: 
    api_response = api_instance.itemsallfields_post(query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->itemsallfields_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Dictionary**](Dictionary.md)| Item to query against system. | [optional] 

### Return type

[**list[Dictionary]**](Dictionary.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orders_post**
> list[Order] orders_post(query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
query = InventoryClient.Dictionary() # Dictionary | Order to query against system. (optional)

try: 
    api_response = api_instance.orders_post(query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->orders_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**Dictionary**](Dictionary.md)| Order to query against system. | [optional] 

### Return type

[**list[Order]**](Order.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **query_post**
> list[Item] query_post(page=page, categoryid=categoryid, sort=sort, search=search, minprice=minprice, maxprice=maxprice, query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
page = 3.4 # float | Current page index. (optional)
categoryid = 'categoryid_example' # str | Get items under specified category id. (optional)
sort = 'sort_example' # str | Comma delimited Sort string. ie ; +ordprice. Please use number based fields only (optional)
search = 'search_example' # str | Performs a regex pattern match against the items within your account (optional)
minprice = 3.4 # float | Min price in hundreds. (optional)
maxprice = 3.4 # float | Max price in hudreds. (optional)
query = InventoryClient.Dictionary() # Dictionary | Custom parameters to query against system. (optional)

try: 
    api_response = api_instance.query_post(page=page, categoryid=categoryid, sort=sort, search=search, minprice=minprice, maxprice=maxprice, query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->query_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Current page index. | [optional] 
 **categoryid** | **str**| Get items under specified category id. | [optional] 
 **sort** | **str**| Comma delimited Sort string. ie ; +ordprice. Please use number based fields only | [optional] 
 **search** | **str**| Performs a regex pattern match against the items within your account | [optional] 
 **minprice** | **float**| Min price in hundreds. | [optional] 
 **maxprice** | **float**| Max price in hudreds. | [optional] 
 **query** | [**Dictionary**](Dictionary.md)| Custom parameters to query against system. | [optional] 

### Return type

[**list[Item]**](Item.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **queryallfields_post**
> list[Dictionary] queryallfields_post(page=page, categoryid=categoryid, sort=sort, search=search, minprice=minprice, maxprice=maxprice, query=query)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
page = 3.4 # float | Current page index. (optional)
categoryid = 'categoryid_example' # str | Get items under specified category id. (optional)
sort = 'sort_example' # str | Comma delimited Sort string. ie ; +ordprice. Please use number based fields only (optional)
search = 'search_example' # str | Performs a regex pattern match against the items within your account (optional)
minprice = 3.4 # float | Min price in hundreds. (optional)
maxprice = 3.4 # float | Max price in hudreds. (optional)
query = InventoryClient.Dictionary() # Dictionary | Custom parameters to query against system. (optional)

try: 
    api_response = api_instance.queryallfields_post(page=page, categoryid=categoryid, sort=sort, search=search, minprice=minprice, maxprice=maxprice, query=query)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->queryallfields_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **float**| Current page index. | [optional] 
 **categoryid** | **str**| Get items under specified category id. | [optional] 
 **sort** | **str**| Comma delimited Sort string. ie ; +ordprice. Please use number based fields only | [optional] 
 **search** | **str**| Performs a regex pattern match against the items within your account | [optional] 
 **minprice** | **float**| Min price in hundreds. | [optional] 
 **maxprice** | **float**| Max price in hudreds. | [optional] 
 **query** | [**Dictionary**](Dictionary.md)| Custom parameters to query against system. | [optional] 

### Return type

[**list[Dictionary]**](Dictionary.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **services_delete**
> Response services_delete(id)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | ID of the service to update

try: 
    api_response = api_instance.services_delete(id)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->services_delete: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID of the service to update | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **services_get**
> list[Service] services_get()



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()

try: 
    api_response = api_instance.services_get()
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->services_get: %s\n" % e
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Service]**](Service.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **services_post**
> Service services_post(service)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
service = InventoryClient.Service() # Service | Service to create.

try: 
    api_response = api_instance.services_post(service)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->services_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service** | [**Service**](Service.md)| Service to create. | 

### Return type

[**Service**](Service.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **services_put**
> Response services_put(id, service)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | ID of the service to update
service = InventoryClient.Service() # Service | New service data to set.

try: 
    api_response = api_instance.services_put(id, service)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->services_put: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| ID of the service to update | 
 **service** | [**Service**](Service.md)| New service data to set. | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **write_delete**
> Response write_delete(id=id)



### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
id = 'id_example' # str | Will delete event attached to this serviceid (optional)

try: 
    api_response = api_instance.write_delete(id=id)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->write_delete: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Will delete event attached to this serviceid | [optional] 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **write_post**
> Response write_post(event_request)



Will ovveride the current event of the specified service.

### Example 
```python
import time
import InventoryClient
from InventoryClient.rest import ApiException
from pprint import pprint

# Configure API key authorization: APIKey
InventoryClient.configuration.api_key['APIKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['APIKey'] = 'Bearer'
# Configure API key authorization: AccountID
InventoryClient.configuration.api_key['accountid'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# InventoryClient.configuration.api_key_prefix['accountid'] = 'Bearer'

# create an instance of the API class
api_instance = InventoryClient.DefaultApi()
event_request = InventoryClient.EventRequest() # EventRequest | Event to upload

try: 
    api_response = api_instance.write_post(event_request)
    pprint(api_response)
except ApiException as e:
    print "Exception when calling DefaultApi->write_post: %s\n" % e
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_request** | [**EventRequest**](EventRequest.md)| Event to upload | 

### Return type

[**Response**](Response.md)

### Authorization

[APIKey](../README.md#APIKey), [AccountID](../README.md#AccountID)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

