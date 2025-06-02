# OrganizationConnectionGroupRolesApi

All URIs are relative to *https://api.loginradius.com/v2/manage*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createConnectionGroupRole**](OrganizationConnectionGroupRolesApi.md#createConnectionGroupRole) | **POST** /organizations/{orgId}/connections/{connId}/grouproles | Create Organization Connection Group Roles |
| [**deleteConnectionGroupRole**](OrganizationConnectionGroupRolesApi.md#deleteConnectionGroupRole) | **DELETE** /organizations/{orgId}/connections/{connId}/grouproles/{groupRoleId} | Delete Organization Connection Group Roles |
| [**getAllConnectionGroupRoles**](OrganizationConnectionGroupRolesApi.md#getAllConnectionGroupRoles) | **GET** /organizations/{orgId}/connections/{connId}/grouproles | Get All Organization Connection Group Roles |
| [**updateConnectionGroupRole**](OrganizationConnectionGroupRolesApi.md#updateConnectionGroupRole) | **PUT** /organizations/{orgId}/connections/{connId}/grouproles/{groupRoleId} | Update Organization Connection Group Roles |


<a id="createConnectionGroupRole"></a>
# **createConnectionGroupRole**
> ConnectionGroupRoleResponse createConnectionGroupRole(connId, orgId, createConnectionGroupRoleRequest)

Create Organization Connection Group Roles

Create a new group-to-role mapping for an identity provider connection

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationConnectionGroupRolesApi;

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

    OrganizationConnectionGroupRolesApi apiInstance = new OrganizationConnectionGroupRolesApi(defaultClient);
    String connId = "conn_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Connection ID
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    CreateConnectionGroupRoleRequest createConnectionGroupRoleRequest = new CreateConnectionGroupRoleRequest(); // CreateConnectionGroupRoleRequest | 
    try {
      ConnectionGroupRoleResponse result = apiInstance.createConnectionGroupRole(connId, orgId, createConnectionGroupRoleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationConnectionGroupRolesApi#createConnectionGroupRole");
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
| **connId** | **String**| Organization Connection ID | |
| **orgId** | **String**| Organization ID | |
| **createConnectionGroupRoleRequest** | [**CreateConnectionGroupRoleRequest**](CreateConnectionGroupRoleRequest.md)|  | |

### Return type

[**ConnectionGroupRoleResponse**](ConnectionGroupRoleResponse.md)

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
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="deleteConnectionGroupRole"></a>
# **deleteConnectionGroupRole**
> DeleteResponse deleteConnectionGroupRole(orgId, connId, groupRoleId)

Delete Organization Connection Group Roles

Delete a specific group-to-role mapping

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationConnectionGroupRolesApi;

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

    OrganizationConnectionGroupRolesApi apiInstance = new OrganizationConnectionGroupRolesApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    String connId = "conn_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Connection ID
    String groupRoleId = "group_role_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Connection Group Role ID
    try {
      DeleteResponse result = apiInstance.deleteConnectionGroupRole(orgId, connId, groupRoleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationConnectionGroupRolesApi#deleteConnectionGroupRole");
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
| **connId** | **String**| Organization Connection ID | |
| **groupRoleId** | **String**| Organization Connection Group Role ID | |

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
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getAllConnectionGroupRoles"></a>
# **getAllConnectionGroupRoles**
> GetAllConnectionGroupRoles200Response getAllConnectionGroupRoles(orgId, connId)

Get All Organization Connection Group Roles

Get all group-to-role mappings for an identity provider connection

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationConnectionGroupRolesApi;

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

    OrganizationConnectionGroupRolesApi apiInstance = new OrganizationConnectionGroupRolesApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    String connId = "conn_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Connection ID
    try {
      GetAllConnectionGroupRoles200Response result = apiInstance.getAllConnectionGroupRoles(orgId, connId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationConnectionGroupRolesApi#getAllConnectionGroupRoles");
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
| **connId** | **String**| Organization Connection ID | |

### Return type

[**GetAllConnectionGroupRoles200Response**](GetAllConnectionGroupRoles200Response.md)

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

<a id="updateConnectionGroupRole"></a>
# **updateConnectionGroupRole**
> ConnectionGroupRoleResponse updateConnectionGroupRole(connId, groupRoleId, orgId, connectionGroupRoleRequest)

Update Organization Connection Group Roles

Update a specific group-to-role mapping

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationConnectionGroupRolesApi;

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

    OrganizationConnectionGroupRolesApi apiInstance = new OrganizationConnectionGroupRolesApi(defaultClient);
    String connId = "conn_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Connection ID
    String groupRoleId = "group_role_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Connection Group Role ID
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    ConnectionGroupRoleRequest connectionGroupRoleRequest = new ConnectionGroupRoleRequest(); // ConnectionGroupRoleRequest | 
    try {
      ConnectionGroupRoleResponse result = apiInstance.updateConnectionGroupRole(connId, groupRoleId, orgId, connectionGroupRoleRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationConnectionGroupRolesApi#updateConnectionGroupRole");
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
| **connId** | **String**| Organization Connection ID | |
| **groupRoleId** | **String**| Organization Connection Group Role ID | |
| **orgId** | **String**| Organization ID | |
| **connectionGroupRoleRequest** | [**ConnectionGroupRoleRequest**](ConnectionGroupRoleRequest.md)|  | |

### Return type

[**ConnectionGroupRoleResponse**](ConnectionGroupRoleResponse.md)

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
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Status Internal Server Error: The server encountered an unexpected error. |  -  |

