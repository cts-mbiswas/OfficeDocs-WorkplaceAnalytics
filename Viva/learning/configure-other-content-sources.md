---
title: Add other content providers for Microsoft Viva Learning
ms.author: chucked
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 11/04/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - highpri
ms.localizationpriority: medium
description: Learn how to configure other content providers as a learning content source for Microsoft Viva Learning.
---

# Add other content providers for Microsoft Viva Learning

A growing set of learning content providers is available through Viva Learning. This set can change at any time as more providers join or change their status with the program.

Some learning sources are enabled by default and available without a Viva Suite or Viva Learning license. These learning sources include:

- [Global skilling initiative (GSI) courses](https://opportunity.linkedin.com/skills-for-in-demand-jobs) from LinkedIn Learning or the full LinkedIn Learning course catalog with a LinkedIn Learning Enterprise subscription.
- Microsoft Learn
- Microsoft 365 Training

Third-party content sources aren't enabled by default. To enable these sources, you need to [add them in the Viva Learning Admin tab](/viva/learning/use-tabs) and follow the specific instructions shown in the following table.

> [!NOTE]
> You'll need a Viva Learning or Viva Suite license to access this feature. [Learn more about licensing](https://www.microsoft.com/microsoft-viva/learning).

> [!NOTE]
> It can take 24 to 48 hours for Viva Learning users to see content for the sources you enabled in the admin portal. It can also take 24 to 48 hours to hide content from LinkedIn Learning, Microsoft Learn and Microsoft 365 trainings from Viva Learning after you have disabled them in the admin portal.

|Content provider  |Configuration instructions  |
|---------|---------|
|Go1     |[Configure Go1 as a content source](configure-go1-content-source.md)         |
|OpenSesame    |[Configure OpenSesame as a content source](configure-opensesame-content-source.md)    |
|Skillsoft     |[Configure Skillsoft as a content source](configure-skillsoft-content-source.md)         |
|Udacity    |[Configure Udacity as a content source](configure-udacity-content-source.md)    |
|Udemy   |[Configure Udemy as a content source](configure-udemy-content-source.md)         |
|Coursera    |Follow the steps below to add Coursera in the Viva Learning Admin tab   |
|edX    |Follow the steps below to add edX in the Viva Learning Admin tab.    |
|Infosec    |Follow the steps below to add Infosec in the Viva Learning Admin tab   |
|Josh Bersin Academy    |Follow the steps below to add Josh Bersin Academy.    |
|Pluralsight    |Follow the steps below to add Pluralsight in the Viva Learning Admin tab   |

 


Refer to the details mentioned in [Manage providers in Viva Learning](/viva/learning/use-tabs) to configure any provider in Viva Learning Admin tab. 

> [!NOTE]
> Available content providers are subject to change. Depending on your organization, you may have access to more content providers than are listed here.

## Dataflow architecture

The dataflow diagram shows how Viva Learning ingests third-party content. The third-party provider is the ultimate source of information for content records for their customers. Viva Learning extracts the content from the third-party provider using the connector.

![Flow chart depicting the content ingestion process, which is described in the paragraph below.](../media/learning/3p-dataflow.png)

The step-by-step content ingestion process is described below.

1. **Third-party provider** <br> Viva Learning requires content catalog data from every third-party content source. The various fields extracted as part of the Content Catalog package or API from the content source are represented in the table [View the table](#content-catalog-metadata-fields).

2. **Third-party Connector** <br> The third-party Connector pulls content from the content provider using both API and SFTP mechanisms. The first time you sync, the third-party extractor pulls the full data. Afterwards, a scheduler triggers once every 24 hours to refresh the data and pull any changes. Then the extract is validated and processed. If you encounter an error in processing, the error code displays on the admin portal. User records received from the extract are mapped with Microsoft Entra ID records to ensure the correct assignment and completion status for every user. Once all the records are processed, the data is synchronized to Viva Learning application and displayed on the Viva Learning app.

3. **Viva Learning** <br> Content details (content provider logo, thumbnail, title, description, etc.) display on the **Home** and **Learning** tabs in Viva Learning.

### Content catalog metadata fields

|Metadata field name |Field details |Priority |
|:-------------------|:-------------|:--------|
|Content provider name | Third-party content provider's name. This can be provided separately and appended. |Required |
|Content provider logo URL | URL to the third-party provider's logo for display purposes. |Required |
|Content source name |Course content source's name |Required if integrated with provider |
|Content source logo |Course content source's logo |Required if integrated with provider |
|Title of learning content |Title of learning content |Required |
|Content module's thumbnail URL |URL to the learning content thumbnail image for display purposes |Required |
|Content module's URL (deep link to consume content) |URL to learning content. This is the link that the user selects to consume content. |Required |
|Content module description/summary |Description or summary of learning content |Required |
|Content language/locale |Language in which content is available. Metadata should be provided in all available languages. |Required |
|Content module duration |Time duration of learning content |Required |
|Last modified date of content module or content creation date |Date the learning content was last modified |Required |
|Content format |Content format, such as article or video |Required |
|Assigned user role |Roles or groups that have permissions to the content  |Required for role-based access |
|Content ID |Unique identifier for learning content |Recommended |
|Content module author/creator/contributor |Author/creator/contributor of learning content |Recommended |
|Content module length/size |Size of content, not based on time. For example, this could be the number of pages. |Recommended |
|Tags and keywords |Keywords, topics, and other tags associated with the learning content |Recommended |
|Difficulty level |Difficulty level of the course (such as beginner, intermediate, or advanced) |Recommended |
|Content module thumbnail alt text |Alternative text to support accessible design for images. Text describes images and can be invoked by screen readers for users with assistive technology. |Recommended |
|Popularity score |Rating or popularity score for learning content |Recommended |
|Skills associated |Skills tags associated with the learning content |Recommended |

## Content ingestion errors

[Learn how to address content ingestion errors from third-party providers](provider-content-ingestion-errors.md).

## Content consumption for end users

Once you've added a content provider as a content source, content from the provider flows to Viva Learning and become visible to end users.

Once a user chooses to play a course in Viva Learning, they're directed to the content provider's webpage. They need to enter the sign-in credentials on the provider's sign-in page. [Learn more about how to consume content with Viva Learning](https://support.microsoft.com/office/01bfed12-c327-41e0-a68f-7fa527dcc98a).
