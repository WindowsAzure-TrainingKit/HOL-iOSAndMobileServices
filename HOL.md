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

* [XCode 4.5](https://go.microsoft.com/fwLink/p/?LinkID=266532)
* An iOS 5.0 (or later version) capable device
* Windows Azure account that has the Windows Azure Mobile Services feature enabled. [Windows Azure Free Trial](http://www.windowsazure.com/en-us/pricing/free-trial/?WT.mc_id=AE564AB28&returnurl=http%3A%2F%2Fwww.windowsazure.com%2Fen-us%2Fdevelop%2Fmobile%2Ftutorials%2Fget-started-ios%2F).
* iOS Developer Program membership


---

<a name="Exercises"></a>
## Exercises ##

This hands-on lab includes the following exercises:

1. [Building your first Windows Azure Application](#Exercise1)
1. [Validate and Modify Data Using Server Scripts](#Exercise2)
1. [Get Started with Push Notifications](#Exercise3)
1. [Get Started with Auth](#Exercise4)


Estimated time to complete this lab: **30 minutes**.

<a name="Exercise1"></a>
### Exercise 1: Building your first Windows Azure App ###

This exersice shows you how to add a cloud-based backend service to an iOS app using Windows Azure Mobile Services.

### Task 1: Create a new mobile service ###
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

1. If you haven't already installed [XCode](https://go.microsoft.com/fwLink/p/?LinkID=266532), click **Install XCode** and perform the installation process.

1. Click **Create TodoItems table** to create a table to store app data.

	![Create TodoItem Table](./Images/create-todo-items-table.png?raw=true "Crate a new iOS app")

	_Create TodoItem Table_

1. Under **Download and run app**, click **Download**.

	![Download Source Code](./Images/download-source code.png?raw=true "Crate a new iOS app")

	_Download source code_

	> **Note** This downloads the project for the sample _To do list_ application that is connected to your mobile service, along with the Mobile Services iOS SDK. Save the compressed project file to your local computer, and make a note of where you saved it.

#### Task 3: Hosting and Running Your iOS App ####

1. Browse to the location where you saved the compressed project files, expand the files on your computer, and open the project file using XCode.

	![Project with XCode](./images/project-file-with-xcode.png?raw=true "Project with XCode")

	_Todolist XCode solution_

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

1. Swipe in _Sign-up for the free trial_ tasks to show the **Complete** button

1. Complete the task

	![Swipe to show complete button](./Images/swipe-to-show-complete-button.png?raw=true "Swipe to show complete button")

	_Swipe to show complete button_

1. Perform the same operation with task _Create the Mobile Service_

1. Do not mark the _Complete the Hands-On Lab_ task as **Complete**

	![Todolist app running in IPad simulator](./Images/todolist-app-running-in-ipad-simulator.png?raw=true "Todolist app running in IPad simulator")

	_Todolist app running in IPad simulator_

	>**Note**: You will see that the tasks disappear when they are complete.

1. Stop the application running in the IPad Simulator

1. Back in the Windows Azure Management Portal, click the **Data** tab and then click the **TodoItems** table.

1. Check how _Sign-up for the free trial_ and Create the Mobile Service tasks have the **complete** flag as **true** while _Complete the Hands-On Lab_ task is **false**

	![Todolist data details](./Images/todolist-data-details2.png?raw=true "Todolist data details")

	_Todolist updated data_


### Task 4: Exploring your App Code ###

In this step we will explore To do list application code and see how simple the Windows Azure Mobile Services Client SDK makes it to interact with Windows Azure Mobile Services.

1. Switch back to the XCode editor.

1. In solution explorer expand the references folder and see the Windows Azure Mobile Services Client SDK reference.

	![Windows Azure Mobile Services SDK](./Images/windows-sdk.png?raw=true"Windows Azure Mobile Services SDK")

	_Windows Azure Mobile Services SDK_

1. Open **QSTodoService.m** and show the MSClient class. This is the key class provided by the client SDK that provides a way for your application to interact with Windows Azure Mobile Services. The first parameter in the constructor is the Mobile Service endpoint and the second parameter is the Application Key for your Mobile Service.

	![Application Key and endpoint](./Images/application-key-and-endpoint.png?raw=true"Application Key and endpoint")

	_Application Key and endpoint_

1. Below thee definition of the MSClient class, we can see the configuration of the table name we created in the previous task.

	![Table name configuration](./Images/table-name-configuration.png?raw=true"Table name configuration")

	_Table name configuration_

1. Scroll down in the same file. You will see the **addItem** method and the **completeItem** method.

	![Add item and Complete item methods](./Images/additemandcompleteitem-methods.png?raw=true"Add item and Complete item methods")

	_Add item and Complete item methods_

	>**Note:** To add additional columns to the table, simply send an insert request including the new properties from your app with dynamic schema enabled. Once a column is created, its data type cannot be changed by Mobile Services. Insert or update operations fail when the type of a property in the JSON object cannot be converted to the type of the equivalent column in the table.


---
<a name="Exercise2"></a>
### Exercise 2: Validate and Modify Data Using Server Scripts ###

In this exercise, you will download an app that stores data in memory, create a new mobile service, integrate the mobile service with the app, and then login to the Windows Azure Management Portal to view changes to data made when running the app.

### Task 1: Add validation###

It is always a good practice to validate the length of data that is submitted by users. First, you register a script that validates the length of string data sent to the mobile service and rejects strings that are too long, in this case longer than 10 characters.

1.	Log into the [Windows Azure Management Portal](https://manage.windowsazure.com/), click **Mobile Services** and then click your Mobile Service.

	![Mobile Service](./Images/mobile-service.png?raw=true "Mobile Service")

	_Mobile Services_


1.	Click the **Data** tab, then click the **TodoItem** table.

1. Click **Script**, then select the **Insert** operation

	![Insert operation in script tab](images/insert-operation-in-script-tab.png?raw=true "Insert operation in script tab")

	_Insert operation in script tab_

1.	Replace the existing script with the following function, and then click **Save**.

	````objective-c
	function insert(item, user, request) {
	    if (item.text.length > 10) {
	        request.respond(statusCodes.BAD_REQUEST, 'Text length must be 10 characters or less.');
	    } else {
	        request.execute();
	    }
	}
	````

	> **NOTE**You can remove a registered script on the Script tab by clicking Clear and then Save.
	> 
	>This script checks the length of the **text** property and sends an error response when the length exceeds 10 characters. Otherwise, the **execute** method is called to complete the insert.

### Task 2: Update the client ###

Now that the mobile service is validating data and sending error responses, you need to update your app to be able to handle error responses from validation.

1.	Switch back to XCode.

1.	Press the **Run** button (**Command** + **R**) to build the project and start the app, then type text longer than 10 characters in the textbox and click the plus (**+**) icon.

	>**Note**: Notice that the app raises an unhandled error as a result of the 400 response (Bad Request) returned by the mobile service.

1.	In the QSTodoService.m file, locate the following line of code in the **addItem** method:

	````objective-c
	[self logErrorIfNotNil:error];
	````
After this line of code, replace the remainder of the block with the following code:

	````objective-c
	BOOL goodRequest = !((error) && (error.code == MSErrorMessageErrorCode));

	// detect text validation error from service.
	if (goodRequest) // The service responded appropriately
	{
		 NSUInteger index = [items count];
		 [(NSMutableArray *)items insertObject:result atIndex:index];
		// Let the caller know that we finished
		completion(index);
	}
	else{
		// if there's an error that came from the service
		// log it, and popup up the returned string.
		if (error && error.code == MSErrorMessageErrorCode) {
			 NSLog(@"ERROR %@", error);
			 UIAlertView *av =
			 [[UIAlertView alloc]
			  initWithTitle:@"Request Failed"
			  message:error.localizedDescription
			  delegate:nil
			  cancelButtonTitle:@"OK"
			  otherButtonTitles:nil
			  ];
			 [av show];
		}
	}
	````

	
	>**Note**: This logs the error to the output window and displays it to the user.

1.	Rebuild and start the app.

1. Enter a text with more than 10 characters (e.g. _A user-specific task_.).

	![Validation Error](images/validation-error.png?raw=true "Validation Error")

	_Validation Error_

	>**Note**: Notice that error is handled and the error messaged is displayed to the user.

---
<a name="Exercise3"></a>
### Exercise 3: Get Started with Push Notifications ###

### Task 1: Generate the Certificate Signing Request file###

First you must generate the Certificate Signing Request (CSR) file, which is used by Apple to generate a signed certificate.

1.	From the Utilities folder, run the Keychain Access tool.

1.	Click **Keychain Access**, expand **Certificate Assistant**, then click **Request a Certificate from a Certificate Authority...**.

	![Request Certificate authority](images/request-certificate-authority.png?raw=true "Request Certificate authority")

	_Request Certificate from Certificate authority_

1.	Select your **User Email Address**, type **Common Name** and **CA Email Address** values, make sure that **Saved to disk** is selected, and then click **Continue**.

	![Certificcate assistant](images/certificcate-assistant.png?raw=true "Certificcate assistant")

	_Certificcate assistant_

1.	Type a name for the Certificate Signing Request (CSR) file in **Save As**, select the location in **Where**, then click **Save**.

	![Save window](images/save-window.png?raw=true "Save window")

	_Save Certificate Window_

This saves the CSR file in the selected location; the default location is in the Desktop. Remember the location chosen for this file.

### Task 2: Register your app for push notifications###

To be able to send push notifications to an iOS app from mobile services, you must register your application with Apple and also register for push notifications.

1.	If you have not already registered your app, navigate to the [iOS Provisioning Portal ](http://go.microsoft.com/fwlink/p/?linkid=272456&clcid=0x409) at the Apple Developer Center, log on with your Apple ID.

1. Click **App IDs**, then click **New App ID**.

	![App IDs](images/app-ids.png?raw=true "App IDs")

	_App IDs_

1.	Type a name for your app in **Description**, enter the value _MobileServices.Quickstart_ in **Bundle Identifier**, then click **Submit**.
This generates your app ID.

	![Create App Id](images/create-app-id.png?raw=true "Create App Id")

	_Create App Id_

	>**NOTE**: If you choose to supply a Bundle Identifier value other thanMobileServices.Quickstart, you must also update the bundle identifier value in your Xcode project.

1.	Locate the app ID that you just created, then click **Configure**.

	![Configuration](images/configuration.png?raw=true "Configuration")

	_Configuration_

1.	Check the **Enable for Apple Push Notification service** check box, then click the **Continue** button for the **Development Push SSL Certificate**.
This displays the Apple Push Notification service SSL Certificate Assistant.

	![Mobile Service Quickstart](images/mobile-service-quickstart.png?raw=true "Mobile Service Quickstart")

	_Mobile Service Quickstart_

	>**NOTE**: This tutorial uses a development certificate. The same process is used when registering a production certificate. Just make sure that you set the same certificate type when you upload the certificate to Mobile Services.

1.	Click **Browse**, browse to the location where you saved the CSR file that you created in the first task, then click **Generate**.

	![Submit certificate request](images/submit-certificate-request.png?raw=true "Submit certificate request")

	_Submit certificate request_

1.	After the certificate is created by the portal, click **Continue** and on the next screen click **Download**. 

	This downloads the signing certificate and saves it to your computer in your Downloads folder.

	![Cer file](images/cer-file.png?raw=true "Cer file")

	_Cer file_

	> **NOTE**: By default, the downloaded file a development certificate is named aps_development.cer.

1.	Double-click the downloaded push certificate **aps_development.cer**.
This installs the new certificate in the Keychain, as shown below:

	![Certificate](images/certificate.png?raw=true "Certificate")

	_Certificate_

	>**NOTE**: The name in your certificate might be different, but it will be prefixed with Apple Development iOS Push Notification Services:.

Later, you will use this certificate to generate a .p12 file and upload it to Mobile Services to enable authentication with APNS.

### Task 3: Create a provisioning profile for the app###

1.	Back in the [iOS Provisioning Portal]( http://go.microsoft.com/fwlink/p/?linkid=272456&clcid=0x409), select **Provisioning**, then click **New Profile**.

	![New Profile](images/new-profile.png?raw=true "New Profile")

	_New Profile_

1.	Enter a **Profile Name**, select the **Certificates** and **Devices** to use for testing, select the **App ID**, then click **Submit**.
This creates a new provisioning profile.

	![Create iOS development provisioning profile](images/create-ios-development-provisioning-profile.png?raw=true "Create iOS development provisioning profile")

	_Create iOS development provisioning profile_

1.	From the list of provisioning profiles, click the **Download** button for this new profile.

	This downloads the profile to the local computer.

	![Download button](images/download-button.png?raw=true "Download button")

	_Download button_

	> **NOTE**: You may need to refresh the page to see the new profile.

1.	In Xcode, open the Organizer select the Devices view, select **Provisioning Profiles** in the **Library** section in the left pane, and then click the **Import** button at the very bottom of the middle pane.

	![Import](images/import.png?raw=true "Import")

	_Import button_

1.	Locate the downloaded provisioning profile and click **Open**.

	![Open profile](images/open-profile.png?raw=true "Open profile")

	_Open profile_

1.	Under **Targets**, click **Quickstart**, expand **Code Signing Identity**, then under **Debug** select the new profile.

	![Debug the selected profile](images/debug-the-selected-profile.png?raw=true "Debug the selected profile")

	_Debug the selected profile_

	This ensures that the Xcode project uses the new profile for code signing. Next, you must upload the certificate to Mobile Services.

### Task 4: Configure Mobile Services to send push requests###

After you have registered your app with APNS and configured your project, you must next configure your mobile service to integrate with APNS.

1.	In Keychain Access, right-click the new certificate, click **Export**, name your file QuickstartPusher, select the**.p12** format, then click **Save**.
Make a note of the file name and location of the exported certificate.

	![Save p12](images/save-p12.png?raw=true "Save p12")

	_Save p12_

	>**NOTE**: This tutorial creates a QuickstartPusher.p12 file. Your file name and location might be different.

1.	Log on to the [Windows Azure Management Portal](https://manage.windowsazure.com/), click **Mobile Services**, and then click your app.

1.	Click the **Push** tab and click **Upload**.

	![Upload certificate](images/upload-certificate.png?raw=true "Upload certificate")

	_Upload certificate_

	This displays the Upload Certificate dialog.

1.	Click **File**, select the exported certificate QuickstartPusher.p12 file, enter the **Password**, make sure that the correct **Mode** is selected, click the check icon, then click **Save**.

	![Upload certificate dialog](images/upload-certificate-dialog.png?raw=true "Upload certificate dialog")

	_Upload certificate dialog_

	>**NOTE**: This lab uses developement certificates.

	Both your mobile service is now configured to work with APNS.
	
### Task 5: Add push notifications to your App###

1.	In Xcode, open the QSAppDelegate.h file and add the following property below the ***window** property:


	````objective-c
	@property (strong, nonatomic) NSString *deviceToken;
	````

	>**NOTE**: When dynamic schema is enabled on your mobile service, a new 'deviceToken' column is automatically added to the TodoItem table when a new item that contains this property is inserted.

1.	In QSAppDelegate.m, replace the following handler method inside the implementation:

	````objective-c
	-(BOOL)application:(UIApplication *)application 
	didFinishLaunchingWithOptions:
	(NSDictionary *)launchOptions
	{
		 // Register for remote notifications
		 [[UIApplication sharedApplication] registerForRemoteNotificationTypes:
		 UIRemoteNotificationTypeAlert | UIRemoteNotificationTypeBadge | UIRemoteNotificationTypeSound];
		 return YES;
	}
	````

1.	In QSAppDelegate.m, add the following handler method inside the implementation:

	````objective-c
	// We are registered, so now store the device token (as a string) on the AppDelegate instance
	// taking care to remove the angle brackets first.
	-(void)application:(UIApplication *)application didRegisterForRemoteNotificationsWithDeviceToken:
	(NSData *)deviceToken {
		 NSCharacterSet *angleBrackets = [NSCharacterSet characterSetWithCharactersInString:@"<>"];
		 self.deviceToken = [[deviceToken description] stringByTrimmingCharactersInSet:angleBrackets];
	}
	````

1.	In QSAppDelegate.m, add the following handler method inside the implementation:

	````objective-c
	// Handle any failure to register. In this case we set the deviceToken to an empty
	// string to prevent the insert from failing.
	-(void)application:(UIApplication *)application didFailToRegisterForRemoteNotificationsWithError:
	(NSError *)error {
		 NSLog(@"Failed to register for remote notifications: %@", error);
		 self.deviceToken = @"";
	}
	````

1.	In QSAppDelegate.m, add the following handler method inside the implementation:

	````objective-c
	// Because toast alerts don't work when the app is running, the app handles them.
	// This uses the userInfo in the payload to display a UIAlertView.
	-(void)application:(UIApplication *)application didReceiveRemoteNotification:
	(NSDictionary *)userInfo {
		 NSLog(@"%@", userInfo);
		 UIAlertView *alert = [[UIAlertView alloc] initWithTitle:@"Notification" message:
		 [userInfo objectForKey:@"inAppMessage"] delegate:nil cancelButtonTitle:
		 @"OK" otherButtonTitles:nil, nil];
		 [alert show];
	}
	````

1.	In QSTodoListViewController.m, import the QSAppDelegate.h file so that you can use the delegate to obtain the device token:

	````objective-c
	#import "QSAppDelegate.h"
	````

1.	In QSTodoListViewController.m, modify the **(IBAction)onAdd** action by locating the following line:

	````objective-c
	NSDictionary *item = @{ @"text" : itemText.text, @"complete" : @(NO) };
	````

	Replace this with the following code:

	````objective-c
	// Get a reference to the AppDelegate to easily retrieve the deviceToken
	QSAppDelegate *delegate = [[UIApplication sharedApplication] delegate];


	NSDictionary *item = @{
		 @"text" : itemText.text,
		 @"complete" : @(NO),
		 // add the device token property to our todo item payload
		 @"deviceToken" : delegate.deviceToken
	};
	````

	This adds a reference to the **QSAppDelegate** to obtain the device token and then modifies the request payload to include that device token.

	>**NOTE**You must add this code before to the call to the addItem method.

	>Your app is now updated to support push notifications.

###Task 6: Update the registered insert script in the Management Portal###

1.	In the Windows Azure Management Portal, click the **Data** tab and then click the **TodoItem** table.


	![Todolist data](./images/todolist-data.png?raw=true "Todolist data")
 
	_Todolist data items_	

1.	In **todoitem**, click the **Script** tab and select **Insert**.

	![Insert operation in script tab](images/insert-operation-in-script-tab2.png?raw=true "Insert operation in script tab")

	_Insert operation in script tab_

	This displays the function that is invoked when an insert occurs in the **TodoItem** table.

1.	Replace the insert function with the following code, and then click **Save**:

	````objective-c
	function insert(item, user, request) {
		 request.execute();
		 // Set timeout to delay the notification, to provide time for the 
		 // app to be closed on the device to demonstrate toast notifications
		 setTimeout(function() {
			  push.apns.send(item.deviceToken, {
					alert: "Toast: " + item.text,
					payload: {
						 inAppMessage: "Hey, a new item arrived: '" + item.text + "'"
					}
			  });
		 }, 2500);
	}
	````

	This registers a new insert script, which uses the apns object <http://go.microsoft.com/fwlink/p/?linkid=272333&clcid=0x409> to send a push notification (the inserted text) to the device provided in the insert request.

	>**NOTE**: This script delays sending the notification to give you time to close the app to receive a toast notification.


### Task 7: Test push notifications in your app###

1.	Press the **Run** button to build the project and start the app in an iOS capable device, then click **OK** to accept push notifications

	![Prompt to send push notification](images/prompt-to-send-push-notification.png?raw=true "Prompt to send push notification")

	_Prompt to send push notification_

	>**NOTE**: You must explicitly accept push notifications from your app. This request only occurs the first time that the app runs.

1.	In the app, type meaningful text, such as _A new Mobile Services task_ and then click the plus (**+**) icon.

	![New task](images/new-task.png?raw=true "New task")

	_New task_

1.	Verify that a notification is received, then click **OK** to dismiss the notification.

	![Notification received](images/notification-received.png?raw=true "Notification received")

	_Notification received_

1.	Repeat step 2 and immediately close the app, then verify that the following toast is shown.

	![Notification Received](images/notification-recieved2.png?raw=true "Notification Received")

	_Notification Received_

---
<a name="Exercise4"></a>
### Exercise 4: Get Started with Auth ###

This exersice shows you how to add facebook authentication to the Application.

### Task 1: Register your app ###

To be able to authenticate users, you must register your iOS app at the Facebook Developer Center.

1. Navigate to the Facebook Developer Center page, log on with your Facebook account if needed, and then follow the instructions to create your app.

1. For the Callback URL enter the URL of your Mobile Service. This can be found on the **Dashboard** tab in the portal under **Mobile Service URL** on the right side.

1. Log on to the [Windows Azure Management Portal](https://manage.windowsazure.com/), click **Mobile Services**, and then click your Mobile Service.

	![Mobile Service](./Images/mobile-service.png?raw=true "Mobile Service")

	_Mobile Services_

1. Click the **Dashboard** tab and make a note of the **Site URL** value

	![Todolist dashboard](./Images/todolist-dashboard.png?raw=true "Todolist dashboard")

	_Todolist dashboard_

1. Click the **Identity** tab, enter the **App ID** and the **App Secret** obtained in the Facebook developer center, and click **Save**.

	![Todolist Identity tab](images/todolist-identity-tab.png?raw=true "Todolist Identity tab")

	_Todolist Identity tab_


### Task 2: Restrict permissions to authenticated users ###

1.	In the Management Portal, click the **Data** tab, and then click the **TodoItem** table.

	![Todolist data](./Images/todolist-data.png?raw=true "Todolist data")
 
	_Todolist data items_

1.	Click the **Permissions** tab, set all permissions to **Only authenticated users**, and then click **Save**. 

	>**Note**: This will ensure that all operations against the **TodoItem** table require an authenticated user. This also simplifies the scripts in the next tutorial because they will not have to allow for the possibility of anonymous users.

	![Setting table permissions](./Images/setting-table-permissions.png?raw=true "Setting table permissions")

	_Setting table permissions_

1.	Switch back to XCode where we left in exercise 1.

2.	Press the **Run** button to build the project and start the app in the iPhone emulator; verify that an unhandled exception with a status code of 401 (Unauthorized) is raised after the app starts.

	>**Note**: This happens because the app attempts to access Mobile Services as an unauthenticated user, but the_TodoItem_ table now requires authentication.
Next, you will update the app to authenticate users before requesting resources from the mobile service.

### Task 3: Add authentication to the app ###

1.	Open the project file **QSTodoListViewController.m** and in the **viewDidLoad** method, remove the following code that reloads the data into the table:

	````objective-c
	[self refresh];
	````

1. Just after the **viewDidLoad** method, add the following code:

	````objective-c
	-(void)viewDidAppear:(BOOL)animated
	{
		 MSClient *client = self.todoService.client;


		if (client.currentUser != nil) {
			return;
		}
		
		[client loginWithProvider:@"facebook" controller:self animated:YES completion:^(MSUser *user, NSError *error) {
			 [self refresh];
		}];
	}
	````

	>**NOTE:** If you are using an identity provider other than Facebook, change the value passed tologinWithProvider above to one of the following:microsoftaccount,facebook,twitter, orgoogle.

1.	Press the **Run** button to build the project, start the app in the iPhone emulator

	![Facebook authentication](images/facebook-authentication.png?raw=true "Facebook authentication")

	_Facebook authentication_

1. Log-on with Facebook (or your chosen identity provider) and accept Facebook to use your public profile. When you are successfully logged-in, the app should run without errors, and you should be able to query Mobile Services and make updates to data.



---

<a name="Summary" />
##Summary##
By completing this Hands-on Lab you have learned how to:

 - 
