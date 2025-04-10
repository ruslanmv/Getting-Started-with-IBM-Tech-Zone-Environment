# Getting Started with IBM Tech Zone Environment for watsonx.ai

This guide will walk you through the steps to set up your watsonx.ai environment using IBM Tech Zone, retrieve necessary credentials, and troubleshoot a common error.

## 1. Accessing Your Watsonx.ai Environment on IBM Tech Zone

IBM Tech Zone provides pre-configured environments for you to explore and experiment with IBM technologies, including watsonx.ai. The first step is to access your reserved environment.

There are two main types of watsonx.ai environments you might encounter on Tech Zone:

* **IBM ID watsonx SaaS environments:** These environments are accessed using your regular IBM ID.
* **Student ID watsonx SaaS environments:** These environments provide a dedicated login page and credentials provided by Tech Zone.

Follow the instructions below based on the type of environment you have reserved. You can usually identify the type by the title or description of the reservation on the Tech Zone platform.

### 1.1. Accessing IBM ID watsonx SaaS Environments

1.  **Locate your reservation:** Once your reservation is provisioned, navigate to the reservation details page on IBM Tech Zone.
2.  **Access IBM Cloud:** You will typically find a link to access IBM Cloud associated with your reservation. Click on this link.
3.  **Accept the Invitation (if applicable):** If you are a new user to the account associated with the reservation, you might receive an email invitation or a notification in the IBM Cloud console (bell icon in the top right). Make sure to accept the invitation to join the account. Refer to the "[Why can't I access IBM Cloud?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-cant-i-access-ibm-cloud)" section of the original document for detailed instructions.
4.  **Navigate to watsonx.ai:** Once logged into IBM Cloud, search for "watsonx.ai" in the catalog or navigate through the services to find it.
5.  **Launch watsonx.ai:** Click on the watsonx.ai service. You might see a "Get Started" button initially. If you do, follow the steps in "[I can't open watsonx.ai ('Get Started' button instead of 'Launch')](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#i-cant-open-watsonxai-get-started-button-instead-of-launch)" to resolve this and access the watsonx.ai platform.

### 1.2. Accessing Student ID watsonx SaaS Environments

1.  **Identify Student ID Environment:** Ensure your reservation has the "_Student ID_" tag in the title and the description indicates it does not use a regular IBM ID login.
2.  **Locate Login Credentials:** On your reservation details page, you will find a specific login link and credentials (username and password).
3.  **Open Login Link:** Open the provided access link in a private browser tab or ensure you are logged out of any personal IBM Cloud accounts.
4.  **Enter Credentials:** Use the username and password provided in the reservation details to log in.
5.  **Navigate to watsonx.ai:** Once logged in, navigate to the resource list and find the "watson studio" instance. Select the instance and click "Launch in watsonx". You might encounter a form initially; wait for it to disappear and click "continue". Refer to "[How to get to the watsonx.ai platform via Student ID?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-get-to-the-watsonxai-platform-via-student-id)" for more details.

## 2. Setting Up Your Watsonx.ai Environment

Once you have access to the watsonx.ai platform, you'll need to create a project to start working.

### 2.1. Creating a Project

1.  **Open the Menu:** On the IBM watsonx home, at the top left of the screen, select the menu button.
    ![watson-menu](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-menu.png)
2.  **View All Projects:** In the sidebar menu, select the "View all projects" option.
    ![sidebar-menu-options](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-sidebar-menu-options.png)
3.  **Create New Project:** On the right side of the Projects page, click the "New project" button.
    ![new-project](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-new-project.png)
4.  **Select Project Type:** Choose the desired project creation option.
    ![project-options](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-project-options.png)
5.  **Enter Project Details:** Fill in the "Name" field for your project. You can also add an optional "Description". Click the "Create project" button at the bottom right.
    ![project-details](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-project-details.png)
6.  **Project Created:** Your watsonx.ai project should now be successfully created.

### 2.2. Associating Services (If Necessary)

In some cases, you might need to associate services like Watson Machine Learning (WML) or Cloud Object Storage (COS) with your project. This is often done automatically in Tech Zone environments, but if you encounter issues, refer to "[Why can't I create a project on SaaS or associate my service in the project?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-cant-i-create-a-project-on-saas-or-associate-my-service-in-the-project)" for guidance. Pay close attention to the filter settings for resource groups and regions.

