---
title: "Viva Engage file storage overview"
description: "Where files are stored in Viva Engage depends on whether the network uses Microsoft 365 connected groups."
f1.keywords:
- NOCSH
ms.author: donnabouldin
author: Starshine89
manager: elizapo
ms.date: 01/04/2024
audience: Admin
ms.topic: article
ms.service: viva
ms-subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
---

# Viva Engage file storage overview

Files uploaded to posts in Viva Engage networks in Microsoft 365 are stored in SharePoint. Files in community posts are stored in the document library that backs up the community; storyline posts are stored in a hidden library in the creator’s OneDrive.

- Learn about [File Storage for storyline posts](https://learn.microsoft.com/viva/engage/eac-storyline#file-storage-for-storyline)
- Learn about [Viva Engage and Microsoft 365 groups](https://learn.microsoft.com/viva/engage/engage-microsoft-365-groups)
- Learn how to [Enable or Disable the Community Resources Module and Files Tab](https://support.microsoft.com/en-gb/topic/manage-viva-engage-community-resources-08fc99bf-c36c-425b-9a98-079e62510135).

> [!NOTE]
> If users upload files in connected Viva networks, policies in SharePoint document libraries take precedence over Viva Engage upload admin configurations.

> [!Important]
> **Avoid using SharePoint to modify, replace, delete, move, or rename** the folder structure (**Documents > Apps > Viva Engage**), documents, and rich media for your Viva Engage network. Changing these elements in SharePoint will break the front-end experience of posts, in communities, and in your storyline.

An exception exists to the preceding rule. When the Viva Engage network isn't connected to Microsoft 365 groups, files uploaded to posts are stored directly in Viva Engage cloud storage. This includes the following:  

- Microsoft 365 tenants that have more than one Viva Engage network  
- Viva Engage networks that don't enforce Office 365 identity  
- Viva Engage basic networks.

<!-- Links in the short bulleted list to be hidden but keep for possible future use per request-->

<!--
For information about using Viva Engage files stored in SharePoint, see the following articles:

 - [Where are my Viva Engage files stored?](https://support.microsoft.com/office/how-do-i-tell-where-my-viva-engage-files-are-being-stored-fadfdefa-e00d-40b6-94cb-a9ddb171a443)

- [Edit a previously uploaded file when your Viva Engage connected group now stores files in SharePoint](https://support.microsoft.com/office/edit-a-previously-uploaded-file-when-your-viva-engage-connected-group-now-stores-files-in-sharepoint-4b2cfde2-871e-4f0d-9936-db5a57ef5f87) 
-->

## Benefits

For network and tenant administrators:

- SharePoint has a rich set of security and compliance features that apply to files uploaded in Viva Engage for Microsoft 365 connected Viva Engage groups. Features include eDiscovery, data loss protection, and in-geo residence for files at rest.  

For end users:
  
- A familiar user interface for file navigation and management in SharePoint.

- Greater discoverability and easier access through Microsoft search.

    Users with appropriate permissions can find and access the files through Viva Engage, SharePoint, and other Microsoft 365 resources by using browse or search in SharePoint and Delve.  

- Offline access to files by syncing a SharePoint folders to a folder on their computer.  
  
## How to restore a Microsoft 365 group or document library that backs a connected community

Community posts can lose attached files and rich media when the Microsoft 365 group that backs up a connected community is deleted, when the group's SharePoint library is deleted, or if the folder structure (**Documents > Apps > Viva Engage**) is deleted or moved from their location. 

To restore a deleted group, contact your administrator, Help desk, IT, or technical support department. For more information, see [Restore a deleted Microsoft 365 group](https://docs.microsoft.com/microsoft-365/admin/create-groups/restore-deleted-group?view=o365-worldwide). 

To restore a document library, follow the instructions in [Restore items in the recycle bin that were deleted from SharePoint or Teams](https://support.microsoft.com/office/restore-items-in-the-recycle-bin-that-were-deleted-from-sharepoint-or-teams-6df466b6-55f2-4898-8d6e-c0dff851a0be).

### Delete files uploaded to deleted community or storyline posts 

If a file or rich media gets removed from a post, it isn't removed from SharePoint or OneDrive. They remain shared and accessible to anyone with access to that community or storyline.  

To fully delete the file, ensure the attachment is removed from the post or from the reply. If the post or reply is already published, the author or a community admin can select the overflow menu (...) and then choose **Edit**. You can also delete the entire post or reply. Then, perform one of the following deletion tasks in SharePoint: 

**To delete files removed from a post or a reply in a community**:

1. Open the SharePoint library backing the community. You can do this one of two ways, depending on your environment:
    - Select the Files tab on the community;
    - Select **SharePoint Library** from the **Community resources** module in the community’s right navigation. 
2. Navigate to the **Documents > Apps > Viva Engage** folder. 
3. Locate the file previously attached to the post and select **Delete**. 

**To delete files removed from a post or a reply on a storyline**: 

Files attached to storyline posts are stored in a hidden library in the author’s OneDrive. There's no entry point to this location in the Microsoft 365 user experience, but you can access it through a URL resembling the following example:  

    `https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage/Attachments/Storyline` 

To determine the precise URL for a user's storyline page, follow these steps: 

1. Open the user's OneDrive in a browser. 

2. Note the URL to the user's OneDrive. 

3. Locate the user identifier, which is the part of the URL immediately that follows `my.sharepoint.com/personal/`.

4. Replace everything after the profile identifier and the backslash plus VivaEngage, without a space, case insensitive. The resulting URL resembles this example:

    `https://<tenantname>-my.sharepoint.com/personal/<useridentifier>/VivaEngage` 

5. Press **Enter**. The library appears.

6. Open the **Attachments > Storyline** folder. The URL to the folder where storyline files are saved resembles this example

    `https://<tenantname>-my.sharepoint.com/personal/<user identifier>/VivaEngage/Attachments/Storyline`

7. Locate the previously attached file and select **Delete**.

Files that users upload in Microsoft 365 connected groups are saved in the **Apps > Viva Engage** subfolder of the SharePoint document library for the group. Users can access the SharePoint document library from Viva Engage under **Microsoft 365 Resources** or **Office 365 Resources** on the right side of a Viva Engage group, or through SharePoint itself. The Viva Engage group must be Microsoft 365 connected.

 > [!NOTE]
 > We recommend that you do not delete, move, or rename files in the **Apps > Viva Engage** subfolder.

## How to resolve images that appear blank in Viva Engage conversation threads

Files attached to community posts are stored in the SharePoint’s document library that backs up the community. Files are stored in the path **Documents > Apps > Viva Engage**.  

If the library location changes, files and images attached to community posts could appear blank. To solve this issue, do the following: 

1. Move the contents of the duplicated folders into the official **Apps/Viva Engage** folder.

2. Once they're empty, delete all duplicated folders.

3. Ensure the permissions on the official **Apps/Viva Engage** folder are the default ones. 

To find the document library that backs up the community, use the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) API `https://graph.microsoft.com/v1.0/groups/{office_365_group_id}/drive/special/approot/` and change the `office_365_group_id` attribute in the API call to the community ID. The following example illustrates:

`https://graph.microsoft.com/v1.0/groups/contoso_program_managers_group/drive/special/approot/`

- Learn [How do I find a community's group feed ID in Viva Engage](https://support.microsoft.com/office/how-do-i-find-a-community-s-group-feed-id-in-viva-engage-9372ab6f-bcc2-4283-bb6a-abf42dec970f#:~:text=To%20find%20the%20group%20ID%20for%20a%20Viva,an%20online%20tool%20to%20decode%20base%2064.%20) 

- Learn [How Yammer evolved to Viva Engage](https://techcommunity.microsoft.com/blog/viva_engage_blog/yammer-is-evolving-to-viva-engage/3738825) 

> [!Important]
> For communities created before March 2023, the SharePoint document libraries are named **Viva Engage**.
  
## Guest access to files

The following table shows how each type of guest can access files uploaded in Viva Engage and stored in SharePoint.

| Type of user | Access to group files in Viva Engage | Access to group files in SharePoint |
|----------|----------|----------|
|**Conversation-level guest that is in your network**|**Private group**: Can view files shared in the conversation, but can't upload files.<br/>**Public group**: Can view, edit, and upload files.|Conversation level guests can't access any files saved in SharePoint nor upload any files. If you want to enable access to specific files in the conversation, add them as an Azure B2B guest on the Office 365 tenant. File upload isn't permitted.|
|**Network-level guest that is also an Azure B2B guest, and also a member of the group in Microsoft 365**|Can view, edit, and upload files.|These Azure B2B guests can view, upload, or edit files from the SharePoint Document library only. File access from Viva Engage isn't permitted.|
|**Azure B2B guest, but not a member of the group<br/>Network-level guest<br/>Conversation-level guest that isn't in your network**|Automatic file access isn't allowed. These users can request access to specific files.<br/>Can't upload files.|Automatic file access isn't permitted. Guests can request access to specific files. File upload isn't permitted.|
|**Network-level guest, but not Azure B2B guest**|Automatic file access isn't allowed. A guest must become an Azure B2B guest and a member of the group in Microsoft 365. Alternatively, other group members can grant access to specific files or the entire document library through one of many SharePoint external sharing methods.|No automatic access for network level guests to Viva Engage files saved in SharePoint. If you want to enable access to specific files, add them as an Azure B2B guest on the Office 365 tenant. For more information, see [Microsoft Entra B2B documentation](/azure/active-directory/b2b/). If guests need to upload files to a specific group from SharePoint or have automatic access to files uploaded to SharePoint, add them as a group member in SharePoint.|

> [!NOTE]
> Membership in the group for guests in Microsoft Entra ID and Viva Engage are completely separate. Deleting a network-level guest from a Microsoft 365 connected Viva Engage group or from the tenant in Microsoft Entra ID doesn't remove the user in Viva Engage, and deleting a user from Viva Engage doesn't delete the user from a Microsoft 365 group or Microsoft Entra ID.

For more information about Microsoft Entra B2B guests, see [Guest access in a Microsoft Entra B2B](/azure/active-directory/b2b/what-is-b2b).

## Requirements

- Viva Engage version requirements

    Ensure your users are using the most recent Viva Engage versions. At a minimum, users should be using the following or newer versions:

    - Viva Engage on iOS - 7.33.0  

    - Viva Engage on Android - 5.5.84

    - Viva Engage desktop on Windows or Mac - 3.4.2

- Cookie and browser requirements

    To store Viva Engage files in SharePoint, we use the ADAL library and use Microsoft Entra ID tokens for authentication. If browsers don’t have third-party cookies enabled or if the security zone settings are incorrect in Internet Explorer 11 or Edge, the ADAL library used to refresh Microsoft Entra tokens can't send information needed to Microsoft Entra ID.

    > [!NOTE]
    > Microsoft 365 apps and services doesn't support Internet Explorer 11 as of August 17, 2021. (Microsoft Teams doesn't support Internet Explorer 11 earlier, as of November 30, 2020.) [Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666). Note that Internet Explorer 11 remains a supported browser. Internet Explorer 11 is a component of the Windows operating system and [follows the lifecycle policy](/lifecycle/faq/internet-explorer-microsoft-edge) for the product on which it is installed.

    When a token refresh call fails, users see:

    - On the Viva Engage page for a connected group, Microsoft 365 Resources are dimmed

    - File operations fail

    - Viva Engage live events can't be created.

     For more information, see [A silent sign-in request was sent but no user is signed in](https://github.com/AzureAD/azure-activedirectory-library-for-js/wiki/FAQs#q6-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in).

    To avoid problems:

    - Ensure that no extensions (such as Ghostery) block or prevent reading of cookies.

    - In Internet Explorer 11 or Microsoft Edge, ensure protected mode is disabled for the trusted zone.

        Include **engage.cloud.microsoft** and related URLs as a part of trusted zone. For more information, see [Microsoft 365 URLs and IP address ranges](/microsoft-365/enterprise/urls-and-ip-address-ranges)

    - In complex environments, especially those using wildcard configurations such as *.fabrikam.com, more effort may be required to find the right configuration. URLs may need to be moved between zones, or replaced with the absolute versions in some cases.

    - Users shouldn’t access Viva Engage using incognito or InPrivate mode or equivalent modes in other browsers.
