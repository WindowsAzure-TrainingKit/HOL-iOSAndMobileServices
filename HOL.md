<a name="HOLTop"></a>
# Get started with Windows Azure Mobile Services and iOS #

---

<a name="Overview"></a>
## Overview ##

Windows Azure Mobile Services is a Windows Azure service offering designed to make it easy to create highly-functional mobile apps using Windows Azure. Mobile Services brings together a set of Windows Azure services that enable backend capabilities for your apps. These capabilities includes simple provisioning and management of tables for storing app data, integration with notification services, integration with well-known identity providers for authentication, among others. In this lab, you will create a new mobile service and a simple _To do list_ app that stores app data in the new mobile service.

<a name="Objectives"></a>
### Objectives ###

In this hands-on lab, you will learn how to:

- 

<a name="Prerequisites"></a>
### Prerequisites ###

Completing this tutorial requires:

* XCode 4.5 
* iOS 5.0 or later versions.
* Windows Azure account that has the Windows Azure Mobile Services feature enabled. [Windows Azure Free Trial](http://www.windowsazure.com/en-us/pricing/free-trial/?WT.mc_id=AE564AB28&returnurl=http%3A%2F%2Fwww.windowsazure.com%2Fen-us%2Fdevelop%2Fmobile%2Ftutorials%2Fget-started-ios%2F).

---

<a name="Exercises"></a>
## Exercises ##

This hands-on lab includes the following exercises:

1. [Building your first Windows Azure Application](#Exercise1)

Estimated time to complete this lab: **30 minutes**.

<a name="Exercise1"></a>
### Exercise 1: Building your first Windows Azure App ###

This exersice shows you how to add a cloud-based backend service to an iOS app using Windows Azure Mobile Services.

### Task 1- Create a new mobile service ###
Follow these steps to create a new mobile service.

1. Log into the [Windows Azure Management Portal](https://manage.windowsazure.com) and navigate to Mobile Services

1. At the bottom of the navigation pane, click **+NEW**.

	![New Button](./Images/new-button.png?raw=true)

	_New Button_

1. Expand **Compute | Mobile Service**, then click **Create**.
 
	![Creating a New Mobile Service](./Images/creating-new-mobile-service.png?raw=true)
 
	_Creating a New Mobile Service_

	This displays the **New Mobile Service** dialog.

1. In the **Create a mobile service** page, type a subdomain name for the new mobile service in the **URL** textbox and wait for name verification. Once name verification completes, click the right arrow button to go to the next page.
 
	![New Mobile Service](./Images/create-mobile-service-step-1.png?raw=true)

	_New Mobile Service_

	This displays the **Specify database settings** page.

	> **Note:** As part of this tutorial, you create a new SQL Database instance and server. You can reuse this new database and administer it as you would any other SQL Database instance. If you already have a database in the same region as the new mobile service, you can instead chooseUse existing Databaseand then select that database. The use of a database in a different region is not recommended because of additional bandwidth costs and higher latencies.

1. In **Name**, type the name of the new database, then type **Login name**, which is the administrator login name for the new SQL Database server, type and confirm the password, and click the check button to complete the process.
 
	![Specifying Database Settings](./Images/create-mobile-service-step-2.png?raw=true)

	_Specifying Database Settings_

	> **Note:**  When the password that you supply does not meet the minimum requirements or when there is a mismatch, a warning is displayed.  We recommend that you make a note of the administrator login name and password that you specify; you will need this information to reuse the SQL Database instance or the server in the future. You have now created a new mobile service that can be used by your mobile apps.

You have now created a new mobile service that can be used by your mobile apps.

### Task 2: Create a New iOS App ###

Once you have created your mobile service, you can follow an easy quickstart in the Management Portal to either create a new app or modify an existing app to connect to your mobile service.
In this section you will create a new iOS app that is connected to your mobile service.

1. In the Management Portal, click **Mobile Services**, and then click the mobile service that you just created.

1. In the quickstart tab, click **iOS** under **Choose platform** and expand **Create a new iOS app**.

	![Getting Started Mobile Services](./Images/get-started-mobile-services.png?raw=true"Getting Started Mobile Services")

	_Getting Started Mobile Services_

	> **Note:** This displays the three easy steps to create an iOS app connected to your mobile service.

1. If you haven't already installed [Xcode](https://go.microsoft.com/fwLink/p/?LinkID=266532), click **Install Xcode** and perform the installation process.

1. Click **Create TodoItems table** to create a table to store app data.

	![Create TodoItem Table](./Images/create-todo-items-table.png?raw=true "Crate a new iOS app")

	_Create TodoItem Table_

1. Under **Download and run app**, click **Download**.

	![Download Source Code](./Images/download-source code.png?raw=true "Crate a new iOS app")

	_Download source code_

	> **Note** This downloads the project for the sample _To do list_ application that is connected to your mobile service, along with the Mobile Services iOS SDK. Save the compressed project file to your local computer, and make a note of where you saved it.

#### Task 3: Hosting and Running Your iOS App ####

1. Browse to the location where you saved the compressed project files, expand the files on your computer, and open the project file using Xcode.

	![Project with Xcode](./images/project-file-with-xcode.png?raw=true "Project with Xcode")

	_Todolist Xcode solution_

1. Make sure the Iphone Simulator is selected and press the **Run** button to build the project and start the app.

	![Run the application](./images/first-run.png?raw=true "Run the application")

	_Run the application_

1. In the app, type meaningful text, such as _Sign-Up for a free trial_ and then click the plus (**+**) icon.

1. Add two more tasks:
	* _Create the Mobile Service_
	* _Complete the Hands-On Lab_

	![IPhone App](./images/iphone-todo-app.png?raw=true "IPhone App")
 
	_Todolist app running in IPhone Simulator_

	> **Note:** You can review the code that accesses your mobile service to query and insert data, which is found in the TodoService.m file.

1. Stop the application running in the IPhone Simulator

1. Back in the Windows Azure Management Portal, click the **Data** tab and then click the **TodoItems** table.

	![Todolist data](./images/todolist-data.png?raw=true "Todolist data")
 
	_Todolist data items_

	> **Note:** This lets you browse the data inserted by the app into the table.

	![Todolist data details](./Images/todolist-data-details.png?raw=true "Todolist data details")

	_Todolist inserted data_

1. Switch back to the XCode editor

1. Change the **Scheme** to use IPad Simulator and **Run** the application.

1. Swipe in the first two tasks to show the **Complete** button

	![Swipe to show complete button](./Images/swipe-to-show-complete-button.png?raw=true "Swipe to show complete button")

	_Swipe to show complete button_

1. Do not mark the last task as **Complete**

	![Todolist app running in IPad simulator](./Images/todolist-app-running-in-ipad-simulator.png?raw=true "Todolist app running in IPad simulator")

	_Todolist app running in IPad simulator_

	>**Note**: You will see that the tasks disappear when they are complete.

1. Stop the application running in the IPad Simulator

1. Back in the Windows Azure Management Portal, click the **Data** tab and then click the **TodoItems** table.

1. Check how the first two task have the completed flag as **true** while the third one is **flag**

	![Todolist data details](./Images/todolist-data-details2.png?raw=true "Todolist data details")

	_Todolist updated data_


### Task 4: Exploring your App Code ###



---

<a name="Summary" />
##Summary##
By completing this Hands-on Lab you have learned how to:

 - 
