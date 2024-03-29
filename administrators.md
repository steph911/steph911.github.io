# Quick Start Tasks for Administrators

This page includes the following topics: 
- Understand the Appliance Deployment
- Install the ownCloud Server Appliance
- Activate the Appliance
- Access the ownCloud Server
- Create a User Account
- Enable Users to Connect to the ownCloud Server
- Next Steps

## Understand the Appliance Deployment

The ownCloud server appliance provides a pre-packaged ownCloud appliance that you can deploy in an existing ESX, VirtualBox, KVM, and VMware virtual machine. This deployment option supports up to 500 users.

The ownCloud 10 virtual image includes all of the software that you need to deploy and run ownCloud, including:
- ownCloud 10.x Server and Enterprise Apps
- Apache 2
- PHP
- MySQL database
- ownCloud Proxy app

The image is pre-configured for secure connections. 

## Install the ownCloud Server Appliance

Before you deploy the ownCloud Server appliance, verify that you have a supported virtual environment. The ownCloud appliance supports the following virtual environments:

- ESXi
- VirtualBox
- VMWare
- KVM

**Complete these steps**: 

1. [Download](https://owncloud.org/download/) the appliance. The ownCloud download is 1.4GB, and may take significant time to download.
1.  Import the appliance files into your virtual machine and launch ownCloud.
1. Start the ownCloud server to launch the configuration wizard.
1. Provide the following information in the configuration wizard: 
- **Localization settings**: Enter language, default locale, and keyboard layout information.
- **Domain and network settings**:  Enter the IP address of the virtual machine, or enable the wizard to obtain the IP address automatically.
- **Domain set up**: Specify where users and permissions are managed. By default, users and permissions are managed in ownCloud. 
- **Account information**:  Specify organization name, the email address (used for receiving the license which you’ll need to activate the appliance), and the administrator password. Specify the password for the administrator (or root user) of the virtual machine, not for the ownCloud installation.
- **Host settings**: Specify the fully-qualified domain name of the virtual appliance and an LDAP Base DN.
**Note**: If you are not familiar with setting up FQDNs and hosts, accept the default settings. 

## Activate the Appliance

After installation, activate the ownCloud appliance by uploading the license file. ownCloud sends the license file to the email address that you specified in the configuration wizard. 

1. Save the license file to your computer.
1. In a web browser, go to https://_virtual_host_IPaddress_. The IP address should match the IP Address that you configured in the configuration wizard.
1. Click **Upload License File**.

## Access the ownCloud Server

After you activate the ownCloud server, you are automatically redirected to the Univention Management Console. The Management Console enables you to manage the virtual appliance, including users, devices, domains, and software. You can also access the ownCloud web interface from the Management Console. 

**Note**: If you are not redirected automatically, use the following URL to access the Management Console: 
```
https://<ip address of the virtual machine>/univention-management-console
```
The default username _and_ password for the Management Console is `ownCloud`.

### Change the ownCloud Server IP Address and Port

If you selected automatic IP address detection in the configuration wizard, you can change the URL that users use to access the ownCloud Server. For example, you can enable users to access the ownCloud Server with a URL that resembles the following example:

```
https://123.45.678.0:8080
```
You can overwrite the initial IP address and port in the Univention Management Console. Go to **System and Domain Settings**, **System**.

**Note**: You can also overwrite the IP address and port in the config/config.php file. See Proxy Configuration in [Config.php Parameters](https://doc.owncloud.com/server/10.1/admin_manual/configuration/server/config_sample_php_parameters.html) in the Admin Manual.

## Create a User Account

As an ownCloud Administrator or Group Administrator, you can add new user accounts.

1. Log in to Univention Management Console.
1. Click **Users**. Then, click **Add**.
1. Enter the first and last name of the user. Also enter the username that they will enter to log in to ownCloud.
1. Enter a password for the user account.
1. (Optional) Select one or more options to control password behavior, or to disable the account.
1. Click **Create User**.

**Note**: You assign users to groups for easy administration. See [User Roles](https://doc.owncloud.com/server/10.3/admin_manual/configuration/user/user_roles.html) in the ownCloud User Manaual for more information. 


## Enable Users to Connect to the ownCloud Server

Your ownCloud Server is now up and running, and you’ve created user accounts for users who can access the server.
Provide those users with the following information: 
- The ownCloud Server hostname or IP address, and port. For example: 
```
https://123.45.345.0:8080
```
- The username that you created when you added the user account.
- The password for the account.

Users enter this information when they install the ownCloud desktop client or app.    

## Next Steps

To install the Desktop Synchronization Client or the Android or iOS app, see [Quick Start Tasks for Users](users.md). 

To learn more about the ownCloud server, and how to configure it for your business, see the [Admin Manual](https://doc.owncloud.com/server/10.3/admin_manual/). 

[Return to the Quick Start Main Page](https://steph911.github.io)


















