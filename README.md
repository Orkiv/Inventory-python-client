# InventoryClient
Orkiv Inventory API client 

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build date: 2016-08-04T12:36:52.479-04:00
- Build package: class io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/Orkiv/Inventory-python-client.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/Orkiv/Inventory-python-client.git`)

Then import the package:
```python
import InventoryClient 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import InventoryClient
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://www.orkiv.com/i/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**all_get**](docs/DefaultApi.md#all_get) | **GET** /all/ | 
*DefaultApi* | [**categories_delete**](docs/DefaultApi.md#categories_delete) | **DELETE** /categories/ | 
*DefaultApi* | [**categories_post**](docs/DefaultApi.md#categories_post) | **POST** /categories/ | 
*DefaultApi* | [**categories_put**](docs/DefaultApi.md#categories_put) | **PUT** /categories/ | 
*DefaultApi* | [**item_add_post**](docs/DefaultApi.md#item_add_post) | **POST** /item/add/ | 
*DefaultApi* | [**item_addbulk_post**](docs/DefaultApi.md#item_addbulk_post) | **POST** /item/addbulk/ | 
*DefaultApi* | [**item_delete**](docs/DefaultApi.md#item_delete) | **DELETE** /item/ | 
*DefaultApi* | [**item_put**](docs/DefaultApi.md#item_put) | **PUT** /item/ | 
*DefaultApi* | [**items_count_post**](docs/DefaultApi.md#items_count_post) | **POST** /items/count/ | 
*DefaultApi* | [**items_post**](docs/DefaultApi.md#items_post) | **POST** /items/ | 
*DefaultApi* | [**itemsallfields_post**](docs/DefaultApi.md#itemsallfields_post) | **POST** /items/?allfields | 
*DefaultApi* | [**orders_post**](docs/DefaultApi.md#orders_post) | **POST** /orders/ | 
*DefaultApi* | [**query_post**](docs/DefaultApi.md#query_post) | **POST** /query/ | 
*DefaultApi* | [**queryallfields_post**](docs/DefaultApi.md#queryallfields_post) | **POST** /query/?allfields | 
*DefaultApi* | [**services_delete**](docs/DefaultApi.md#services_delete) | **DELETE** /services/ | 
*DefaultApi* | [**services_get**](docs/DefaultApi.md#services_get) | **GET** /services/ | 
*DefaultApi* | [**services_post**](docs/DefaultApi.md#services_post) | **POST** /services/ | 
*DefaultApi* | [**services_put**](docs/DefaultApi.md#services_put) | **PUT** /services/ | 
*DefaultApi* | [**write_delete**](docs/DefaultApi.md#write_delete) | **DELETE** /write/ | 
*DefaultApi* | [**write_post**](docs/DefaultApi.md#write_post) | **POST** /write/ | 


## Documentation For Models

 - [Category](docs/Category.md)
 - [Dictionary](docs/Dictionary.md)
 - [Error](docs/Error.md)
 - [EventRequest](docs/EventRequest.md)
 - [InventoryGroup](docs/InventoryGroup.md)
 - [Item](docs/Item.md)
 - [Order](docs/Order.md)
 - [Response](docs/Response.md)
 - [Service](docs/Service.md)


## Documentation For Authorization


## APIKey

- **Type**: API key
- **API key parameter name**: APIKey
- **Location**: HTTP header

## AccountID

- **Type**: API key
- **API key parameter name**: accountid
- **Location**: HTTP header


## Author



