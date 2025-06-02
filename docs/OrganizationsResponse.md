

# OrganizationsResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**display** | [**OrganizationBaseDisplay**](OrganizationBaseDisplay.md) |  |  [optional] |
|**domains** | [**List&lt;OrganizationsDomainsResponse&gt;**](OrganizationsDomainsResponse.md) | List of domains associated with the organization |  [optional] |
|**metadata** | **Map&lt;String, String&gt;** | Additional metadata for the organization |  [optional] |
|**name** | **String** | Name of the organization |  [optional] |
|**connections** | [**List&lt;ConnectionResponse&gt;**](ConnectionResponse.md) | List of connections associated with the organization |  [optional] |
|**createdDate** | **OffsetDateTime** | Date when the organization was created |  [optional] |
|**id** | **String** | Unique identifier for the organization |  [optional] |
|**isActive** | **Boolean** | Indicates whether the organization is active |  [optional] |
|**modifiedDate** | **OffsetDateTime** | Date when the organization was last modified |  [optional] |
|**policies** | [**OrganizationsPolicyBase**](OrganizationsPolicyBase.md) |  |  [optional] |



