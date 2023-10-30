# Connect to NebulaGraph

After successfully launching Explorer, you can enter database credentials to connect to the database. You can connect directly to NebulaGraph by default. 

!!! note

    To ensure data security, OAuth2.0 and CAS authentication are also supported. You can connect to NebulaGraph only after the authentication is passed. For detailed configuration, see [Deploy Explorer](ex-ug-deploy.md).

## Prerequisites

Before connecting to the NebulaGraph database, you need to confirm the following information:

- The NebulaGraph services and Explorer are started. For more information, see [Deploy Explorer](../deploy-connect/ex-ug-connect.md).

- You have the local IP address and the port used by the Graph service of NebulaGraph. The default port is `9669`.

- You have a NebulaGraph account and its password.

- We recommend you to use the Chrome browser of the version above 89. Otherwise, there may be compatibility issues.

## Procedure

To connect Explorer to NebulaGraph, follow these steps:

1. Type `http://<ip_address>:7002` in the address bar of your browser.

  The following login page shows that Explorer is successfully connected to NebulaGraph.

  <img src="https://docs-cdn.nebula-graph.com.cn/figures/eo_expl_login_230913_en.png" width="1200" alt="A screenshot that shows the login UI of explorer">

  !!! note

        When logging into NebulaGraph Explorer for the first time, the content of *END USER LICENSE AGREEMENT* is displayed on the login page. Please read it and then click **I agree**.

2. On the **Config Server** page of Explorer, configure these fields:

  - **Graphd IP address**: Enter the IP address of the Graph service of NebulaGraph. For example, `192.168.10.100`.

    !!! note

        - When NebulaGraph and Explorer are deployed on the same machine, you must enter the IP address of the machine, instead of `127.0.0.1` or `localhost`.
        - When connecting a NebulaGraph database on a new tab, The new session will overwrite the sessions of the old TAB. If you need to log in to multiple NebulaGraph databases at the same time, you can use different browsers or non-trace mode.

  - **Port**: The port of the Graph service. The default port is `9669`.

  - **Username** and **Password**: Fill in the log in account according to the [authentication settings](../../7.data-security/1.authentication/1.authentication.md) of NebulaGraph.

    - If authentication is not enabled, you can use `root` and any password as the username and its password.

    - If authentication is enabled and no account information has been created, you can only log in as GOD role and use `root` and `nebula` as the username and its password.

    - If authentication is enabled and different users are created and assigned roles, users in different roles log in with their accounts and passwords.

3. After the configuration, click the **Login** button.

  !!! note

        One session continues for up to 30 minutes. If you do not operate Explorer within 30 minutes, the active session will time out and you must connect to NebulaGraph again.

A welcome page is displayed on the first login, showing the relevant functions according to the usage process, and the test datasets can be automatically downloaded and imported.

To visit the welcome page, click ![help](https://docs-cdn.nebula-graph.com.cn/figures/navbar-help.png) -> **Beginner's Guide**.

## Clear connection

When Explorer is still connected to a NebulaGraph database, on the upper right corner of the page, select ![icon](https://docs-cdn.nebula-graph.com.cn/figures/nav-setup.png) > **Clear Connect**.

After that, if the **configuration database** page is displayed on the browser, it means that Explorer has successfully disconnected from the NebulaGraph.