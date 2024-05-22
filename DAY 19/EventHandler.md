
| Event Handler   | Definition                                      | Syntax                                  | Example                                       | Explanation                                                                                                                                                                    |
|-----------------|-------------------------------------------------|-----------------------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| onclick         | Triggered when an element is clicked.           | `<element onclick="functionName()">`    | `<button onclick="alert('Button clicked')">Click Me</button>` | This event handler executes a function when the element is clicked.                                                                                                          |
| onsubmit        | Triggered when a form is submitted.             | `<form onsubmit="functionName()">`      | `<form onsubmit="validateForm()">...</form>`        | This event handler executes a function when the form is submitted. It's commonly used to validate form inputs before submitting.                                              |
| onload          | Triggered when a webpage finishes loading.     | `<body onload="functionName()">`       | `<body onload="init()">`                           | This event handler executes a function when the webpage has finished loading. It's useful for initializing scripts or elements upon page load.                              |
| onmouseover     | Triggered when the mouse pointer moves over an element. | `<element onmouseover="functionName()">` | `<div onmouseover="highlight()">...</div>`          | This event handler executes a function when the mouse pointer moves over the element. It's often used to provide visual feedback or trigger actions.                        |
| onmouseout      | Triggered when the mouse pointer moves out of an element. | `<element onmouseout="functionName()">` | `<div onmouseout="removeHighlight()">...</div>`     | This event handler executes a function when the mouse pointer moves out of the element. It's commonly used to revert changes made by onmouseover.                            |
| onchange        | Triggered when the value of a form element changes. | `<element onchange="functionName()">`  | `<input type="text" onchange="validateInput()">`   | This event handler executes a function when the value of the form element changes. It's useful for live validation or updating dependent elements.                             |
| onkeydown       | Triggered when a key is pressed down.          | `<element onkeydown="functionName()">` | `<input type="text" onkeydown="handleKeyPress()">` | This event handler executes a function when a key is pressed down while the element is focused. It's commonly used for capturing user input.                                |
| onkeyup         | Triggered when a key is released.              | `<element onkeyup="functionName()">`   | `<input type="text" onkeyup="handleKeyUp()">`      | This event handler executes a function when a key is released after being pressed down while the element is focused. It's useful for responding to user input.              |
| onfocus         | Triggered when an element gets focus.          | `<element onfocus="functionName()">`   | `<input type="text" onfocus="highlight()">`        | This event handler executes a function when the element receives focus (e.g., via clicking or tabbing). It's commonly used to provide visual cues or initiate actions.    |
| onblur          | Triggered when an element loses focus.         | `<element onblur="functionName()">`    | `<input type="text" onblur="validateInput()">`     | This event handler executes a function when the element loses focus. It's often used for validation or cleanup tasks after user interaction.                                 |

These event handlers can be attached directly to HTML elements as attributes (`on[event]`) or added dynamically using JavaScript (`element.addEventListener()`). They provide a way to respond to user interactions and other events occurring within a webpage.

## `alert`, `confirm`, and `prompt` methods in JavaScript:

| Method   | Purpose                                      | User Interaction | Returns      |
|----------|----------------------------------------------|------------------|--------------|
| `alert`  | Displays a message to the user.              | None             | Undefined    |
| `confirm`| Presents a dialog box with OK and Cancel buttons. | OK or Cancel buttons | Boolean (true if OK, false if Cancel) |
| `prompt` | Prompts the user to enter input via a text box. | Text input field | String (user input) or null if cancelled |

### Detailed Explanation:

1. **`alert`**:
   - **Purpose**: Used to display a message to the user, providing information or notifying about something.
   - **User Interaction**: No user interaction is required; it simply displays a message with an OK button.
   - **Returns**: `undefined`.

2. **`confirm`**:
   - **Purpose**: Presents a dialog box with OK and Cancel buttons, typically used for confirming an action or decision.
   - **User Interaction**: The user can click either the OK or Cancel button.
   - **Returns**: 
     - `true` if the user clicks OK.
     - `false` if the user clicks Cancel.

3. **`prompt`**:
   - **Purpose**: Prompts the user to enter input via a text box, typically used to request user input or gather information.
   - **User Interaction**: The user can enter text into a text input field provided by the prompt dialog box and then click OK or Cancel.
   - **Returns**: 
     - A string containing the text entered by the user if the user clicks OK.
     - `null` if the user clicks Cancel or closes the prompt dialog box without entering any text.

These methods are often used in web development to interact with users and gather input or provide information in a user-friendly manner.
