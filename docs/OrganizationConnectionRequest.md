

# OrganizationConnectionRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Name of the connection |  [optional] |
|**domain** | **String** | Domain associated with the connection |  [optional] |
|**attributes** | [**OrganizationsConnectionBaseAttributes**](OrganizationsConnectionBaseAttributes.md) |  |  [optional] |
|**connectionType** | [**ConnectionTypeEnum**](#ConnectionTypeEnum) |  |  [optional] |
|**idPEntityId** | **String** | Unique identifier for the Identity Provider (IdP). |  [optional] |
|**idPMetadataUrl** | **String** | URL to the IdP metadata XML file. |  [optional] |
|**isIDPInitiated** | **Boolean** | Indicates whether the SAML connection is initiated by the IdP. |  [optional] |
|**idPCertificate** | **String** |  |  [optional] |
|**authorizationUrl** | **String** |  |  [optional] |
|**clientId** | **String** |  |  [optional] |
|**clientSecret** | **String** |  |  [optional] |
|**issuer** | **String** |  |  [optional] |
|**scopes** | **List&lt;String&gt;** |  |  [optional] |
|**tokenAuthMethod** | **String** |  |  [optional] |
|**tokenUrl** | **String** |  |  [optional] |
|**userInfoUrl** | **String** |  |  [optional] |



## Enum: ConnectionTypeEnum

| Name | Value |
|---- | -----|
| OIDC_CUSTOM | &quot;oidc_custom&quot; |



