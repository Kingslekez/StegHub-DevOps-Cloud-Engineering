Created three component files, then attempted to write an Input.js component with syntax errors—missing closed braces, brackets, and incomplete render logic, was carefully fixed.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Creating%20Input.js%20component%20with%20incompletemalformed%20code%20(syntax%20errors).png)


Installing the <mark>axios</mark> dependency in the client directory to make HTTP requests from React components to the backend API endpoints.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Installing%20axios%20dependency%20in%20the%20client%20directory.png)


creating <mark>ListTodo.js</mark>, a functional component that renders a list of todos with click-to-delete functionality, mapping through todos prop and calling <mark>deleteTodo</mark>.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Creating%20ListTodo.js%20component%20with%20delete%20functionality.png)

creating <mark>Todo.js</mark>, a class component that fetches todos on mount, stores them in state, and handles deletion via API calls using axios.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Creating%20Todo.js%20component%20with%20getTodos%20and%20deleteTodo%20methods.png)


Updating <mark>App.js</mark> to import and render the <mark>Todo</mark> component inside a div with className "App", integrating the todo functionality into the root component.


![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Updating%20App.js%20to%20import%20and%20render%20the%20Todo%20component.png)

Adding CSS styling in <mark>App.css</mark> for the Todo app, including centered layout, custom input styles, and button styling with dark theme colors.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Adding%20CSS%20styling%20in%20App.css%20for%20the%20Todo%20app.png)

Updating <mark>index.css</mark> with global styles, including dark background <mark>#282c34</mark>, font settings, and box-sizing for the entire application.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Updating%20index.css%20with%20global%20styles.png)

Running the full-stack application with <mark>npm run dev</mark>, concurrently starting the Express backend on port 5000 and React frontend on port 3000. Both compile successfully.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/Running%20the%20full%20stack%20application%20with%20npm%20run%20dev%20(both%20backend%20and%20frontend).png)

The image below shows the React Todo app UI displaying a heading "My Todo(s)", an input field, and "No todo(s) left" message, indicating no todos currently exist.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/9fb49877af77fa32ba1b7a3bbb12da9a7e2e77a4/MERN%20STACK/Images/The%20React%20Todo%20app%20UI%20displaying%20No%20todo(s)%20left.png)