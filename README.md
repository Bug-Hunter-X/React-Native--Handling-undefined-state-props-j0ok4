# React Native: Handling undefined state/props

This repository demonstrates a common error in React Native applications: attempting to access state or props before they have been properly assigned values. This often occurs when dealing with asynchronous operations, such as fetching data from an API.

The `Bug.js` file showcases the problematic code that leads to the `Cannot read properties of undefined (reading '...property...')` error.  The `BugSolution.js` file presents a corrected version, illustrating how to properly handle asynchronous operations and prevent the error.

## Setup:

1. Clone this repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install` or `yarn install` to install the dependencies.
4. Run the application using `npx react-native run-android` or `npx react-native run-ios`.

## Error Explanation:

The error arises when a component tries to use a state variable or prop that hasn't been populated yet.  This is usually due to the component rendering before the data is ready.  This commonly happens when fetching data from an API or using other asynchronous actions.

## Solution:

The solution involves ensuring that the component only tries to access the state or prop *after* it has been assigned a value.  This typically involves using conditional rendering or the optional chaining operator.