---
demo:
    title: 'Demonstration: Administer Identity'
    module: 'Administer Identity'
---

# 1 - Administer Identity

## Configure Azure Active Directory

This area does not have a formal demonstration. Consider these
Quickstarts.

[Quickstart - Access & create new tenant - Azure AD \| Microsoft
Docs](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-access-create-new-tenant)

[Quickstart - View groups & members - Azure AD \| Microsoft
Docs](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-view-azure-portal)

## Configure User and Group Accounts

In this demonstration, we will explore Azure Active Directory.

**Note:** Depending on your subscription not all areas of the Azure
Active Directory blade will be available.

> [Add or delete users - Azure Active Directory \| Microsoft
> Docs](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory)
>
> [Create a basic group and add members - Azure Active Directory \|
> Microsoft
> Docs](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal#create-a-basic-group-and-add-members)

**Review license and domain information**

1.  Access the Azure portal and navigate to the **Azure Active
    Directory** blade.

2.  On the Overview blade, review the **Tenant information** including
    license and primary domain.

**Explore user accounts**

1.  Select the **Users** blade.

2.  Explain the choices for **New user** and **New guest user**.

3.  Select **New user** and discuss the differences between **Create
    user** and **Invite user**.

4.  Create a **New user** reviewing the **Identity**, **Groups and
    roles**, **Settings**, and **Job Info** parameters.

5.  After the user is created, review **Reset password**, **Delete
    user**, and **Sign-ins**.

**Explore group accounts**

1.  Return to the **Azure Active Directory** page and select
    the **Groups** blade.

2.  Create a **New group** or select an existing group to review.

3.  Review information about a group including **Membership
    type** and **Type**.

**Optional - Explore PowerShell for group management**

1.  Create a new group called Developers.

> **New-AzADGroup -DisplayName Developers -MailNickname Developers**

2.  Retrieve the Developers group ObjectId.

> **Get-AzADGroup**

3.  Retrieve the user ObjectId for the member to add.

 **Get-AzADUser**

4.  Add the user to the group. Replace groupObjectId and userObjectId.

> **Add-AzADGroupMember -MemberUserPrincipalName
> \"\"myemail@domain.com\"\" -TargetGroupDisplayName
> \"\"MyGroupDisplayName\"\"**

5.  Verify the members of the group. Replace groupObjectId.

> **Get-AzADGroupMember -GroupDisplayName \"MyGroupDisplayName\"**