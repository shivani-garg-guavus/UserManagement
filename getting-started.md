# Getting-Started

As stated earlier User Management provides API' for modifying any aspects of user like its role, permission etc. When integrating with User Management, solutions might need create new users, roles, permissions and applictions as per their needs.As described earlier Roles are nothing but combination of Permissions and a Permission can be anything like a module, solution, service or an API. So in a way Permission represent feature or module level control for the user. User Mangement support Service permission only like for example a service permission can be whether an user has access to User Managment application or not.

1. Installation of User Management is part of platform installation, click [here](https://confluence.guavus.com/display/PA/UM+installation+guide).
2. Integration of any solution with UserManagement, click [here](https://confluence.guavus.com/display/PA/User+Management+Integration+with+Solution).

After Integration with UM Solution, user can login to User Management application by using default admin user and utilize the user interface for creating new users and roles, but Solution specific permissions and applications can not be created using the UI. To create default set of a permissions and applications solution need to use [this public](https://confluence.guavus.com/display/PA/User+Management+API#UserManagementAPI-PublicAPIs) API at the time of solution installation on top of platform.

