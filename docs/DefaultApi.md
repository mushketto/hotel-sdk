# DefaultApi

All URIs are relative to *http://localhost:3000/api/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**hotelsGet**](#hotelsget) | **GET** /hotels | Отримати список усіх готелів|
|[**hotelsHotelIdRoomsGet**](#hotelshotelidroomsget) | **GET** /hotels/{hotelId}/rooms | Отримати список номерів конкретного готелю|
|[**hotelsPost**](#hotelspost) | **POST** /hotels | Додати новий готель|

# **hotelsGet**
> Array<Hotel> hotelsGet()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

const { status, data } = await apiInstance.hotelsGet();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<Hotel>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Успішна відповідь |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **hotelsHotelIdRoomsGet**
> hotelsHotelIdRoomsGet()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let hotelId: number; // (default to undefined)

const { status, data } = await apiInstance.hotelsHotelIdRoomsGet(
    hotelId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hotelId** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Список номерів |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **hotelsPost**
> hotelsPost(hotel)


### Example

```typescript
import {
    DefaultApi,
    Configuration,
    Hotel
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let hotel: Hotel; //

const { status, data } = await apiInstance.hotelsPost(
    hotel
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hotel** | **Hotel**|  | |


### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Готель створено |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

