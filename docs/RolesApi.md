# RolesApi

All URIs are relative to *https://api.loginradius.com/v2/manage*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createRole**](RolesApi.md#createRole) | **POST** /roles |  |
| [**deleteRole**](RolesApi.md#deleteRole) | **DELETE** /roles/{id} |  |
| [**getAllRoles**](RolesApi.md#getAllRoles) | **GET** /roles |  |
| [**getRoleById**](RolesApi.md#getRoleById) | **GET** /roles/{id} |  |
| [**roleByName**](RolesApi.md#roleByName) | **GET** /roles/{name}/name | Get Role by Name |
| [**setDefaultRole**](RolesApi.md#setDefaultRole) | **PUT** /roles/{id}/default |  |
| [**updateRole**](RolesApi.md#updateRole) | **PUT** /roles/{id} |  |


<a id="createRole"></a>
# **createRole**
> TenantRole createRole(rolePostRequest)



Create a new role in the tenant

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    RolePostRequest rolePostRequest = new RolePostRequest(); // RolePostRequest | 
    try {
      TenantRole result = apiInstance.createRole(rolePostRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#createRole");
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
| **rolePostRequest** | [**RolePostRequest**](RolePostRequest.md)|  | |

### Return type

[**TenantRole**](TenantRole.md)

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
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="deleteRole"></a>
# **deleteRole**
> DeleteResponse deleteRole(id)



Delete Role

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    String id = "role_2enk23n3"; // String | Role ID
    try {
      DeleteResponse result = apiInstance.deleteRole(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#deleteRole");
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
| **id** | **String**| Role ID | |

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
| **404** | Not Found: The requested resource could not be found. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getAllRoles"></a>
# **getAllRoles**
> GetAllRoles200Response getAllRoles()



Get all roles in the tenant

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    try {
      GetAllRoles200Response result = apiInstance.getAllRoles();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#getAllRoles");
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

[**GetAllRoles200Response**](GetAllRoles200Response.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK: The request was successful. |  -  |
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getRoleById"></a>
# **getRoleById**
> Role getRoleById(id)



Get details of a specific role by its ID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    String id = "role_2enk23n3"; // String | Role ID
    try {
      Role result = apiInstance.getRoleById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#getRoleById");
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
| **id** | **String**| Role ID | |

### Return type

[**Role**](Role.md)

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

<a id="roleByName"></a>
# **roleByName**
> RoleByName200Response roleByName(name, orgid)

Get Role by Name

This API is used to get the role by the role name.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    String name = "Admin"; // String | Role Name
    String orgid = "org_2enk23n3"; // String | Organization ID
    try {
      RoleByName200Response result = apiInstance.roleByName(name, orgid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#roleByName");
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
| **name** | **String**| Role Name | |
| **orgid** | **String**| Organization ID | [optional] |

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
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="setDefaultRole"></a>
# **setDefaultRole**
> DefaultResponse setDefaultRole(id)



Set Default Role

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    String id = "role_2enk23n3"; // String | Role ID
    try {
      DefaultResponse result = apiInstance.setDefaultRole(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#setDefaultRole");
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
| **id** | **String**| Role ID | |

### Return type

[**DefaultResponse**](DefaultResponse.md)

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

<a id="updateRole"></a>
# **updateRole**
> Role updateRole(id, rolesPutRequest)



Update a role&#39;s details by its ID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.RolesApi;

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

    RolesApi apiInstance = new RolesApi(defaultClient);
    String id = "role_2enk23n3"; // String | Role ID
    RolesPutRequest rolesPutRequest = new RolesPutRequest(); // RolesPutRequest | 
    try {
      Role result = apiInstance.updateRole(id, rolesPutRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RolesApi#updateRole");
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
| **id** | **String**| Role ID | |
| **rolesPutRequest** | [**RolesPutRequest**](RolesPutRequest.md)|  | |

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
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Not Found: The requested resource could not be found. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

