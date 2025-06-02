# UserRoleApi

All URIs are relative to *https://api.loginradius.com/v2/manage*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**assignRolesToUser**](UserRoleApi.md#assignRolesToUser) | **PUT** /account/{uid}/orgcontext/{orgId}/roles | Assign roles to the user in an org |
| [**assignRolesToUserInAllOrgs**](UserRoleApi.md#assignRolesToUserInAllOrgs) | **PUT** /account/{uid}/orgcontext/roles | Assign roles to the user in tenant |
| [**deleteOrgContextByUid**](UserRoleApi.md#deleteOrgContextByUid) | **DELETE** /account/{uid}/orgcontext | Delete Organization Context by UID |
| [**deleteOrgContextByUidAndOrgId**](UserRoleApi.md#deleteOrgContextByUidAndOrgId) | **DELETE** /account/{uid}/orgcontext/{orgId} | Delete Organization roles of OrgID of user UID |
| [**getOrgContextByUid**](UserRoleApi.md#getOrgContextByUid) | **GET** /account/{uid}/orgcontext | Get Organization Context by UID |
| [**getOrgContextByUidAndOrgId**](UserRoleApi.md#getOrgContextByUidAndOrgId) | **GET** /account/{uid}/orgcontext/{orgId} | Get Organization roles of OrgID of user UID |


<a id="assignRolesToUser"></a>
# **assignRolesToUser**
> GetOrgContextByUid200Response assignRolesToUser(uid, orgId, userRolePutRequest)

Assign roles to the user in an org

This API is used to assign roles to the user in the specific organization.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UserRoleApi;

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

    UserRoleApi apiInstance = new UserRoleApi(defaultClient);
    String uid = "123456789"; // String | UID of the user
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    UserRolePutRequest userRolePutRequest = new UserRolePutRequest(); // UserRolePutRequest | 
    try {
      GetOrgContextByUid200Response result = apiInstance.assignRolesToUser(uid, orgId, userRolePutRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRoleApi#assignRolesToUser");
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
| **uid** | **String**| UID of the user | |
| **orgId** | **String**| Organization ID | |
| **userRolePutRequest** | [**UserRolePutRequest**](UserRolePutRequest.md)|  | |

### Return type

[**GetOrgContextByUid200Response**](GetOrgContextByUid200Response.md)

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

<a id="assignRolesToUserInAllOrgs"></a>
# **assignRolesToUserInAllOrgs**
> GetOrgContextByUid200Response assignRolesToUserInAllOrgs(uid)

Assign roles to the user in tenant

This API is used to assign roles to the user in tenant.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UserRoleApi;

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

    UserRoleApi apiInstance = new UserRoleApi(defaultClient);
    String uid = "123456789"; // String | UID of the user
    try {
      GetOrgContextByUid200Response result = apiInstance.assignRolesToUserInAllOrgs(uid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRoleApi#assignRolesToUserInAllOrgs");
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
| **uid** | **String**| UID of the user | |

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
| **403** | Forbidden: The server understood the request, but is refusing to fulfill it. |  -  |
| **404** | Not Found: The requested resource could not be found. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="deleteOrgContextByUid"></a>
# **deleteOrgContextByUid**
> DeleteResponse deleteOrgContextByUid(uid)

Delete Organization Context by UID

This API is used to delete the user roles of all organization by UID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UserRoleApi;

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

    UserRoleApi apiInstance = new UserRoleApi(defaultClient);
    String uid = "123456789"; // String | UID of the user
    try {
      DeleteResponse result = apiInstance.deleteOrgContextByUid(uid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRoleApi#deleteOrgContextByUid");
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
| **uid** | **String**| UID of the user | |

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
| **400** | Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="deleteOrgContextByUidAndOrgId"></a>
# **deleteOrgContextByUidAndOrgId**
> DeleteResponse deleteOrgContextByUidAndOrgId(uid, orgId)

Delete Organization roles of OrgID of user UID

This API is used to delete the user roles of an organization by UID and OrgID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UserRoleApi;

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

    UserRoleApi apiInstance = new UserRoleApi(defaultClient);
    String uid = "123456789"; // String | UID of the user
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      DeleteResponse result = apiInstance.deleteOrgContextByUidAndOrgId(uid, orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRoleApi#deleteOrgContextByUidAndOrgId");
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
| **uid** | **String**| UID of the user | |
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
| **400** | Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Forbidden: The server understood the request, but is refusing to fulfill it. |  -  |
| **404** | Not Found: The requested resource could not be found. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getOrgContextByUid"></a>
# **getOrgContextByUid**
> GetOrgContextByUid200Response getOrgContextByUid(uid)

Get Organization Context by UID

This API is used to get the user roles of all organization by UID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UserRoleApi;

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

    UserRoleApi apiInstance = new UserRoleApi(defaultClient);
    String uid = "123456789"; // String | UID of the user
    try {
      GetOrgContextByUid200Response result = apiInstance.getOrgContextByUid(uid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRoleApi#getOrgContextByUid");
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
| **uid** | **String**| UID of the user | |

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
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getOrgContextByUidAndOrgId"></a>
# **getOrgContextByUidAndOrgId**
> GetOrgContextByUid200Response getOrgContextByUidAndOrgId(uid, orgId)

Get Organization roles of OrgID of user UID

This API is used to get the user roles of an organization by UID and OrgID.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UserRoleApi;

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

    UserRoleApi apiInstance = new UserRoleApi(defaultClient);
    String uid = "123456789"; // String | UID of the user
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      GetOrgContextByUid200Response result = apiInstance.getOrgContextByUidAndOrgId(uid, orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserRoleApi#getOrgContextByUidAndOrgId");
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
| **uid** | **String**| UID of the user | |
| **orgId** | **String**| Organization ID | |

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

