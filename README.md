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

| Funcionality                | Scenario                                                                                                          |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| User login and registration | Check users can register and logged users have access to their task list and all app actions                      |
| Change user password        | Check logged user can change password, do it, log out and try to log in again                                     |
| Change user data            | Login to account, change existing data like nickname, avatar after submit check the data is the new               |
| Create new task             | Move to task list as logged user, try to create new task and after submit, check the list is updated              |
| Update exisitng task        | Move to task list as logged user, try to update existing task and after submit, check the task has new data       |
| Delete exisitng task        | Move to task list as logged user, try to delete task and after submit, check the list doesnt contain deleted task |
| Mark task as completed      | Move to task list as logged user, try to mark task as completed after action, check the progress is updated       |
| Check notifications         | Try to get notification or remindner and check everythink is correct                                              |

### 1d. Testing enviroments

Its React Native mobile application then we want to testing it on android and iOS operating systems. We use for it a lot of kind real devices with different resolution and symulators/emulators.

### 1e. Success

- All app's features work correctly
- App works smooth and without delays
- App doesn't have bugs and errors

## 2. Unit tests

We will use TDD method to write unit tests. We write a piece of the test and create software code for it, after that we do refactor for this unit. It gives us posibility to create minimalist code. Additionaly we generate in the same time code and tests. The tests can be type of documentation of our code. It very useful way to build high performance applications.

We need to test every simple component like:

- `<LoginForm />`, `<TasksList />`

and methods like:

- create, update, delete task,

### EXAMPLE:

```
import React from 'react';
import { render, fireEvent } from '@testing-library/react-native';
import TodoList from '../TodoList';

describe('Create new task test', () => {
  test('Add new task', () => {
    const { getByPlaceholderText, getByText } = render(<TodoList />);

    const inputField = getByPlaceholderText('New Task');
    const addButton = getByText('Add');

    fireEvent.changeText(inputField, 'Task example');
    fireEvent.press(addButton);

    const addedTask = getByText('Task example');
    expect(addedTask).toBeTruthy();
  });
});

```
