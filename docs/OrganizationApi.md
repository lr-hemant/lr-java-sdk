# OrganizationApi

All URIs are relative to *https://api.loginradius.com/v2/manage*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createOrganization**](OrganizationApi.md#createOrganization) | **POST** /organizations | Create Organization |
| [**createRole**](OrganizationApi.md#createRole) | **POST** /organizations/{orgId}/roles |  |
| [**deleteOrganization**](OrganizationApi.md#deleteOrganization) | **DELETE** /organizations/{orgId} | Delete Organization |
| [**getAllOrganizations**](OrganizationApi.md#getAllOrganizations) | **GET** /organizations | Get All Organizations |
| [**getOrgContextByOrgId**](OrganizationApi.md#getOrgContextByOrgId) | **GET** /organizations/{orgId}/orgcontext | Get Organization Context by OrgID |
| [**getOrgRolesByOrgId**](OrganizationApi.md#getOrgRolesByOrgId) | **GET** /organizations/{orgId}/roles |  |
| [**getOrganization**](OrganizationApi.md#getOrganization) | **GET** /organizations/{orgId} | Get Organization |
| [**updateOrganization**](OrganizationApi.md#updateOrganization) | **PUT** /organizations/{orgId} | Update Organization |
| [**updateOrganizationPolicy**](OrganizationApi.md#updateOrganizationPolicy) | **PUT** /organizations/{orgId}/policy | Update Organization Policy |
| [**updateOrganizationStatus**](OrganizationApi.md#updateOrganizationStatus) | **PUT** /organizations/{orgId}/status | Update Organization Status |


<a id="createOrganization"></a>
# **createOrganization**
> OrganizationsResponse createOrganization(createOrganizationRequest)

Create Organization

Create a new organization in the tenant

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    CreateOrganizationRequest createOrganizationRequest = new CreateOrganizationRequest(); // CreateOrganizationRequest | 
    try {
      OrganizationsResponse result = apiInstance.createOrganization(createOrganizationRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#createOrganization");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createOrganizationRequest** | [**CreateOrganizationRequest**](CreateOrganizationRequest.md)|  | |

### Return type

[**OrganizationsResponse**](OrganizationsResponse.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="createRole"></a>
# **createRole**
> Role createRole(orgId, rolePostRequest)



Create a new role within an organization

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    RolePostRequest rolePostRequest = new RolePostRequest(); // RolePostRequest | 
    try {
      Role result = apiInstance.createRole(orgId, rolePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#createRole");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |
| **rolePostRequest** | [**RolePostRequest**](RolePostRequest.md)|  | |

### Return type

[**Role**](Role.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Forbidden: The server understood the request, but is refusing to fulfill it. |  -  |
| **404** | Not Found: The requested resource could not be found. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="deleteOrganization"></a>
# **deleteOrganization**
> DeleteResponse deleteOrganization(orgId)

Delete Organization

Delete an organization by its ID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      DeleteResponse result = apiInstance.deleteOrganization(orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#deleteOrganization");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |

### Return type

[**DeleteResponse**](DeleteResponse.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getAllOrganizations"></a>
# **getAllOrganizations**
> GetAllOrganizations200Response getAllOrganizations()

Get All Organizations

Get a list of all organizations in the tenant

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    try {
      GetAllOrganizations200Response result = apiInstance.getAllOrganizations();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#getAllOrganizations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetAllOrganizations200Response**](GetAllOrganizations200Response.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getOrgContextByOrgId"></a>
# **getOrgContextByOrgId**
> GetOrgContextByUid200Response getOrgContextByOrgId(orgId)

Get Organization Context by OrgID

This API is used to get the user roles of all organization by OrgID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_fasf432d"; // String | Unique identifier of the organization.
    try {
      GetOrgContextByUid200Response result = apiInstance.getOrgContextByOrgId(orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#getOrgContextByOrgId");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Unique identifier of the organization. | |

### Return type

[**GetOrgContextByUid200Response**](GetOrgContextByUid200Response.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Not Found: The requested resource could not be found. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getOrgRolesByOrgId"></a>
# **getOrgRolesByOrgId**
> RoleByName200Response getOrgRolesByOrgId(orgId)



Get all roles defined within an organization

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      RoleByName200Response result = apiInstance.getOrgRolesByOrgId(orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#getOrgRolesByOrgId");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |

### Return type

[**RoleByName200Response**](RoleByName200Response.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Not Found: The requested resource could not be found. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getOrganization"></a>
# **getOrganization**
> OrganizationsResponse getOrganization(orgId)

Get Organization

Get details of a specific organization by its ID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      OrganizationsResponse result = apiInstance.getOrganization(orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#getOrganization");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |

### Return type

[**OrganizationsResponse**](OrganizationsResponse.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="updateOrganization"></a>
# **updateOrganization**
> OrganizationsResponse updateOrganization(orgId, organizationBase)

Update Organization

Update an organization&#39;s details by its ID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    OrganizationBase organizationBase = new OrganizationBase(); // OrganizationBase | 
    try {
      OrganizationsResponse result = apiInstance.updateOrganization(orgId, organizationBase);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#updateOrganization");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |
| **organizationBase** | [**OrganizationBase**](OrganizationBase.md)|  | |

### Return type

[**OrganizationsResponse**](OrganizationsResponse.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="updateOrganizationPolicy"></a>
# **updateOrganizationPolicy**
> OrganizationsPolicyBase updateOrganizationPolicy(orgId, organizationsPolicyBase)

Update Organization Policy

Update Organization Policy

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    OrganizationsPolicyBase organizationsPolicyBase = new OrganizationsPolicyBase(); // OrganizationsPolicyBase | 
    try {
      OrganizationsPolicyBase result = apiInstance.updateOrganizationPolicy(orgId, organizationsPolicyBase);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#updateOrganizationPolicy");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |
| **organizationsPolicyBase** | [**OrganizationsPolicyBase**](OrganizationsPolicyBase.md)|  | |

### Return type

[**OrganizationsPolicyBase**](OrganizationsPolicyBase.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="updateOrganizationStatus"></a>
# **updateOrganizationStatus**
> OrganizationsStatusResponse updateOrganizationStatus(orgId, organizationsStatusRequest)

Update Organization Status

Update Organization Status

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.loginradius.com/v2/manage");
    
    // Configure API key authorization: ClientIdAuth
    ApiKeyAuth ClientIdAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientIdAuth");
    ClientIdAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientIdAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ClientSecretAuth
    ApiKeyAuth ClientSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ClientSecretAuth");
    ClientSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ClientSecretAuth.setApiKeyPrefix("Token");

    // Configure HTTP bearer authorization: M2MBearerAuth
    HttpBearerAuth M2MBearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("M2MBearerAuth");
    M2MBearerAuth.setBearerToken("BEARER TOKEN");

    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure API key authorization: ApiSecretAuth
    ApiKeyAuth ApiSecretAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiSecretAuth");
    ApiSecretAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiSecretAuth.setApiKeyPrefix("Token");

    OrganizationApi apiInstance = new OrganizationApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    OrganizationsStatusRequest organizationsStatusRequest = new OrganizationsStatusRequest(); // OrganizationsStatusRequest | 
    try {
      OrganizationsStatusResponse result = apiInstance.updateOrganizationStatus(orgId, organizationsStatusRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationApi#updateOrganizationStatus");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **orgId** | **String**| Organization ID | |
| **organizationsStatusRequest** | [**OrganizationsStatusRequest**](OrganizationsStatusRequest.md)|  | |

### Return type

[**OrganizationsStatusResponse**](OrganizationsStatusResponse.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **400** | Status Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **409** | Status Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

