---
author: kengaderdus
ms.service: entra-external-id
ms.subservice: customers
ms.topic: include
ms.date: 03/30/2023
ms.author: kengaderdus
ms.manager: mwongerapk
---
To grant your client app (*ciam-client-app*) API permissions, follow these steps:

1. From the **App registrations** page, select the application that you created (such as *ciam-client-app*) to open its **Overview** page.
 
1. Under **Manage**, select **API permissions**.
 
1. Under **Configured permissions**, select **Add a permission**.

1. Select **Microsoft APIs** tab.

1. Under **Commonly used Microsoft APIs** section, select **Microsoft Graph**.

1. Select **Delegated permissions** option.

1. Under **Select permissions** section, search for and select both **openid** and **offline_access** permissions.

1. Select **Add permissions** button. 
 
1. Under **Configured permissions**, select **Add a permission** again.

1. Select the **My APIs** tab.
 
1. In the list of APIs, select the API such as *ciam-ToDoList-api*.
 
1. Select **Delegated permissions** option.
 
1. From the permissions list, select **ToDoList.Read, ToDoList.ReadWrite** (use the search box if necessary).
 
1. Select the **Add permissions** button.
 
1. At this point, you've assigned the permissions correctly. However, since the tenant is a customer's tenant, the  consumer users themselves can't consent to these permissions. To address this problem, you as the admin must consent to these permissions on behalf of all the users in the tenant:

    1. Select **Grant admin consent for \<your tenant name\>**, then select **Yes**.

    1. Select **Refresh**, then verify that **Granted for \<your tenant name\>** appears under **Status** for both scopes.

1. From the **Configured permissions** list, select the **ToDoList.Read** and **ToDoList.ReadWrite** permissions, one at a time, and then copy the permission's full URI for later use. The full permission URI looks something similar to `api://{clientId}/{ToDoList.Read}` or `api://{clientId}/{ToDoList.ReadWrite}`.