---
title: "Mendix Advanced Scheduler"
url: /appstore/app-services/mendix-advanced-scheduler/
category: "Widgets"
description: "Describes the configuration and usage of Mendix Advanced Scheduler widget, which is available in the Mendix Marketplace."
tags: ["marketplace", "marketplace component", "platform support"]
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details. 
---

## 1 Introduction

The [Mendix Advanced Scheduler](#needsurl) enables you to load resources and events and visualize them. It offers you options to use a fixed timeline or a dynamic timeline for to view schedules. With a fixed timeline, you can navigate through time using buttons, and a dynamic timeline enables you to scroll through the time.

## 2 Installation

### 2.1 Starting a Subscription {#obtain-license-key}

{{% todo %}}Check if this works.{{% /todo %}}

Mendix Advanced Scheduler is a premium Mendix product that is subject to a purchase and subscription fee. You can deploy Mendix Advanced Scheduler locally or in a Mendix Free App for free. However, to deploy Mendix Advanced Scheduler on the cloud, you need to start a subscription to get a license token and [configure](#) it later. To start a subscription, contact your Customer Success Manager (CSM) or the Mendix Sales organization.

### 2.2 Installing the Component in Your App

To download and install Mendix Advanced Scheduler app service in your app, click the **Contact Us** button on the [Mendix Advanced Scheduler](#needsurl) Marketplace page. 

Then follow the instructions in the [Importing Content from the App Explorer](http://localhost:1313/appstore/general/app-store-content/#import) section in *Use Marketplace Content in Studio Pro* to import the component into your app.

## 3 Configuration 

### 3.1 Configuring the Mendix Scheduler Widget

#### 3.1.1 Views Tab

* **Scheduler Start Date** – This is the start date of the scheduler.

* **Scheduler End Date** – This is the end date of the scheduler.

* **On changed time window** – You can set an action that is triggered if the time window is changed.

* **Views** – You can manage the available views on the list. All the views on this list will be shown in the view selector.
  
  {{< figure src="/attachments/appstore/app-services/mendix-advanced-scheduler/view-selector.png" >}}
  
  * **New** – You can add a new view with the following items:
    * **ID of the view** – This is the ID used to define a view.
  
    * **Name of the view** – This is the name of the view.
  
    * **Default or Custom view** – You can select whether you use one of the following default views or a custom view:
      * **Day** – If selected, you use this default view.
      
      * **Week**– If selected, you use this default view.
      
      * **Month** – If selected, you use this default view.
      
      * **Year** – If selected, you use this default view.
      
      * **Custom** – If selected, you use a custom view.
        * **Unit of time** – You can define the unit of time used in the custom view.
        * **Visible timeline** – You can define how many units of time are visible in the time window.
        * **On prev/next button skip** – You can define how many units of time get skipped when you click the previous button (**<**) or the next button (**>**).
      
    
  * **Delete** – You can delete the selected view.
  
  * **Edit** – You can edit the selected view.
  
  * **Move up** – You can move up the selected view.
  
  * **Move down** – You can move down the selected view.
  
* **Selected View** – This is an attribute of an entity in your Domain Model, which is used to change the view in Mendix. You can build logic around this in your app or implement your own switching mechanism in your own custom header.

* **Fixed Timeline**
  * **Yes** – If selected, you cannot change the timeline in the time window.
  * **No** – If selected, you can scroll along the timeline.

#### 3.1.2 Resources Tab

* **Resources Datasource** – This is the data source for the resources that are shown on the left side of the scheduler.
* **Resource ID** – This is the ID of the resource.
* **Resource Classname** – This is the class name of the resource, which can be used for the styling of the resource.
  * If left empty, the value is set to *resource-type-default*.
* **On Click** – You can set an action that is triggered when the resource is clicked.

#### 3.1.3 Events Tab

*  **List of Data sources** – You can manage the data sources of events on the list.
    *  **New** – You can add a new data source with the following items:
        * **General** tab
          * **Data source** – This is the data source of the event.
          * **Event ID** – This is the ID of the event.
          * **Resource ID** – This is the ID of the corresponding resource.
          * **Before event travel time** – You can add some travel time before the event.
          * **Start event** – This is the start date of an event.
          * **End event** – This is the end date of an event.
          * **After event travel time** – You can add some travel time after the event.
          * **Movable** – You can select a Boolean attribute to indicate whether the event can be dragged to a different time slot on the timeline.
          * **Resizeable** – You can select a Boolean attribute to indicate whether the length of the event can be resized.
        * **UI** tab
          * **Event content** – This is the title of the event. It supports HTML.
          * **Tooltip content** – This is the content of the tooltip of the event.
          * **Classname** – This is the class name of the event, which can be used for the styling of an event.
            * If left empty, the value is set to *event-type-default*.
        * **User interaction** tab
          * **On click action** – You can set an action that is triggered when the event is clicked.
          * **On change action** – You can set an action that is triggered when the event is moved to a different time slot on the timeline or when its length is resized.
    *  **Delete** – Yo can delete the select data source.
    *  **Edit** – You can edit the selected data source.
    *  **Move up** – You can move up the selected data source.
    *  **Move down** – You van move down the selected data source.
* **Create new events**
  * **Yes** – If selected, you can create a new event by selecting an empty area in the timeline and then dragging the borders to define the start and end time or by double-clicking a time slot. 
  * **No** – If selected, you cannot create a new event by drag and drop or double-clicking a time slot.
*  **On create event action** – You can set an action that is triggered when a new event is created.
*  **Last Moved Event Id** – The ID that references the event that has been last moved
*  **New Resource ID** –  The ID  that references the resource that an event has been moved to
*  **New Start Event** – The new start time of the dragged event
* **New End Event** – The new end time of the dragged event

#### 3.1.4 Rosters Tab

{{% alert color="info" %}}The roster has a light yellow background in the scheduler.{{% /alert %}}

{{< figure src="/attachments/appstore/app-services/mendix-advanced-scheduler/roster.png" >}}

* **Datasource** – This is the data source for the roster.
* **Resource ID** – This is the resource ID for the roster.
* **Start date time** – This is the start date of the roster.
* **End date time** – This is the end date of the roster.
* **Name of the roster** – This is name displayed in the roster.
* **ClassName** – This is the class name of the roster, which can be used for the styling of a roster.
  * If left empty, the value is set to *event-type-default*.

#### 3.1.5 UI Tab

* **Today button**  – You can change the text shown on the **Today** button, for example, to the translation of "today" in a different language.
* **Hide navigation**
  * **Yes** – If selected, the navigation, including the previous button (**<**), the next button (**>**), the **Today** button, and the view selector, is hidden. You can create your own Mendix buttons.
  * **No** – If selected, the navigation, including the previous button (**<**), the next button (**>**), the **Today** button, and the view selector, is visible.

#### 3.1.6 Common Tab

For more information, see [Common Section](/refguide/common-widget-properties/#common-properties) in *Properties Common in the Page Editor*.

#### 3.1.7 Appearance Tab

The properties in the Appearance tab have no influence on the widget. This tab can be ignored.

### 3.2 Configuring the Header Dropzone

{{< figure src="/attachments/appstore/app-services/mendix-advanced-scheduler/header-dropzone.png" >}}

You can define your own header in this area. The header will be shown above the scheduler, and override the default header. You will also lose options like changing view or moving days. 

{{< figure src="/attachments/appstore/app-services/mendix-advanced-scheduler/header.png" >}}

### 3.3 Configuring the Resource Area

{{< figure src="/attachments/appstore/app-services/mendix-advanced-scheduler/resource-area.png" >}}

You can define what is shown as **Resources** in the scheduler in this area.

{{< figure src="/attachments/appstore/app-services/mendix-advanced-scheduler/resources.png" >}}

### 3.4 Configuring the License Key {#configure-license-key}

You can deploy the Mendix Advanced Scheduler locally or in a Mendix Free App for free. However, to deploy the Mendix Advanced Scheduler in the Mendix Cloud, you need to start a subscription to [obtain a license key](#obtain-license-key), and then configure it.

Before you deploy your app, configure the app **Constants** in the deployment package in the [Developer Portal](https://docs.mendix.com/developerportal/deploy/environments-details/).

If you have already deployed your app, change the existing **Licensekey** constant value on the **Model Options** tab and restart the app.

## 4 Example Implementation

For an example about how to implement the widget, see the example implementation. {{% todo %}}Add the link and check the name of the example implementation.{{% /todo %}}