## 3. Retrieving `WATSONX_API_KEY`, `WATSONX_URL`, and `PROJECT_ID`

To interact with watsonx.ai programmatically, you'll need to retrieve the API key, URL, and project ID.

### 3.1. Retrieving the `WATSONX_API_KEY`

The API key is often attached to your watsonx reservation in Tech Zone. Here's how to access and use it:

1.  **Locate API Key Information:** On your Tech Zone reservation details page, look for information related to the API key. This might be directly displayed or accessible through a link.
2.  **Access Control in Project:** In your watsonx.ai project, navigate to **Access Control** (usually found in the project settings or under the "Manage" tab).
3.  **Add Access Group:** Click on the "Add Collaborators" button and select "Add Access Group".
4.  **Search for Access Group:** Search for the Access Group name associated with your reservation. You can typically find this name mentioned in the environment details on your reservation page.
5.  **Import Access Group:** Select the correct access group and import it as an **Admin**. This step enables the use of the API key associated with that access group within your project. Refer to "[How to use the API Key attached to my watsonx reservation?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-use-the-api-key-attached-to-my-watsonx-reservation)" for more visual guidance, especially the section for Student ID environments which outlines the process clearly.

**Note:** The actual API key value might not be directly visible in the Tech Zone interface. The process above focuses on granting your project access to use the API key associated with your reservation's access group. When you use the watsonx.ai Python SDK or other programmatic interfaces, the authentication will happen based on this access.

### 3.2. Retrieving the `WATSONX_URL`

The `WATSONX_URL` will depend on the specific geographical location (region) where your watsonx.ai instance is provisioned. You can usually determine the region from your IBM Cloud account or the URL you use to access the watsonx.ai platform. Here are some common regional URLs:

* Dallas: `https://dataplatform.cloud.ibm.com`
* Frankfurt: `https://eu-de.dataplatform.cloud.ibm.com`
* Tokyo: `https://jp-tok.dataplatform.cloud.ibm.com`
* London: `https://eu-gb.dataplatform.cloud.ibm.com`

**To find the specific URL for your instance:**

1.  Log in to your IBM Cloud account (if using an IBM ID environment).
2.  Navigate to your list of resources.
3.  Find your watsonx.ai service instance.
4.  Click on the instance to view its details. The URL will usually be displayed on this page or will be the base URL you use to access the watsonx.ai platform.

For **Student ID environments**, the base URL will be the one you used to access the cloud account (e.g., the URL from the login link on your reservation page).

### 3.3. Retrieving the `PROJECT_ID`

You can find the `PROJECT_ID` within your watsonx.ai project:

1.  Open your project in the watsonx.ai platform.
2.  Navigate to the project settings or information page. The location might vary slightly depending on the interface updates, but it's usually found under a "Manage" or "Settings" tab.
3.  Look for a field labeled "Project ID" or similar. This will be a unique identifier for your project.

### 3.4. Storing Credentials in a `.env` File

It's a good practice to store sensitive information like API keys and URLs in a `.env` file. This prevents you from hardcoding them in your scripts.

1.  **Create a `.env` file:** In the root directory of your project, create a new file named `.env`.
2.  **Add Credentials:** Open the `.env` file and add the following lines, replacing the placeholders with your actual values:

    ```
    WATSONX_API_KEY=YOUR_WATSONX_API_KEY_VALUE
    WATSONX_URL=YOUR_WATSONX_URL
    PROJECT_ID=YOUR_PROJECT_ID
    ```

    **Important:** As mentioned in section 3.1, the `WATSONX_API_KEY` might not be a direct string value you copy. Instead, ensure you have correctly imported the access group associated with your reservation into your project. Your code should then be able to authenticate using the underlying credentials associated with that access group. You might need to refer to the documentation of the specific watsonx.ai SDK or library you are using for details on how it handles authentication in this scenario. It might involve using the IBM Cloud API key associated with your IBM ID (for IBM ID environments) or the credentials implicitly available through the Student ID environment after importing the access group.

## 4. Troubleshooting Common Errors

## Summary

