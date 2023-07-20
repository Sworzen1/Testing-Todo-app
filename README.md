# Testing-Todo-app
## 1. Testing plan
A well thought out and well written test plan allows you to quickly and thoroughly test all aspects of your application. Thanks to this, we will save resources such as time and manpower. It defines the level of risk, allows for early detection of errors and threats. It is a kind of documentation about the project. It clearly defines the goals and tasks for the test team, and can be a support for developers
### 1a. Test goals
  - Check that all functions work properly
  - Check that the application does not return errors that may cause it to stop
  - Check application performance
### 1b. Functional range
  - User login and registration
  - Change user password
  - Change user data
  - Create new task
  - Update existing task
  - Delete existing task
  - Mark task as completed
  - Check notifications

### 1c. Testing scenario based on functionalities
| Funcionality             |  Scenario   |
| ----------------- | ------------------------------------------------------------------ |
| User login and registration | Check users can register and logged users have access to their task list and all app actions |
| Change user password | Check logged user can change password, do it, log out and try to log in again |
| Change user data | Login to account, change existing data like nickname, avatar after submit check the data is the new |
| Create new task | Move to task list as logged user, try to create new task and after submit, check the list is updated |
| Update exisitng task | Move to task list as logged user, try to update existing task and after submit, check the task  has new data |
| Delete exisitng task | Move to task list as logged user, try to delete task and after submit, check the list doesnt  contain deleted task |
| Mark task as completed | Move to task list as logged user, try to mark task as completed after action, check the progress is updated |
| Check notifications | Try to get notification or remindner and check everythink is correct |
