---
ms.date: 12/06/2024
title: Publish reports
description: Provides instructions to Viva Insights analysts and admins on how to publish and view insights reports and customize their settings.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Publish reports (preview)

>[!IMPORTANT]
> This feature is for public preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

The Publish reports feature lets you share insights and reports directly with leaders, decision-makers, or even an entire organization in the recipient’s Viva Insights app. This helps to streamline the communication process between analysts and leadership, ensuring that organizational insights and data are delivered effectively alongside other Viva Insights content.

A “report” refers to any analyst-created dashboard that includes Viva Insights metrics, though it might also feature other types of metrics like surveys or Copilot metrics. Typically, this dashboard is a Power BI, but other formats are possible. You might have already shared this report via email, but with this feature you can publish it seamlessly within Viva Insights.

Here’s a few more details about how it works:

* With this feature, you publish your report as a prominently displayed card on the recipient’s Viva Insights home page.

* We’ll help you create the card, which includes a title, description, and a link to your report.

* You select the card’s recipient(s), and specify how long you want it to be published.

* After publishing, cards always appear at the top of recipient’s home page, and you can track the impact using their unique card IDs.

## Prerequisite

This feature is off by default. To enable this feature in your tenant, Insights admins must first agree to the [Microsoft Viva Preview Agreement terms](/legal/viva/vccp-pre-release-agreement). To do so, use [this page](https://analysis.insights.cloud.microsoft/analyst/publishReports) to agree to these terms and enable this feature in your tenant.

## Roles and permissions

You can access this feature within the advanced insights app.

* Analysts can create new publishes, view publishes, and remove any existing publishes.

* Insights admins can view publishes and set which analysts can publish using Viva Feature Access Management (VFAM).

## Publish reports landing page

This page displays all the publishes within the past year from the partition, regardless of their state.  From this page, you can manage your previous publishes, as well as publish a new report.

When viewing existing publishes, you can see details on the author, publish name, publish date, end date, status, and actions.

:::image type="content" source="../images/publish-reports-landing-page.png" alt-text="Screenshot that shows the publish reports landing page.":::

|Term |Description |
|---|---|
|Author |The email address of the person who published the report. |
|Publish name | A friendly name for the publish that’s only visible in the advanced insights app, and not to any recipients. |
| Publish date | The date the publish was made. |
| End date | The date recipients will no longer be able to see this publish. The end date is selected by the publisher at the time of publish. |
| Status | The current state of the publish. It can be one of five values:  <br><br /><li> **Publishing**: The state of the report immediately after publishing. This state will generally exist for up to 10 minutes as the system delivers the publish to recipients.  <li>**Published**: The report is currently available for recipients to view in their Viva Insights app. <li>**Ended**: The report reached its scheduled end time, and is no longer available for recipients to view in their Viva Insights app. <li>**Removed**: Before a report reached its scheduled end date, an analyst removed a publish so recipients can no longer view it in their Viva Insights app. <li>**Failed**: The report was unable to be published due to system errors. |
| Actions | For any publish in the list, there are a set of available actions:   <br><br /><li>**View publish**: This is available for all publishes and lets you see the details of a publish. <li>**Remove publish**: This is only available for actively published reports. This will remove a publish so that it’s no longer available for recipients to view in their Viva Insights app. The status will change to **Removed**. <li>**Re-publish**: This is only available for failed reports. This attempts to re-publish a failed report.|

## How to publish a new report

Under the **Analysis** tab in the advanced insights app, select **Publish reports**. Then, at the top right, select **Publish new**.

### Create your card

The card you create is what recipients will see on their Viva Insights app homepage.  Fill out the details for this card and ensure it looks accurate via the card preview before publishing. You’re responsible for the content that appears on your published cards.

* **Report Link**: Provide the URL where the report can be accessed.

    >[!IMPORTANT]
    > This feature does not provide recipients permissions to the URL you’re publishing. Ensure that you have already made this URL available to your recipient audience so there aren’t permissions issues when recipients access this link from the card.

    * If you're publishing a Power BI report, ensure that you have already shared it with your desired audience so they can access the content once you publish. [Learn more about sharing Power BI reports](/power-bi/collaborate-share/service-share-dashboards).  

    >[!IMPORTANT]
    > This feature does not filter or edit the data based on viewer, so whatever you publish is published as-is to all recipients.

    * If you're publishing a Power BI report, consider adding [row-level security](/fabric/security/service-admin-row-level-security) to it if you want viewers to only see a subset of the data that is applicable to them.

* **Card Title**: Choose a concise and descriptive title for your report. This can’t be empty and must be less than 100 characters.

* **Publisher Name**: Keep your name or update it to reflect the entity publishing the report. This can’t be empty and must be less than 100 characters.

* **Description**: Write a summary of the report's content and its relevance to the target audience. This can’t be empty and must be less than 500 characters.

Ensure this content looks accurate by reviewing the preview on the right side of the page. 

Here's an example:

Let's say you want to publish your Hybrid workplace dashboard. This dashboard is saved to your Power BI workspace and has already been shared with your desired audience. It does not have row-level security implemented, so recipients see all the data in the report. You can create your card like the one below and publish it under your team name, HR Analytics, rather than using your own name as publisher. You can see how this card will look when it’s published to  your recipients with the Preview.

:::image type="content" source="../images/publish-reports-create-card.png" alt-text="Screenshot that shows the create card page.":::

### Select target audience