

# ConnectionResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Name of the connection |  [optional] |
|**domain** | **String** | Domain associated with the connection |  [optional] |
|**attributes** | [**OrganizationsConnectionBaseAttributes**](OrganizationsConnectionBaseAttributes.md) |  |  [optional] |
|**id** | **String** | Unique identifier for the connection |  [optional] |
|**isActive** | **Boolean** | Indicates whether the connection is active |  [optional] |
|**createdDate** | **OffsetDateTime** | Date when the connection was created |  [optional] |
|**groupRoles** | [**List&lt;ConnectionGroupRoleResponse&gt;**](ConnectionGroupRoleResponse.md) |  |  [optional] |
|**modifiedDate** | **OffsetDateTime** | Date when the connection was last modified |  [optional] |
|**idPEntityId** | **String** | Unique identifier for the Identity Provider (IdP). |  [optional] |
|**idPMetadataUrl** | **String** | URL to the IdP metadata XML file. |  [optional] |
|**isIDPInitiated** | **Boolean** | Indicates whether the SAML connection is initiated by the IdP. |  [optional] |
|**idPCertificate** | [**OrganizationsConnectionSamlBaseIDPCertificate**](OrganizationsConnectionSamlBaseIDPCertificate.md) |  |  [optional] |
|**connectionType** | [**ConnectionTypeEnum**](#ConnectionTypeEnum) | Type of the connection, which is OIDC in this case. |  [optional] |
|**entityId** | **String** | The unique identifier for the SAML service provider. |  [optional] |
|**metadataUrl** | **String** | The URL to the SAML metadata XML file. |  [optional] |
|**acSEndpoint** | **String** | The Assertion Consumer Service (ACS) endpoint URL for SAML responses. |  [optional] |
|**spCertificate** | [**SamlConnectionResponseAllOfSPCertificate**](SamlConnectionResponseAllOfSPCertificate.md) |  |  [optional] |
|**authorizationUrl** | **String** |  |  [optional] |
|**clientId** | **String** |  |  [optional] |
|**clientSecret** | **String** |  |  [optional] |
|**issuer** | **String** |  |  [optional] |
|**scopes** | **List&lt;String&gt;** |  |  [optional] |
|**tokenAuthMethod** | **String** |  |  [optional] |
|**tokenUrl** | **String** |  |  [optional] |
|**userInfoUrl** | **String** |  |  [optional] |
|**redirectURI** | **String** | The redirect URI for the OIDC connection, where the authorization server will send the user after authentication. |  [optional] |



## Enum: ConnectionTypeEnum

| Name | Value |
|---- | -----|
| OIDC_CUSTOM | &quot;oidc_custom&quot; |



