# Login-signup-Page-using-php

Here's a documentation outline for the PHP signup/login code:

## Signup Page PHP Code Documentation

### Introduction
This documentation outlines the PHP code for implementing a signup functionality for user registration on a website. The code validates user inputs, checks for existing usernames, and securely stores user account information in a database.

### Code Overview
The provided PHP code handles user registration and displays success and error messages using Bootstrap alerts.

#### PHP Logic (`signup.php`)
- The code checks the request method (`POST`) to handle form submissions.
- It includes the database connection file using `include`.
- User inputs (username, password, confirm password) are collected using the `$_POST` superglobal.
- The code queries the database to check if the provided username already exists.
- If the username doesn't exist, the code checks if the passwords match and securely stores the user's account information.

#### Bootstrap Alerts
- Bootstrap alerts are used to display success and error messages based on the signup process outcome.
- Success message: Displayed when the user account is successfully created.
- Error message: Displayed when there's an error, such as an existing username or password mismatch.

#### HTML Form
- The HTML form collects user inputs (username, password, confirm password) and submits them to the server.
- The form uses Bootstrap classes for styling.











## Login Page PHP Code Documentation

Here's a breakdown of the code :

1. **PHP Logic:**
   - The code begins with PHP logic to handle the login process. It queries the database to check if the provided username exists and verifies the password using `password_verify()` function.
   - It uses sessions to maintain user login state, setting `$_SESSION['loggedin']` and `$_SESSION['username']` upon successful login.

2. **HTML Form:**
   - The HTML form collects the username and password from the user.
   - The form's action attribute points to `/loginsys/login.php`. 

3. **Bootstrap Alerts:**
   - Bootstrap alerts are used to display success and error messages. This provides a nice user interface for feedback.

4. **Bootstrap Styling:**
   - The page uses Bootstrap classes for styling elements, which helps create a visually appealing and responsive design.


5. **Security Considerations:**
   - It uses uses password_hashing() php function which uses - the bcrypt crypto algorithm
   to store passwords hashed form which enhances the security as even if database is attacked    user password wont be compromised.



###SCOPE, IMPROVEMENTS & CONSIDERATIONS

●	Client-side form validation using JavaScript to enhance user experience by providing instant feedback on invalid inputs.
●	To validate and sanitize user inputs on the server-side to prevent potential SQL injection attacks.
●	To use the PHP mail() function or a third-party email library (e.g., PHPMailer) to send a verification email.
●	Use prepared statements for database queries to further enhance security.
### Conclusion
By implementing the provided PHP code, we can create a functional user registration (signup) and login page that securely stores user account information in a database. Following the outlined steps and considering the suggested improvements will help you create a more secure and user-friendly registration process.
