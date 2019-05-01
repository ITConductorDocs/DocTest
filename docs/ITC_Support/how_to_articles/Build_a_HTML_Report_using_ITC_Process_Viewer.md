Build a HTML Report using ITC Process Viewer
============================================

Created by

[Too Choong](/people/5b7619017825cb0653519756?ref=confluence&src=profilecard)

Last updated [Sep 24, 2018](/wiki/pages/diffpagesbyversion.action?pageId=597262458&selectedPageVersions=13&selectedPageVersions=14)

This guide will take you through the process of creating a report using the ITC Process Viewer (the report needs to be in a Process in order for it tone scheduled). The Process can then be scheduled to run in a time slot as defined in the ITC Scheduler. When the scheduled run is completed, the report will be send to the receivers as configured during the report creation.  

Step-by-step guide
------------------

If you don't have an existing Process defined for use or require a new Process, follow steps 1-3 to create a Process before continuing.  The Process is required by the ITC Scheduler.

### 1 Start with My Objects

1.1 Select 'My Objects' from the Dashboard header menu.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-18_16-38-35.png?version=1&modificationDate=1537252720386&cacheVersion=1&api=v2&width=257&height=249)

  

### 2 Create Process Definition

2.1 Select 'Create New Object' icon to start the new Process definition.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-19_15-10-34.png?version=1&modificationDate=1537333838759&cacheVersion=1&api=v2&width=700&height=252)

  

### 3 Input Process Definition Details

3.1 The 'Create New Object' icon will display Process Definition screen for input.  Click on the 'General' tab as shown below.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-19_15-23-8.png?version=1&modificationDate=1537334593865&cacheVersion=1&api=v2&width=700&height=276)

  

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-19_16-17-18.png?version=1&modificationDate=1537337845440&cacheVersion=1&api=v2&width=700&height=497)

  

3.2 Enter the following inputs:

3.2.1 Name - this is the name of the Process. This field is mandatory.\\

3.2.2 Description - Process description, can be the same as the Process name.

3.2.3 Tenant - use the dropdown to select the Tenant where the Process will be created.

3.2.4 Owner - use the dropdown to select the owner, usually the nominated end-user (Customer). Ask the Tenant administrator, if unsure. (Note: if a different owner is used, then you will need to impersonate the owner to be able to retrieve and modify the Process subsequently).

3.2.5 Engine - use the dropdown to select the appropriate Engine to assign. Ask the Tenant administrator, if unsure.

  

3.3 Save the inputs

3.3.1 After completed the inputs above, select the 'Create new Process Definition' icon, on the top right corner of the screen. This will save the inputs and creates the Process Definition as named.

  

### 4 Display Process Definitions

4.1 The newly created Process Definition is now displayed on the screen.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_14-20-12.png?version=1&modificationDate=1537417216977&cacheVersion=1&api=v2&width=300&height=378)

  

4.2 Use the Process Viewer to maintain the process in the Process Definition.\\

4.2.1 Click on the 'Process Definition' icon next to the process name. A dropdown list of actions will be displayed.

4.2.2 Select the 'Process Viewer' option to launch the action.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-21_14-28-19.png?version=1&modificationDate=1537504104735&cacheVersion=1&api=v2&width=300&height=429)

  

### 5 Navigate the Process Viewer

5.1 When the Process Viewer is displayed, all existing Process Definitions for the user will be listed otherwise a <blank> screen will be displayed.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_14-44-38.png?version=1&modificationDate=1537418682612&cacheVersion=1&api=v2&width=300&height=391)

  

5.2 Click on the 'Graphical Process Composer' icon to start the create process. 

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-21_14-46-45.png?version=1&modificationDate=1537505209700&cacheVersion=1&api=v2&width=300&height=391)

  

5.3 Expand the Activity node when the tree structure is displayed.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_15-6-26.png?version=1&modificationDate=1537419990979&cacheVersion=1&api=v2&width=300&height=402)

  

5.4 Expand the VirtualAcvtivity node.

5.4.1 Look for the Report option within this node.

