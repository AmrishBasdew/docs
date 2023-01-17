---
title: "App Insights – Mini-Surveys"
url: /appstore/modules/app-insights/
category: "Modules"
description: "Describes the configuration and usage of the App Insights – Mini-Surveys module, which is available in the Mendix Marketplace."
tags: ["marketplace", "marketplace component", "app insights", "mini-survey", "mini survey"]
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details. 
---

## 1 Introduction

After you have created a mini-survey in [App Insights](/developerportal/collaborate/app-insights/) in the Developer Portal, use the [App Insights – Mini-Surveys](https://marketplace.mendix.com/link/component/205483) module to implement your mini-survey in Studio Pro.

## 2 Installation

To import this module into your app, follow the instructions in [How to Use Marketplace Content in Studio Pro](/appstore/general/app-store-content/).

## 3 Configuration {#configuration}

{{% alert color="info" %}}Before you configure this module in Studio Pro, make sure you have  [created your mini-survey](/developerportal/collaborate/app-insights/#create-survey) in **App Insights** in the Developer Portal. {{% /alert %}}

1. Open your app in Studio Pro.
2. In **App Explorer**, go to **Marketplace modules** > **AppInsights_MiniSurvey** > **_SETUP**.
3. Open the **Set API Key & mode** folder and do the following:

    1. Set the constant **APIKEY_APPINSIGHTS** to the [API key](/developerportal/collaborate/app-insights/#obtain-api-key) that you obtained.
    2. (Optional) Configure the constant **TEST_MODE**. If this is turned on, the survey will always show.
    3. Save the changes.

4. Open the **Put Survey Widget On Template** folder, and place **Template_SurveyWidget** on the page where you would like the mini-survey to appear.
5. Open the **Show Survey** folder, and copy the **ShowSurvey_OnAction** nanoflow to your own module.
6. Set up the **ShowSurvey_OnAction** nanoflow as follows:

    1. Double-click **Create String variable**, fill in the survey ID of the mini-survey, and then save the changes. You can find the survey ID on the [Settings](/developerportal/collaborate/app-insights/#survey-details-settings) tab or [Implementation](/developerportal/collaborate/app-insights/#survey-details-implementation) tab of the survey details page in **App Insights** in the Developer Portal.
    2. Double-click **CHANGE ME**, add your microflow or nanoflow action here,  then save the changes.

7. Create a button that calls the **ShowSurvey_OnAction** nanoflow on the page where **Template_SurveyWidget** is placed. Mendix recommends renaming the flow to something that describes the original action.
8. In **App Explorer**, double-click **Security**, and add the **AppInsights_MiniSurvey.User** user role to all the system roles that use the mini-survey in the **App Security** dialog box.

{{% alert color="info" %}}Once the start time of the mini-survey is reached, the mini-survey will start running, and all the target users of the mini-survey will receive the survey automatically.{{% /alert %}}
