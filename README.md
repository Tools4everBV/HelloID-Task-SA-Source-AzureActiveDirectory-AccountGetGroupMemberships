# HelloID-Task-SA-Source-AzureActiveDirectory-AccountGetGroupMemberships

## Prerequisites
- [ ] This script uses the Microsoft Graph API and requires an App Registration with App permissions:
  - [ ] Read all group memberships <b><i>GroupMember.Read.All</i></b>

## Description

This code snippet executes the following tasks:

1. Define `$userPrincipalName` based on the `selectedUser` data source input `$dataSource.selectedUser.UserPrincipalName`
2. Creates a token to connect to the Graph API.
3. List all user's memberships in Azure AD using the API call: [List a user's direct memberships](https://learn.microsoft.com/en-us/graph/api/user-list-memberof?view=graph-rest-1.0&tabs=http)
4. Return a hash table for each user account using the `Write-Output` cmdlet.

> To view an example of the data source output, please refer to the JSON code pasted below and select the `Interpreted as JSON` option in HelloID

```json
{
    "UserPrincipalName": "a.acevedo@domain.local"
}
```