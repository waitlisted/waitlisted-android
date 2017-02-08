# ReservationApi

All URIs are relative to *https://www.waitlisted.co/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createReservation**](ReservationApi.md#createReservation) | **POST** /reservations | 
[**deleteReservation**](ReservationApi.md#deleteReservation) | **DELETE** /reservations | 
[**getReservation**](ReservationApi.md#getReservation) | **GET** /reservations | 


<a name="createReservation"></a>
# **createReservation**
> ReservationsResponse createReservation(body)



Creates a new reservation.

### Example
```java
// Import classes:
//import co.waitlisted.ApiException;
//import co.waitlisted.api.ReservationApi;


ReservationApi apiInstance = new ReservationApi();
Reservation body = new Reservation(); // Reservation | Reservation Data
try {
    ReservationsResponse result = apiInstance.createReservation(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ReservationApi#createReservation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Reservation**](Reservation.md)| Reservation Data |

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteReservation"></a>
# **deleteReservation**
> deleteReservation(body)



Delete a reservation.

### Example
```java
// Import classes:
//import co.waitlisted.ApiClient;
//import co.waitlisted.ApiException;
//import co.waitlisted.Configuration;
//import co.waitlisted.auth.*;
//import co.waitlisted.api.ReservationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: api_key
ApiKeyAuth api_key = (ApiKeyAuth) defaultClient.getAuthentication("api_key");
api_key.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.setApiKeyPrefix("Token");

ReservationApi apiInstance = new ReservationApi();
ReservationRequest body = new ReservationRequest(); // ReservationRequest | Reservation Data
try {
    apiInstance.deleteReservation(body);
} catch (ApiException e) {
    System.err.println("Exception when calling ReservationApi#deleteReservation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ReservationRequest**](ReservationRequest.md)| Reservation Data |

### Return type

null (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getReservation"></a>
# **getReservation**
> ReservationsResponse getReservation(email)



Get a reservation.

### Example
```java
// Import classes:
//import co.waitlisted.ApiException;
//import co.waitlisted.api.ReservationApi;


ReservationApi apiInstance = new ReservationApi();
String email = "email_example"; // String | Email address
try {
    ReservationsResponse result = apiInstance.getReservation(email);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ReservationApi#getReservation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **String**| Email address |

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