5.4.2 Click on this option and drag it into the space on the right of the double-line to create the report.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_15-11-32.png?version=1&modificationDate=1537420296825&cacheVersion=1&api=v2&width=300&height=378)

  

### 6 Create Report Template

6.1 After dragging the Report option, the Create Report template is displayed.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_15-44-16.png?version=1&modificationDate=1537422261529&cacheVersion=1&api=v2&width=1000&height=492)

  

6.2 Enter inputs as follows.

6.2.1 Name - 

6.2.2 Description - 

6.2.3 Output Type -

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-21_15-43-7.png?version=1&modificationDate=1537508593825&cacheVersion=1&api=v2&width=1000&height=507)

  

6.3 Enter the metrics in the graph or charts format as required in the report template in HTML format.

6.3.1 Sample report template in HTML - the following sample code display the SAP System Availability. Replace the following (highlighted in RED) with the appropriate values from the tenant where the report is being created.

6.3.1.1 `<h1>` : replace with the required report heading

6.3.1.2 href= : replace OBJECT\_Id and itconductor.context values with the corresponding tenant's Availability chart object\_id and context values

6.3.1.3 title : replace with the required report title

6.3.1.4 OBJECT\_Id : same as 6.3.1.2

6.3.1.5 context : same as 6.3.1.2

  

Sample HTML code:

<itc:report xmlns:itc="urn:itconductor">  
```
<h1>??? Service Health and Utilization Report</h1>  
<h2 style="white-space: nowrap;"><a href="[https://service.itconductor.com/thresholdView?OBJECT\_Id=6285545522902332&amp;itconductor.context=6285545521423708](https://service.itconductor.com/thresholdView?OBJECT_Id=6285545522902332&itconductor.context=6285545521423708)" style="white-space: nowrap; text-decoration: none;" title="SAP System GCP">/T-Systems\_ZuelligPharma/Production/SAP Systems/GCP</a></h2>

<!-- Availability -->  
<itc:chart>  
<itc:parameter name="OBJECT\_Id">6285545522902332</itc:parameter>  
<itc:parameter name="context">6285545521423708</itc:parameter>  
<itc:parameter name="title">true</itc:parameter>  
<itc:parameter name="timeScale">HOUR</itc:parameter>  
<itc:parameter name="range">H12</itc:parameter>  
<itc:parameter name="fit">width</itc:parameter>  
</itc:chart>

</itc:report>
```
  

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_15-48-18.png?version=1&modificationDate=1537422504576&cacheVersion=1&api=v2&width=1000&height=538)

  

6.4 When all the required inputs are completed, select the 'Create Report' icon on the top left screen.

6.4.1 A message confirming the successful creation of the report object will be displayed.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-21_16-40-35.png?version=1&modificationDate=1537512044245&cacheVersion=1&api=v2&width=1000&height=511)

  

### 7 Process showing defined Report

The created report will be shown in the Graphical Process Composer in purple. Double-click on the purple rectangle to confirm, if required, and it will display the Report definition in Modify mode.

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-20_15-50-26.png?version=1&modificationDate=1537422630806&cacheVersion=1&api=v2&width=300&height=330)

  

### 8 Display My Reports List

8.1 Navigate back to 'My Objects' on the top menu bar and select 'My Reports from the dropdown list. 

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-25_13-30-36.png?version=1&modificationDate=1537846242442&cacheVersion=1&api=v2&width=300&height=292)

  

8.2 A list of all the reports associated with the login user will be displayed. 

8.2.1 A hierarchy icon denotes that the Report is defined in a Process and can only be run by the ITC Scheduler.

8.2.2 

![](https://itconductor.atlassian.net/wiki/download/thumbnails/597262458/image2018-9-25_13-47-55.png?version=1&modificationDate=1537847281145&cacheVersion=1&api=v2&width=1000&height=135)

  

  

Like[Femi Charles](/people/5af51ee979a85f559261f6cf?ref=confluence&src=profileCard) likes this

No labels

Write a comment…
