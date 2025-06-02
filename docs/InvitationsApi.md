# InvitationsApi

All URIs are relative to *https://api.loginradius.com/v2/manage*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteInvitationByInvitationId**](InvitationsApi.md#deleteInvitationByInvitationId) | **DELETE** /invitations/{invitationid} | Delete/Revoke invitation by invitation id |
| [**getInvitationByInvitationId**](InvitationsApi.md#getInvitationByInvitationId) | **GET** /invitations/{invitationid} | Get invitation by invitation id |
| [**getInvitationsByOrgId**](InvitationsApi.md#getInvitationsByOrgId) | **GET** /invitations | Get all invitations By Org id |
| [**resendInvitationByInvitationId**](InvitationsApi.md#resendInvitationByInvitationId) | **POST** /invitations/{invitationid}/resend | Resend invitation by ID |
| [**sendInvitation**](InvitationsApi.md#sendInvitation) | **POST** /invitations | Send new invitation |
| [**updateInvitationByInvitationId**](InvitationsApi.md#updateInvitationByInvitationId) | **PUT** /invitations/{invitationid} | Update invitation by invitation id |


<a id="deleteInvitationByInvitationId"></a>
# **deleteInvitationByInvitationId**
> Invitation deleteInvitationByInvitationId(invitationid)

Delete/Revoke invitation by invitation id

Delete or revoke an invitation by invitation id

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InvitationsApi;

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

    InvitationsApi apiInstance = new InvitationsApi(defaultClient);
    String invitationid = "inv_123456789"; // String | The ID of the invitation. The ID is typically in the format *inv_<unique_id>*, where *<unique_id>* is a string of alphanumeric characters.
    try {
      Invitation result = apiInstance.deleteInvitationByInvitationId(invitationid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvitationsApi#deleteInvitationByInvitationId");
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
| **invitationid** | **String**| The ID of the invitation. The ID is typically in the format *inv_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. | |

### Return type

[**Invitation**](Invitation.md)

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
| **404** | Not Found: The server cannot find the requested resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getInvitationByInvitationId"></a>
# **getInvitationByInvitationId**
> Invitation getInvitationByInvitationId(invitationid)

Get invitation by invitation id

Get invitation details by invitation ID

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InvitationsApi;

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

    InvitationsApi apiInstance = new InvitationsApi(defaultClient);
    String invitationid = "inv_123456789"; // String | The ID of the invitation. The ID is typically in the format *inv_<unique_id>*, where *<unique_id>* is a string of alphanumeric characters.
    try {
      Invitation result = apiInstance.getInvitationByInvitationId(invitationid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvitationsApi#getInvitationByInvitationId");
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
| **invitationid** | **String**| The ID of the invitation. The ID is typically in the format *inv_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. | |

### Return type

[**Invitation**](Invitation.md)

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
| **404** | Not Found: The server cannot find the requested resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="getInvitationsByOrgId"></a>
# **getInvitationsByOrgId**
> GetInvitationsByOrgId200Response getInvitationsByOrgId(orgid)

Get all invitations By Org id

Get all invitations By Org id

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InvitationsApi;

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

    InvitationsApi apiInstance = new InvitationsApi(defaultClient);
    String orgid = "org_123456789"; // String | 
    try {
      GetInvitationsByOrgId200Response result = apiInstance.getInvitationsByOrgId(orgid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvitationsApi#getInvitationsByOrgId");
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
| **orgid** | **String**|  | |

### Return type

[**GetInvitationsByOrgId200Response**](GetInvitationsByOrgId200Response.md)

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
| **404** | Not Found: The server cannot find the requested resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="resendInvitationByInvitationId"></a>
# **resendInvitationByInvitationId**
> ResendInvitation resendInvitationByInvitationId(invitationid)

Resend invitation by ID

Resend invitation details by invitation id

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InvitationsApi;

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

    InvitationsApi apiInstance = new InvitationsApi(defaultClient);
    String invitationid = "inv_123456789"; // String | The ID of the invitation. The ID is typically in the format *inv_<unique_id>*, where *<unique_id>* is a string of alphanumeric characters.
    try {
      ResendInvitation result = apiInstance.resendInvitationByInvitationId(invitationid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvitationsApi#resendInvitationByInvitationId");
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
| **invitationid** | **String**| The ID of the invitation. The ID is typically in the format *inv_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. | |

### Return type

[**ResendInvitation**](ResendInvitation.md)

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
| **404** | Not Found: The server cannot find the requested resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="sendInvitation"></a>
# **sendInvitation**
> Invitation sendInvitation(sendInvitation, invitationUrl)

Send new invitation

Send a new invitation

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InvitationsApi;

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

    InvitationsApi apiInstance = new InvitationsApi(defaultClient);
    SendInvitation sendInvitation = new SendInvitation(); // SendInvitation | 
    String invitationUrl = "https://example.com/accept-invite"; // String | The URL to which the user will be redirected after accepting the invitation. This URL should be a valid URL and can include query parameters if needed.
    try {
      Invitation result = apiInstance.sendInvitation(sendInvitation, invitationUrl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvitationsApi#sendInvitation");
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
| **sendInvitation** | [**SendInvitation**](SendInvitation.md)|  | |
| **invitationUrl** | **String**| The URL to which the user will be redirected after accepting the invitation. This URL should be a valid URL and can include query parameters if needed. | [optional] |

### Return type

[**Invitation**](Invitation.md)

### Authorization

[ClientIdAuth](../README.md#ClientIdAuth), [ClientSecretAuth](../README.md#ClientSecretAuth), [M2MBearerAuth](../README.md#M2MBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ApiSecretAuth](../README.md#ApiSecretAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Invitation sent successfully |  -  |
| **400** | Bad Request: The request could not be understood by the server due to malformed syntax. |  -  |
| **403** | Forbidden: The client does not have permission to access the resource. |  -  |
| **404** | Not Found: The server cannot find the requested resource. |  -  |
| **409** | Conflict: The request could not be completed due to a conflict with the current state of the resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

<a id="updateInvitationByInvitationId"></a>
# **updateInvitationByInvitationId**
> Invitation updateInvitationByInvitationId(invitationid, updateInvitationByInvitationIdRequest, invitationUrl)

Update invitation by invitation id

Update invitation details by invitation id

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.InvitationsApi;

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

    InvitationsApi apiInstance = new InvitationsApi(defaultClient);
    String invitationid = "inv_123456789"; // String | The ID of the invitation. The ID is typically in the format *inv_<unique_id>*, where *<unique_id>* is a string of alphanumeric characters.
    UpdateInvitationByInvitationIdRequest updateInvitationByInvitationIdRequest = new UpdateInvitationByInvitationIdRequest(); // UpdateInvitationByInvitationIdRequest | 
    String invitationUrl = "https://example.com/accept-invite"; // String | The URL to which the user will be redirected after accepting the invitation. This URL should be a valid URL and can include query parameters if needed.
    try {
      Invitation result = apiInstance.updateInvitationByInvitationId(invitationid, updateInvitationByInvitationIdRequest, invitationUrl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvitationsApi#updateInvitationByInvitationId");
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
| **invitationid** | **String**| The ID of the invitation. The ID is typically in the format *inv_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. | |
| **updateInvitationByInvitationIdRequest** | [**UpdateInvitationByInvitationIdRequest**](UpdateInvitationByInvitationIdRequest.md)|  | |
| **invitationUrl** | **String**| The URL to which the user will be redirected after accepting the invitation. This URL should be a valid URL and can include query parameters if needed. | [optional] |

### Return type

[**Invitation**](Invitation.md)

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
| **404** | Not Found: The server cannot find the requested resource. |  -  |
| **500** | Internal Server Error: The server encountered an unexpected error. |  -  |

