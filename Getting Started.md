# Getting Started

As stated earlier User Management provides APIs for modifying any aspect of an user like its role, permission etc. When integrating with User Management, solutions might need to create new users, roles, permissions and applictions as per their needs. As described earlier roles were nothing but combination of permissions and a permission can be anything like a module, solution, service or an API. So in a way permission represent feature or module level control for the user. User Management supports service permission only. For example, a service permission can be whether an user has access to User Managment application or not.

1. Installation of User Management is part of platform installation, click [here](https://confluence.guavus.com/display/PA/UM+installation+guide).
2. Integration of any solution with UserManagement, click [here](https://confluence.guavus.com/display/PA/User+Management+Integration+with+Solution).

After Integration with UM Solution, user can log into User Management application by using default admin user and utilize the user interface for creating new users and roles, but solution specific permissions and applications can not be created using the user interface. 
To  create  default set of a permissions and applications solution needs to use [this public](https://confluence.guavus.com/display/PA/User+Management+API) API  at the time of solution installation on top of platform.
