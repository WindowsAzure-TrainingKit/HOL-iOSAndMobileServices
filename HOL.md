<a name="HOLTop"></a>
# Get started with Windows Azure Mobile Services and iOS #

---

<a name="Overview"></a>
## Overview ##

This tutorial shows you how to add a cloud-based backend service to an iOS app using Windows Azure Mobile Services. In this tutorial, you will create both a new mobile service and a simple _To do list_ app that stores app data in the new mobile service.

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

1. [Create a new mobile service](#Exercise1)

1. [Create a new iOS app](#Exercise2)

1. [Run your new iOS app](#Exercise3)
 
Estimated time to complete this lab: **30 minutes**.

<a name="Exercise1"></a>
### Exercise 1: Create a new mobile service ###

Follow these steps to create a new mobile service.

1. Log into the [Management Portal](https://manage.windowsazure.com/).

1. At the bottom of the navigation pane, click **NEW**.

	![New Button.](./Images/new-button.png?raw=true "New Button")

	_New Button_

1. Expand **Compute** and **Mobile Service**, then click **Create**.

	![New Mobile Services](./images/mobile-services.png?raw=true "New Mobile Services")

	_New Mobile Services_

1. In the **Create a Mobile Service** page, type a subdomain name for the new mobile service in the **URL**textbox and wait for name verification. Once name verification completes, click the right arrow button to go to the next page.

	![Create Mobile Services.](./images/create-mobile-services.png?raw=true "Create Mobile Services.")

	_Create Mobile Services_

	This displays the **Specify database settings** page.
 
	> **Note:** As part of this tutorial, you create a new SQL Database instance and server. You can reuse this new database and administer it as you would any other SQL Database instance. If you already have a database in the same region as the new mobile service, you can instead choose Use existing Database and then select that database. The use of a database in a different region is not recommended because of additional bandwidth costs and higher latencies. 

1. In **Name**, type the name of the new database, then type **Login name**, which is the administrator login name for the new SQL Database server, type and confirm the password, and click the check button to complete the process.

	![This displays the Specify database settings page.](./images/specify-databse-settings.png?raw=true "This displays the Specify database settings page.")

	_Specify database settings page_

	> **Note:** When the password that you supply does not meet the minimum requirements or when there is a mismatch, a warning is displayed. 

1. Take note of the administrator login name and password that you specify and finish the wizard. You have now created a new mobile service that can be used by your mobile apps.

<a name="Exercise2"></a>
### Exercise 2: Create a new iOS app ###

Once you have created your mobile service, you can follow an easy quickstart in the Management Portal to either create a new app or modify an existing app to connect to your mobile service.
In this section you will create a new iOS app that is connected to your mobile service.

1. In the Management Portal, click **Mobile Services**, and then click the mobile service that you just created.

1. In the quickstart tab, click **iOS** under **Choose platform** and expand **Create a new iOS app**.

	![Getting Started Mobile Services](./images/get-started-mobile-services.png?raw=true"Getting Started Mobile Services")

	_Getting Started Mobile Services_

	> **Note:** This displays the three easy steps to create an iOS app connected to your mobile service.

1. If you haven't already installed [Xcode](https://go.microsoft.com/fwLink/p/?LinkID=266532), click **Install Xcode** and perform the installation process.

1. Click **Create TodoItems table** to create a table to store app data.

	![Create a new iOS app](./images/create-a-new-os-app.png?raw=true "Crate a new iOS app")

	_Create TodoItem Table_

1. Under **Download and run app**, click **Download**.

	> **Note** This downloads the project for the sample _To do list_ application that is connected to your mobile service, along with the Mobile Services iOS SDK. Save the compressed project file to your local computer, and make a note of where you saved it.

<a name="Exercise3"></a>
### Exercise 3: Run your new iOS app ###

The final stage of this tutorial is to build and run your new app.

1. Browse to the location where you saved the compressed project files, expand the files on your computer, and open the project file using Xcode.

	![Project with Xcode](./images/project-file-with-xcode.png?raw=true "Project with Xcode")

	_TODO Xcode solution_

1. Press the **Run** button to build the project and start the app in the iPhone emulator, which is the default for this project.

1. In the app, type meaningful text, such as _Complete the tutorial_ and then click the plus (**+**) icon.

	![IPhone App](./images/iphone-todo-app.png?raw=true "IPhone App")
 
	_TODO app running in IPhone_

	> **Note:** You can review the code that accesses your mobile service to query and insert data, which is found in the TodoService.m file.

1. Back in the Management Portal, click the **Data** tab and then click the **TodoItems** table.

	![Todolist data](./images/todolist-data.png?raw=true "Todolist data")
 
	_TODO data items_

	> **Note:** This lets you browse the data inserted by the app into the table.

	![Todolist data details](./images/todolist-data-details.png?raw=true "Todolist data details")

	_TODO data list_

---

<a name="Summary" />
##Summary##
By completing this Hands-on Lab you have learned how to:

 - 
