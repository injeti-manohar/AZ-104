> Azure Active Directory (Azure AD) is Microsoft’s cloud-based identity and access management service, which helps your employees sign in and access resources

Azure AD helps you authenticate in - 
- `External resources`, such as Microsoft 365, the Azure portal, and thousands of other SaaS applications(like wordpress, even AWS)
- `Internal Resources`

**Features:**

| **Category** | **What AAD Offers** |
| ---- | ------|
| Application Management | [App Management Docs ](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/) |
| Authentication |    [Docs](https://docs.microsoft.com/en-us/azure/active-directory/authentication/) |
| Business-to-Business (B2B) |  [B2B Docs](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/) | 
| Business to Customer (B2C) |   [B2C](https://docs.microsoft.com/en-us/azure/active-directory-b2c/) | 
| Conditional Access | 

### Groups
the group is synced from on premises Windows AD they cannot be managed in Azure AD. They must be managed on-prem 

### Service Principal
An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.

For example, you can assign roles to allow adding or changing users, resetting user passwords, managing user licenses, or managing domain names.

Who signs up for Azure AD is global administrator

# Active directory

Active Directory Domain Services (AD DS), provides the methods for storing directory data and making this data available to network users and administrators.
For example, AD DS stores information about user accounts, such as names, passwords, phone numbers, and so on, and enables other authorized users on the same network to access this information
[Learn more from Microsoft docs](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview)
[High level overview of AD](https://www.pcwdld.com/active-directory-guide)

## Ad Ds Vs Azure AD
**NTLM** - Windows New Technology LAN Manager (NTLM) is a suite of security protocols offered by Microsoft to authenticate users' identity 


## terms and concepts

- Trust - trust is a relationship which is established between two domains so that one domain can be authenticated by the () domain controller of other domain. 
