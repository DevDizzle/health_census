# User Information Collection Form

## Project Overview

In this practice project, you will discover how to design a structured form to collect diverse user information such as name, age, email, job, and product feedback. You will see how to use JavaScript functions to manage form submission, capture input values, and dynamically display user-provided feedback on the webpage. You will also observe event handling mechanisms.

## Features

- **Structured Form**: Collect user information including name, age, email, job, and product feedback.
- **Form Submission Management**: Handle form submissions using JavaScript.
- **Input Value Capture**: Capture input values provided by users.
- **Dynamic Feedback Display**: Display user-provided feedback dynamically on the webpage.
- **Event Handling**: Implement event handling mechanisms to improve user interaction.

## Technologies Used

- HTML
- CSS
- JavaScript

## Getting Started

### Prerequisites

To run this project, you need a web browser and a code editor.

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/user-info-collection-form.git
    ```

2. Navigate to the project directory:

    ```sh
    cd user-info-collection-form
    ```

## Usage

1. Open the `index.html` file in your web browser to see the form.
2. Fill in the form fields and submit the form.
3. Observe the captured input values and the dynamically displayed feedback.

## Code Explanation

### HTML

The HTML file contains the structure of the form with fields for name, age, email, job, and product feedback.

### CSS

The CSS file provides basic styling for the form to make it visually appealing.

### JavaScript

The JavaScript file includes functions to:

- Manage form submissions.
- Capture input values.
- Display user-provided feedback dynamically.
- Handle events for better user interaction.

### Example JavaScript Functions

#### Form Submission Handler

```javascript
document.getElementById('feedbackForm').addEventListener('submit', function(event) {
    event.preventDefault();
    captureInputValues();
});

function captureInputValues() {
    const name = document.getElementById('name').value;
    const age = document.getElementById('age').value;
    const email = document.getElementById('email').value;
    const job = document.getElementById('job').value;
    const feedback = document.getElementById('feedback').value;
    
    displayFeedback(name, age, email, job, feedback);
}

function displayFeedback(name, age, email, job, feedback) {
    const feedbackDisplay = document.getElementById('feedbackDisplay');
    feedbackDisplay.innerHTML = `
        <p><strong>Name:</strong> ${name}</p>
        <p><strong>Age:</strong> ${age}</p>
        <p><strong>Email:</strong> ${email}</p>
        <p><strong>Job:</strong> ${job}</p>
        <p><strong>Feedback:</strong> ${feedback}</p>
    `;
}
