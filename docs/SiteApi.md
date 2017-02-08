# SiteApi

All URIs are relative to *https://www.waitlisted.co/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSite**](SiteApi.md#getSite) | **GET** /site | 


<a name="getSite"></a>
# **getSite**
> SiteResponse getSite()



Get site settings and reservation count.

### Example
```java
// Import classes:
//import co.waitlisted.ApiException;
//import co.waitlisted.api.SiteApi;


SiteApi apiInstance = new SiteApi();
try {
    SiteResponse result = apiInstance.getSite();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SiteApi#getSite");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SiteResponse**](SiteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

