## 0. Commence with class components

#### Start this project with files from the the last task of the 0x03. React Props project:

Convert the App function into a React Class:

- Modify the function within App.js to convert the App function into a React class
- Make sure that the tests are still passing

#### Requirements:

- At this point, reloading the App should display the exact same page as the last task
- The console in your browser should not show any error or warning

### 1. Lifecycles

Add lifecycle to a component

#### In the App Class:

Add a props named logOut with the props type being function
The default value for this property, should be an empty function
Add an event listener when the component is mounted to listen to when the user is pressing down the keyboard keys
When the user is pressing down the control and the h keys simultaneously, display the alert Logging you out and call the function logOut
Add the tests

#### In the test file for the App Class:

Create a test to verify that when the keys control and h are pressed the logOut function, passed as a prop, is called and the alert function is called with the string Logging you out
Requirements:

- Make sure to remove the event listener when the component is unmounted
- In the test file, make sure to restore the alert function you mocked
- At this point, reloading the App should display the exact same page as the last task
- The console in your browser should not show any error or warning

## 2 Handling Events
mandatory
Create a new handing event

In the Notifications component:

Convert the function into a React Class
Make sure that the tests are still passing
Create a new markAsRead function within the Notifications class. It accepts one argument: id(number)
When the function is called, it logs to the console the message “Notification $id has been marked as read
Pass the function markAsRead to the NotificationItem component as a property
In the NotificationItem Class:

Modify the li element to call the new function markAsRead on click. It should send the id of the notification
Define the new property type and the default property for the new properties
Add the tests

In the Notifications test file:

Create a test, that will mockup the console.log function
Check that when calling the function markAsRead on an instance of the component, the spy is being called with the right message
In the NotificationItem test file:

Create a test, that will pass a spy as the markAsRead property
Check that when simulating a click on the component, the spy is called with the right ID argument
Requirements:

Make sure to bind the function markAsRead in your constructor to avoid unecessary re-rendering
In the test file, make sure to restore the console function you mocked
At this point, reloading the App should display the exact same page as the last task. Use the React Chrome Extension to make sure the Notifications component displays correctly
The console in your browser should not show any error or warning

### Containment

Create a new component named BodySection. The component does not know its children. It should output the following:

A div with the class bodySection
Within the div, a h2 element containing a title passed as a prop
Under the h2 the children of BodySection
Tips:

Rendering the following

### 4. Specialization
mandatory
in task_3/dashboard/src/BodySection/BodySectionWithMarginBottom.js, create a new component named BodySectionWithMarginBottom. The component does not know its children. It should output the following:

A div with the class bodySectionWithMargin
Within the div, a BodySection element with the same props passed to bodySectionWithMargin
in task_3/dashboard/src/BodySection/BodySectionWithMarginBottom.css

Set the style for the class bodySectionWithMargin with a margin bottom of 40px
Import the styling into the BodySectionWithMarginBottom component
Requirements:

Make sure to define the propTypes for both props
Do not repeat each props manually and use the spread operator

### 5. Use the new components
mandatory
in task_3/dashboard/src/App/App.js, modify the App component:

Wrap the CourseList component with the newly created BodySectionWithMarginBottom component. The title should be Course list
Wrap the Login component with the newly created BodySectionWithMarginBottom component. The title should be Log in to continue
Using the BodySection component, add a new block with the title News from the School. The component should contain a paragraph with some random text
Repo:

GitHub repository: alx-react
Directory: 0x03-React_component
File: task_3/dashboard/src/App/App.js