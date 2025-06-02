

# OidcConnectionResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**authorizationUrl** | **String** |  |  [optional] |
|**clientId** | **String** |  |  [optional] |
|**clientSecret** | **String** |  |  [optional] |
|**issuer** | **String** |  |  [optional] |
|**scopes** | **List&lt;String&gt;** |  |  [optional] |
|**tokenAuthMethod** | **String** |  |  [optional] |
|**tokenUrl** | **String** |  |  [optional] |
|**userInfoUrl** | **String** |  |  [optional] |
|**connectionType** | [**ConnectionTypeEnum**](#ConnectionTypeEnum) | Type of the connection, which is OIDC in this case. |  [optional] |
|**redirectURI** | **String** | The redirect URI for the OIDC connection, where the authorization server will send the user after authentication. |  [optional] |



## Enum: ConnectionTypeEnum

| Name | Value |
|---- | -----|
| OIDC_CUSTOM | &quot;oidc_custom&quot; |



