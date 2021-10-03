
### What's covered in this lab

This lab shows how you can use **WhiteSource Bolt with Azure DevOps** to automatically detect alerts on vulnerable open source components, outdated libraries, and license compliance issues in your code.

Azure DevOps integration with WhiteSource Bolt will enable you to:

1. Detect and remedy vulnerable open source components.
1. Generate comprehensive open source inventory reports per project or build.
1. Enforce open source license compliance, including dependencies’ licenses.
1. Identify outdated open source libraries with recommendations to update.

### Before you begin

1.Use https://marketplace.visualstudio.com/items?itemName=whitesource.whiteSource-bolt-v2 to provision the WhiteSource project on your Azure DevOps Organization.

## Exercise 1: Activate WhiteSource Bolt

In your Azure DevOps Project, under **Pipelines** section, go to **PartsUnlimitedt** build pipeline and edit it.Add the **whitesource bolt** task and save the yaml file.

![Dev_Essentials](images/whitesource.png)


## Exercise 2: Trigger a build


1. Go to **Pipelines** section under **Pipelines** tab, select the build definition **PartsUnlimited** and click on **Run pipeline** to trigger a build. Click **Run** (leave defaults).

   ![build-def](images/run.png)


1. Navigate to **WhiteSource Bolt Build Report** tab  and wait for the report generation of the completed build to see the vulnerability report.

   ![](images/selectwhitesourcetab.png)
   ![report](images/WhiteSourceBolt13.png)

## Exercise 3: Analyze Reports

WhiteSource bolt automatically detects OpenSource components in the software including transitive dependencies and their respective licenses.

### Security Dashboard

The security dashboard shows the vulnerability of the build.
This report shows the list of all vulnerable open source components with **Vulnerability Score, Vulnerable Libraries, Severity Distribution**.

![Security](images/WhiteSourceBolt30.png)

You can see the opensource license distribution and a detailed view of all components and links to their metadata and licensed references.

### Outdated Libraries

WhiteSource Bolt also tracks outdated libraries in the project, getting all the detailed information and links to newer versions and recommendations.

![outdatedlibraries](images/outdatedlibraries.png)

## Summary

With Azure DevOps and WhiteSource Bolt integration, you can *shift-left* your open source management. The integration allows you to have alerts in real time, on vulnerabilities and other issues to help you take immediate action.
