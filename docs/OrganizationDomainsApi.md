# OrganizationDomainsApi

All URIs are relative to *https://api.loginradius.com/v2/manage*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addOrganizationDomain**](OrganizationDomainsApi.md#addOrganizationDomain) | **POST** /organizations/{orgId}/domains | Add Organization Domain |
| [**deleteOrganizationDomain**](OrganizationDomainsApi.md#deleteOrganizationDomain) | **DELETE** /organizations/{orgId}/domains/{domainId} | Delete Organization Domain |
| [**getAllOrganizationDomains**](OrganizationDomainsApi.md#getAllOrganizationDomains) | **GET** /organizations/{orgId}/domains | List of Organization Domains |
| [**getOrganizationDomain**](OrganizationDomainsApi.md#getOrganizationDomain) | **GET** /organizations/{orgId}/domains/{domainId} | Get Organization Domain |
| [**verifyOrganizationDomain**](OrganizationDomainsApi.md#verifyOrganizationDomain) | **POST** /organizations/{orgId}/domains/{domainId} | Verify Organization Domain |


<a id="addOrganizationDomain"></a>
# **addOrganizationDomain**
> OrganizationsDomainsResponse addOrganizationDomain(orgId, addOrganizationDomainRequest)

Add Organization Domain

Add Organization Domain

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationDomainsApi;

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

    OrganizationDomainsApi apiInstance = new OrganizationDomainsApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    AddOrganizationDomainRequest addOrganizationDomainRequest = new AddOrganizationDomainRequest(); // AddOrganizationDomainRequest | 
    try {
      OrganizationsDomainsResponse result = apiInstance.addOrganizationDomain(orgId, addOrganizationDomainRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationDomainsApi#addOrganizationDomain");
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
| **addOrganizationDomainRequest** | [**AddOrganizationDomainRequest**](AddOrganizationDomainRequest.md)|  | |

### Return type

[**OrganizationsDomainsResponse**](OrganizationsDomainsResponse.md)

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

<a id="deleteOrganizationDomain"></a>
# **deleteOrganizationDomain**
> DeleteResponse deleteOrganizationDomain(orgId, domainId)

Delete Organization Domain

Delete Organization Domain

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationDomainsApi;

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

    OrganizationDomainsApi apiInstance = new OrganizationDomainsApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    String domainId = "org_domain_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Domain ID
    try {
      DeleteResponse result = apiInstance.deleteOrganizationDomain(orgId, domainId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationDomainsApi#deleteOrganizationDomain");
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
| **domainId** | **String**| Organization Domain ID | |

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

<a id="getAllOrganizationDomains"></a>
# **getAllOrganizationDomains**
> GetAllOrganizationDomains200Response getAllOrganizationDomains(orgId)

List of Organization Domains

Get all domains associated with an organization

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationDomainsApi;

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

    OrganizationDomainsApi apiInstance = new OrganizationDomainsApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      GetAllOrganizationDomains200Response result = apiInstance.getAllOrganizationDomains(orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationDomainsApi#getAllOrganizationDomains");
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

[**GetAllOrganizationDomains200Response**](GetAllOrganizationDomains200Response.md)

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

<a id="getOrganizationDomain"></a>
# **getOrganizationDomain**
> OrganizationsDomainsResponse getOrganizationDomain(orgId, domainId)

Get Organization Domain

Get Organization Domain

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationDomainsApi;

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

    OrganizationDomainsApi apiInstance = new OrganizationDomainsApi(defaultClient);
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    String domainId = "org_domain_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Domain ID
    try {
      OrganizationsDomainsResponse result = apiInstance.getOrganizationDomain(orgId, domainId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationDomainsApi#getOrganizationDomain");
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
| **domainId** | **String**| Organization Domain ID | |

### Return type

[**OrganizationsDomainsResponse**](OrganizationsDomainsResponse.md)

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

<a id="verifyOrganizationDomain"></a>
# **verifyOrganizationDomain**
> OrganizationsDomainsResponse verifyOrganizationDomain(domainId, orgId)

Verify Organization Domain

Verify Organization Domain

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.OrganizationDomainsApi;

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

    OrganizationDomainsApi apiInstance = new OrganizationDomainsApi(defaultClient);
    String domainId = "org_domain_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization Domain ID
    String orgId = "org_1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef"; // String | Organization ID
    try {
      OrganizationsDomainsResponse result = apiInstance.verifyOrganizationDomain(domainId, orgId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling OrganizationDomainsApi#verifyOrganizationDomain");
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
| **domainId** | **String**| Organization Domain ID | |
| **orgId** | **String**| Organization ID | |

### Return type

[**OrganizationsDomainsResponse**](OrganizationsDomainsResponse.md)

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

