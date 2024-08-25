# CODTECH-Task2
Name: THUMUGANTI LAHARI

Company: CODTECH IT SOLUTIONS

ID: CT8WD1420

Domain: WEB DEVELOPMENT

Duartion: JUNE 25th 2024 TO AUGUST 25TH 2024

**OVERVIEW OF THE PROJECT**

Project: To do list app

Objective:

The objective of this to-do list app is to provide a simple and efficient tool for managing tasks. It allows users to create, view, and complete tasks, making it a convenient way to stay organized and focused. By utilizing local storage, the app ensures that tasks are persisted even after the browser window is closed, providing a seamless user experience. Additionally, the app's user-friendly interface and clear task management features make it easy for users to prioritize and track their tasks effectively.

It builds a simple to-do list application using HTML, CSS, and JavaScript. Here's a breakdown of each part:

**HTML (index.html):**

-Defines the basic structure of the web page.

-Creates a container element with the ID app to hold the to-do list components.

-Includes an h1 element for the title ("To do list").

-Defines an unordered list (ul) to display the to-do items.

-Includes an input field for users to enter new tasks and a button to add them.

-Adds a descriptive paragraph below the input field.

**CSS (style.css):**

-Sets up a global stylesheet for consistent formatting across elements.

-Defines styles for the body element:

*Centered content using justify-content: center; and align-items: center;*

*Full viewport height (height: 100%;) and width (width: 100%;)*

*Background color and font family*

-Styles specific elements:

*h1 with a decorative font, centered text, and large size*

*ul with specific font style and margin*

*li list items with margins and color*

*Styled links within list items for marking tasks complete (including hover effect)*

*Input field and button with appropriate sizing, colors, and hover effects*

**JavaScript (app.js):**

-Selects elements from the HTML:

*The unordered list (#app ul)*

*The input field (#app input)*

*The button (#app button)*

-Retrieves existing to-do items from local storage (if available) using JSON.parse(localStorage.getItem("list_todos")) and stores them in a todos array.

-Defines a function renderTodos() to populate the list:

*Clears the existing list content (listElement.innerHTML = "";)*

*Iterates through the todos array*

*Creates a new list item (li) and text node for each item*

*Creates a link element (a) with an "onclick" attribute to call the deleteTodo function and display "done" text*

*Appends the task text and link to the list item*

*Adds the list item to the main list (listElement)*

-Calls renderTodos() to initially display any existing to-do items from local storage.

-Defines a function addTodo() to add new tasks:

*Retrieves the user input from the input field (var todoText = inputElement.value;)*

*Adds the new task to the todos array (todos.push(todoText);)*

*Clears the input field (inputElement.value = "";)*

*Calls renderTodos() to update the list with the new item*

*Calls saveToStorage() to persist the updated list in local storage*

-Attaches an event listener to the button click that calls the addTodo() function.

-Defines a function deleteTodo(pos) to remove completed tasks:

*Removes the task from the todos array based on its position (todos.splice(pos, 1);)*

*Calls renderTodos() to update the list with the removed item*

*Calls saveToStorage() to persist the updated list in local storage*

-Defines a function saveToStorage() to store the todos array in local storage:

*Converts the array to JSON format (JSON.stringify(todos))*

*Stores the JSON data in local storage using localStorage.setItem("list_todos", JSON.stringify(todos));*

**Overall functionality:**

1.The app retrieves and displays any previously saved to-do items from local storage upon loading.

2.Users can enter new tasks in the input field.

3.Clicking the "Add" button triggers the addTodo() function, which adds the new task to the list and local storage.

4.Clicking the link next to a task calls the deleteTodo() function, removing it from both the list and local storage.

*This is a basic to-do list app and can be further enhanced to offer features like editing tasks, marking them as incomplete, or prioritizing tasks.*

*Local storage is used to persist data even after the browser window is closed. However, this data is specific to the user's device.*
