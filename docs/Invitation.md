

# Invitation


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | The unique identifier for the invitation. The ID is typically in the format *inv_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. |  [optional] |
|**emailId** | **String** | The email address of the user to whom the invitation is sent. |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | The status of the invitation. Possible values are *invited*, *accepted*, *expired*, and *revoked*. |  [optional] |
|**roleIds** | **List&lt;String&gt;** | The list of role IDs associated with the invitation. Each role ID is typically in the format *role_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. |  [optional] |
|**orgId** | **String** | The unique identifier for the organization associated with the invitation. The ID is typically in the format *org_&lt;unique_id&gt;*, where *&lt;unique_id&gt;* is a string of alphanumeric characters. |  [optional] |
|**createdDate** | **OffsetDateTime** | The date and time when the invitation was created, UTC format. |  [optional] |
|**expirationDate** | **OffsetDateTime** | The date and time when the invitation expires, UTC format. |  [optional] |
|**modifiedDate** | **OffsetDateTime** | The date and time when the invitation was last modified, UTC format. |  [optional] |
|**inviterUid** | **String** | The unique identifier for the user who sent the invitation. The ID is typically in the format unique_id, where *&lt;unique_id&gt;* is a string of alphanumeric characters. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| INVITED | &quot;invited&quot; |
| ACCEPTED | &quot;accepted&quot; |
| EXPIRED | &quot;expired&quot; |
| REVOKED | &quot;revoked&quot; |



