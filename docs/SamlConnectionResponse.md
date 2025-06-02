

# SamlConnectionResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**idPEntityId** | **String** | Unique identifier for the Identity Provider (IdP). |  [optional] |
|**idPMetadataUrl** | **String** | URL to the IdP metadata XML file. |  [optional] |
|**isIDPInitiated** | **Boolean** | Indicates whether the SAML connection is initiated by the IdP. |  [optional] |
|**idPCertificate** | [**OrganizationsConnectionSamlBaseIDPCertificate**](OrganizationsConnectionSamlBaseIDPCertificate.md) |  |  [optional] |
|**connectionType** | [**ConnectionTypeEnum**](#ConnectionTypeEnum) | The type of SAML connection. |  [optional] |
|**entityId** | **String** | The unique identifier for the SAML service provider. |  [optional] |
|**metadataUrl** | **String** | The URL to the SAML metadata XML file. |  [optional] |
|**acSEndpoint** | **String** | The Assertion Consumer Service (ACS) endpoint URL for SAML responses. |  [optional] |
|**spCertificate** | [**SamlConnectionResponseAllOfSPCertificate**](SamlConnectionResponseAllOfSPCertificate.md) |  |  [optional] |



## Enum: ConnectionTypeEnum

| Name | Value |
|---- | -----|
| SAML_CUSTOM | &quot;saml_custom&quot; |
| SAML_OKTA | &quot;saml_okta&quot; |
| SAML_ENTRAID | &quot;saml_entraid&quot; |
| SAML_GOOGLE_WORKSPACE | &quot;saml_google_workspace&quot; |
| SAML_SALESFORCE | &quot;saml_salesforce&quot; |



