# Features

**User Management** opens as separate web application via app switcher of main application where admin can manage users and roles. This application has two tabs, namely **Manage Users** and **Manage Roles**. Depending upon the solutions requirements of Manage Roles we can enable or disable it from configuration but still roles can be managed via SQL directly.

## Manage Users

In the application user can see the list of all users available in database. User can be created, edited and deleted. Super admin user \(username is admin\) cannot be deleted, only it's password can be changed. Super admin cannot be disabled too. It is created during setup of User Management for solutions.

Admin users can change his personal details, password and so on. They can not delete, disable or change role of themself. Only other admin users can do it for them.

## New User

Create user can be done via **Add User** button. Enter details in all the required fields \(personal details\), assign him a pre-defined role and if application has option for dimension permissions then dimensions values can be chosen for the user. Display of dimension permission tabs is controlled by database only.

After user is successfully created, user details can be modified except\(user\_id\). Admin user cannot delete or disable himself.

Timezone field will be shown as drop-down if application support multiple timezone at same time else this will display as label only.

For LDAP users only Roles or Dimensions permissions can be modified, rest all fields are non-editable. Enabled or disable users is not available in case of LDAP users.

## Manage Roles

In this tab, we will see list of roles available in this system. Admin can create new roles by clicking **Add Role** button. He will see popup showing all the modules or privileges of the system.

Roles is nothing but combination of module, service, feature privileges or permissions.

Admin can edit and delete roles.

This UI feature, will be optional, depends on solution use case. If Roles are pre-defined \(fixed\), we can use SQL scripts to create roles. No need to show Role Management UI.

## LDAP Support

For users who needs authentication from LDAP will be first authenticated from LDAP server, once verified then we will create entry in our database for that user and assign him some default role as per the required solution policy. User Management's current design will provide a hook to assign roles for newly created users via LDAP authentication.

LDAP feature is configuration via solutions.

### i18n Support:

User Management provides support internationlization so that it can easily be adapted to a specific language. As of now it support English as a default language and it can be configured for German language suport.

## Notification Service

The Notification service feature provided by User Management can be used by any third party solution which is using User Management. The aim of the this feature is to send a notification to third party solutions whenever any aspect of user changes.

**User Management** uses [Kafka](http://kafka.apache.org) for its notification service. It sends a notifcation whenever a user or role is created, updated or deleted.

## REST API

User Management exposed an extensive sets of REST APIs that can be used to manage users and roles. It also provides APIs for managing the applications and permissions. All the User Management REST APIs are secured. So user needs to authenticate himself before using these APIs.

## OAuth Intgration

User Management integrated with Oauth via configuration. OAuth provide mechanism for Login and other Authentication.

## Custom Exceptions

User Management has its custom exception handling mechanism written on top spring's default exception handling feature. It throws a pre-defined exception \(code, message and status\) due to which its easier for solutions to debug and issue when acccessing the REST APIs exposed by User Management.

## User Management Client

User Management clients have Java methods to access all REST APIs of User Management Server. User Management Server can be integrated with any third party java applications like OAuth, Service Reflex or Marleting Reflex backend solutions with client Java methods.

