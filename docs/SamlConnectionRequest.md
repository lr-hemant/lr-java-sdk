

# SamlConnectionRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Name of the connection |  [optional] |
|**domain** | **String** | Domain associated with the connection |  [optional] |
|**attributes** | [**OrganizationsConnectionBaseAttributes**](OrganizationsConnectionBaseAttributes.md) |  |  [optional] |
|**idPEntityId** | **String** | Unique identifier for the Identity Provider (IdP). |  [optional] |
|**idPMetadataUrl** | **String** | URL to the IdP metadata XML file. |  [optional] |
|**isIDPInitiated** | **Boolean** | Indicates whether the SAML connection is initiated by the IdP. |  [optional] |
|**idPCertificate** | **String** |  |  [optional] |
|**connectionType** | [**ConnectionTypeEnum**](#ConnectionTypeEnum) |  |  [optional] |



## Enum: ConnectionTypeEnum

| Name | Value |
|---- | -----|
| SAML_CUSTOM | &quot;saml_custom&quot; |
| SAML_OKTA | &quot;saml_okta&quot; |
| SAML_ENTRAID | &quot;saml_entraid&quot; |
| SAML_GOOGLE_WORKSPACE | &quot;saml_google_workspace&quot; |
| SAML_SALESFORCE | &quot;saml_salesforce&quot; |



