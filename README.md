# codsoft_taskno.1
# Chatbot Project

## Overview
This project is a simple web-based chatbot interface where users can ask specific predefined questions and receive answers from the chatbot. It utilizes HTML, CSS, and JavaScript for the front-end implementation.

## Features
- **Interactive User Interface**: Users can type in questions and receive responses from the chatbot.
- **Predefined Responses**: The chatbot responds to specific questions with predefined answers.
- **Guidelines**: A set of example questions is provided to guide the user on what to ask.

## Installation
1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Open `index.html` in a web browser to start interacting with the chatbot.

## Usage
1. **Ask a Question**: Type your question in the input box labeled "Enter your Question?".
2. **Send the Question**: Click the "Send" button to submit your question.
3. **View the Response**: The chatbot's response will be displayed below the user's question.

## Code Explanation

### HTML
The HTML file sets up the basic structure of the chatbot interface, including sections for displaying the user's input and the chatbot's response, an input box for typing questions, and a set of example questions.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chatbot</title>
    <link rel="stylesheet" href="Style.css">
</head>
<body>
    <div class="container">
        <strong>User</strong>
        <p id="Usertxt"></p>
        <strong>ChatBot</strong>
        <p id="Chattxt"></p>
        <input type="text" placeholder="Enter your Question?" id="ChatBox" required>
        <input type="submit" value="Send" id="btn">
    </div>
    <div class="Rules">
        <h1>Questions</h1>
        <p>
            User => Hi, My name is Sagnik Dey
            <br/>
            User => How are you?
            <br/>
            User => What is the Capital of India?
            <br/>
            User => What is your Name?
        </p>
    </div>
    <script src="Script.js"></script>
</body>
</html>
```

### CSS
The CSS file styles the chatbot interface, ensuring it is visually appealing and user-friendly.

```css
body {
    background-image: url(https://www.shutterstock.com/image-vector/3d-vector-robot-chatbot-ai-600nw-2301916351.jpg);
    background-size: 100vw 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    width: 100vw;
}

.container {
    background-color: #FFAA44;
    font-family: Arial, Helvetica, sans-serif;
    color: #112A46;
    display: inline-block;
    padding: 10px;
    border-radius: 10px;
    width: 400px;
}

#ChatBox {
    width: 380px;
    height: 30px;
    border-radius: 10px;
}

#btn {
    margin-top: 20px;
    background-color: #000000;
    color: white;
    padding: 5px;
    padding-left: 12px;
    padding-right: 12px;
    font-weight: 700;
    border-radius: 10px;
}

.Rules {
    margin-top: 40px;
    background-color: white;
    padding: 25px;
    display: inline-block;
    border-radius: 10px;
    font-family: Arial, Helvetica, sans-serif;
}
```

### JavaScript
The JavaScript file handles the logic of the chatbot, including capturing user input, responding to predefined questions, and displaying the responses.

```javascript
let Usertxt = document.getElementById("Usertxt");
let Chattxt = document.getElementById("Chattxt");
let ChatBox = document.getElementById("ChatBox");
let btn = document.getElementById("btn");

btn.addEventListener("click", () => {
    let User = Usertxt.innerHTML = ChatBox.value;
    Chatting(User);
});

function Chatting(User) {
    if (User == "Hi, My name is Sagnik Dey") {
        Chattxt.innerHTML = "Hi how can I help you?";
    } else if (User == "How are you?") {
        Chattxt.innerHTML = "I am fine";
    } else if (User == "What is the Capital of India?") {
        Chattxt.innerHTML = "Delhi";
    } else if (User == "What is your Name?") {
        Chattxt.innerHTML = "My name is ChatBot";
    } else if (User == "") {
        Chattxt.innerHTML = "";
    } else {
        Chattxt.innerHTML = "Didn't get that";
    }
}
```

## Contributing
Feel free to fork this project and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License.

## Acknowledgements
- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
