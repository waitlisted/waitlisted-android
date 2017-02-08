# android-api

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>waitlisted</groupId>
    <artifactId>android-api</artifactId>
    <version>2.0.0</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "waitlisted:android-api:2.0.0"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

* target/android-api-2.0.0.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import co.waitlisted.*;
import co.waitlisted.auth.*;
import co.waitlisted.model.*;
import co.waitlisted.api.ReservationApi;

import java.io.File;
import java.util.*;

public class ReservationApiExample {

    public static void main(String[] args) {
        
        ReservationApi apiInstance = new ReservationApi();
        Reservation body = new Reservation(); // Reservation | Reservation Data
        try {
            ReservationsResponse result = apiInstance.createReservation(body);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ReservationApi#createReservation");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://www.waitlisted.co/api/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ReservationApi* | [**createReservation**](docs/ReservationApi.md#createReservation) | **POST** /reservations | 
*ReservationApi* | [**deleteReservation**](docs/ReservationApi.md#deleteReservation) | **DELETE** /reservations | 
*ReservationApi* | [**getReservation**](docs/ReservationApi.md#getReservation) | **GET** /reservations | 
*SiteApi* | [**getSite**](docs/SiteApi.md#getSite) | **GET** /site | 


## Documentation for Models

 - [ErrorResponse](docs/ErrorResponse.md)
 - [FormResponse](docs/FormResponse.md)
 - [Reservation](docs/Reservation.md)
 - [ReservationRequest](docs/ReservationRequest.md)
 - [ReservationsResponse](docs/ReservationsResponse.md)
 - [SiteResponse](docs/SiteResponse.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### api_key

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issue.

## Author