Instructions how to navigate and troubleshoot issues on Techzone's watsonx Certified Base images. This guide shows workaround and provides background information on common errors and known issues.

## Table of Contents

### 1. IBM ID watsonx SaaS environments

* [Why am I not receiving a cloud account invite?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-am-i-not-receiving-a-cloud-account-invite)
* [Steps to create a Project on a watsonx.ai instance on SaaS](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#steps-to-create-a-project-on-a-watsonxai-instance-on-saas)
* [Why can't I create a project on SaaS or associate my service in the project?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-cant-i-create-a-project-on-saas-or-associate-my-service-in-the-project)
* [How to share my project?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-share-my-project)
* [Why can't I share my WatsonX project with a user?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-cant-i-share-my-watsonx-project-with-a-user)
* [I can't open watsonx.ai ('Get Started' button instead of 'Launch')](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#i-cant-open-watsonxai-get-started-button-instead-of-launch)
* [Why can't I access IBM Cloud?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-cant-i-access-ibm-cloud)
* [Why am I getting error "The AWS Access Key ID you provided does not exist in our records"?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#why-am-i-getting-error-the-aws-access-key-id-you-provided-does-not-exist-in-our-records)
* [Service is disabled, and I cannot select an option](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#service-is-disabled-and-i-cannot-select-an-option)
* [User Facing out of tokens error on watsonx.ai SaaS reservation](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#user-facing-out-of-tokens-error-on-watsonxai-saas-reservation)
* [How to use the API Key attached to my watsonx reservation?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-use-the-api-key-attached-to-my-watsonx-reservation)
* [(Optional) Backing up a project](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#optional-backing-up-a-project)

### 2. Student ID watsonx SaaS environments

* [What is Student ID environment?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#what-is-student-id-environment)
* [How to login with my Student ID?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-login-with-my-student-id)
* [How to get to the watsonx.ai platform via Student ID?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-get-to-the-watsonxai-platform-via-student-id)
* [How to use the API Key attached to my watsonx reservation?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-use-the-api-key-attached-to-my-watsonx-reservation)

[Back to Top](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#watsonx-troubleshooting-guide)

## IBM ID watsonx SaaS environments

### Why am I not receiving a cloud account invite?

1.  If you are already part of the account where the reservation is provisioned you will not receive an invite. You can start using your reservation upon provision.
2.  If you don't have the account and haven't received an invite, please [open a support case](https://ibmsf.force.com/ibminternalproducts/s/createrecord/NewCase?language=en_US) so that our team can quickly resend the invite for you or the user whom you shared with.

### Steps to create a Project on a watsonx.ai instance on SaaS

1.  On the IBM watsonx home, at the top left of the screen, select the menu button.

    ![watson-menu](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-menu.png)
2.  Within the sidebar menu, select the "View all projects" option.

    ![sidebar-menu-options](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-sidebar-menu-options.png)
3.  On the right side of the Projects page, select the "New project" button.

    ![new-project](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-new-project.png)
4.  Select either Project creation option.

    ![project-options](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-project-options.png)
5.  Fill the project "Name" field. Optionally, fill the "Description" field. Then at the bottom right, press the "Create project" button.

    ![project-details](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-project-details.png)
6.  Your project should be successfully created.

### Why can't I create a project on SaaS or associate my service in the project?

Why can't I create a watsonx.ai or watsonx project? Filter settings are stored as browser cookies and will continue to apply the filter on other pages including the "Creating a new project" page, preventing the user from creating a new project. Resources will not be displayed unless resource groups matching the resources are selected in the filter.

To resolve:

1.  Firstly ensure that the user has permissions from the parent reservation owner (unless they are the reservation owner)
2.  On the IBM watsonx Projects page, select any previous project.

    ![select-project](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-select-project.png)
3.  Next, ensure that you are on the "Manage" tab.

    ![manage-tab](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-manage-tab.png)
4.  Then, on the left menu bar, select "Services and Integrations"

    ![services-tab](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-services-tab.png)
5.  On the right side of the page, click on the "Associate service" button.

    ![associate-service](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-associate-service.png)
6.  Remove both the "resource group" filter and select the appropriate "region" filter. Region filter for COS (cloud object storage) is global, so region filter must be deselected, but WML (watson machine learning) is regional, so must match the region that the project was created in.

    ![filters](https://github.com/IBM/itz-support-public/blob/cbb2db54636f6ce44aaf2a87f37ea9d05c2c05d6/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-filters.png)
7.  Once the filters have been adjusted, click the "Cancel" button at the bottom right to exit.
8.  The user should now be able to create a new project.

### How to share my project?

The steps below are required in order to share a wastonx project you have created.

1.  Share reservation with user using share menu option on reservation card (not on reservation details page), you can see how to do that as illustrated in the image bellow
    ![reservations-card-share-watsonx](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/reservations-card-share-watsonx.png)
2.  Import your access group following the steps outlined [here](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-use-the-api-key-attached-to-my-watsonx-reservation):
3.  Ensure shared user accepts cloud invitation
4.  Ensure user initializes watsonx workspace in account and geo reservation was shared from

    > Geo Locations direct URLs
    >
    > * Dallas:  https://dataplatform.cloud.ibm.com/wx/home?context=wx
    > * Frankfurt: https://eu-de.dataplatform.cloud.ibm.com/wx/home?context=wx
    > * Tokyo: https://jp-tok.dataplatform.cloud.ibm.com/registration/steptwo?context=wx
    > * London: https://eu-gb.dataplatform.cloud.ibm.com/wx/home?context=wx
5.  The user should have access now as part of the access group.

### Why can't I share my WatsonX project with a user?

1.  Ensure you have imported the access group as outlined here in your project:
    * [How to use the API Key with my Student ID reservation?](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/watsonx_troubleshooting_guide.md#how-to-use-the-api-key-attached-to-my-watsonx-reservation)
2.  Share the reservation with the user and ensure they are part of the access group.

### I can't open watsonx.ai ('Get Started' button instead of 'Launch')

If you are getting stuck with the registration screen when attempting to access watsonx.ai via IBM Cloud please ensure to follow the steps below.

1.  Click 'Get started' button
2.  On the tab that opens go to the URL tab and remove the contents of the URL after the slash "/" part of the URL. This is illustrated below.
    The url should look similar to the one in the photo, depending on the geolocation. Notice the highlighted part.
    <img width="1725" alt="image" src="https://github.com/IBM/itz-support-public/assets/152641641/6ea4116b-b4d0-4c2d-8845-8abe812e518c">
3.  Once you remove the part after the slash "/", the URL should look like this (depending on the geolocation):
    * Dallas:  https://dataplatform.cloud.ibm.com
    * Frankfurt: https://eu-de.dataplatform.cloud.ibm.com
    * Tokyo: https://jp-tok.dataplatform.cloud.ibm.com
    * London: https://eu-gb.dataplatform.cloud.ibm.com
4.  Click enter and that will take you to the watsonx.ai homepage. If you are first time user you will be prompted to select the cloud account from your reservation. Check the reservation page and select the same cloud account.

### Why can't I access IBM Cloud?

What Happens If I Do Not Accept the IBM Cloud Invitation? If you do not accept the IBM Cloud invitation, as specifically directed in the reservation details you will encounter an error.

![watsonx Cloud Error](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-cloud-error.png)

![IBM Cloud Reservation Details](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ibmcloud-reservation-details.png)

To accept the invitation, either navigate to the email you should receive within 24 hours of creating your IBM Cloud account, or navigate to the bell notification icon on the top right of the IBM Cloud page, and on the right side of the screen you will see a notification that says "You are invited to join an account in IBM Cloud", click the blue hyperlink on the right of your screen that says "Join now."

![Bell Icon](https://github.com/IBM/itz-support-public/blob/1395e12dd3ca6461ec5d19f7feec469108bb6a0d/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/ibmcloud-notification.png)

### Why am I getting error "The AWS Access Key ID you provided does not exist in our records"?

![cos-error](https://github.com/IBM/itz-support-public/blob/cb24717ff45c577a2e12d96ff994791330ca81e1/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watsonx-cos-error.png)

The AWS access key error indicates that your COS instance was deleted. The COS instance is deleted either by reservation expiry or user deletion. To resolve, you must create a fresh reservation and re-associate the new COS instance with project.

### Why can't I create a COS instance?

I shared my reservation with a user but they cannot create a COS instance, how can a shared user create a COS instance? Shared users shouldn’t be creating a new COS instance, they should be using the COS instance that came with the reservation.

This might occur if the COS instance has been deleted, the reservation becomes unusable because all the services might have been deleted. A new reservation must be created.

### Service is disabled, and I cannot select an option

If service is disabled and you are unable to select an option you should try entering the regional watsonx.ai URLs directly.

![watsonx-troubleshooting](https://media.github.ibm.com/user/358578/files/80ee0e90-50ee-4e37-af2f-7cb1c08fe746)

Enter the appropriate regional watsonx.ai URL directly, based on these options:

* Dallas:  https://dataplatform.cloud.ibm.com/wx/home?context=wx
* Frankfurt: https://eu-de.dataplatform.cloud.ibm.com/wx/home?context=wx
* Tokyo: https://jp-tok.dataplatform.cloud.ibm.com/registration/steptwo?context=wx
* London: https://eu-gb.dataplatform.cloud.ibm.com/wx/home?context=wx

### User Facing out of tokens error on watsonx.ai SaaS reservation

Often occurs when a user associates a personal WML instance to their created project. If they were to associate the correct WML, there would not be restrictions such as no tokens, so the user needs to reassociate the WML instance or create a new project with the correct WML.

I have an Out of Token error on my watsonx.ai SaaS reservation. This happens when you associate a personal WML instance to your created project. If you associate the correct WML, there would not be restrictions such as no tokens, so the user needs to reassociate the WML instance or create a new project with the correct WML.

### (Optional) Backing up a project

To back up projects before reservation expires so that you do not lose projects on a dedicated account, you must specify the value of the "_Default install of dedicated services (customer poc), or use shared services? Note that dedicated services include the COS instance that will get destroyed with your project data upon expiry, so be sure to export your projects as needed when choosing dedicated._" field.

![backup-field](https://github.com/IBM/itz-support-public/blob/52c7807676a1394d1474c90bf6ad8bae0974b0b9/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/watson-backup-field.png)

\_Dedicated is an isolated environment. Shared is a shared environment access.\_

## Student ID watsonx SaaS environments

### What is Student ID environment?

The watsonx Student ID environments are now available as part of Certified Base images collection. They offer an alternative way for users to access the watsonx services via a dedicated login page with a user provided by Techzone. Student ID environments are marked with the \_Student ID\_ tag.

### How to login with my Student ID?

1.  Review and ensure you have reserved a Student ID environment. They contain the Student ID tag in the title and a clarifying text in the tile of the card: **This does not use IBM ID. Do not use the regular IBM Cloud login page. Use the login page from the reservation. Demo environments with API requirements should use the IBM ID version for now.**
2.  Once you have provisioned your environment, navigate to the reservation page and you will notice that there is a different login in link and credentials provided. They are different from logging into IBM Cloud directly.

    ![studentid-resdetails](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-resdetails.png)
3.  Open the access link in a private tab or ensure you have logged out of your own IBM Cloud account. The URL name will be different depending on the cloud account where your reservation is.

    ![studentid-loginpage](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-loginpage.png)
4.  Enter the credentials provided within the reservation, do not use your IBM ID.
5.  Click login and you will be redirected to the cloud account.

### How to get to the watsonx.ai platform via Student ID?

1.  Once you have logged in to the cloud account using the Student ID, navigate to the resource list and find the watson studio instance.

    ![studentid-resources](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-resources.png)
2.  Select the instance and click 'Launch in watsonx'.

    ![studentid-studio](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-studio.png)
3.  A form will be prompted requesting to provide details. Wait for up to a minute and the form will disappear and click the continue button, then the platform will apear.

    ![studentid-form](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-form.png)

### How to use the API Key attached to my watsonx reservation?

1.  To enable the use of API Key, open the project settings under Access Control.

    ![studentid-dropdown](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-dropdown.png)
2.  Click the Add Collaborators button and select Add Access Group.
3.  Search for the Access Group name (you can find your access group name under environment on your reservation page).
4.  Select the access group and import it as admin.

    ![studentid-agadd](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/studentid-agadd.png)
