# IIT Kharagpur US Trip Registration Form

This is a simple PHP-based web application for collecting participant details for the IIT Kharagpur US Trip. Participants can fill out the form with their personal information, and upon submission, the data is stored in a MySQL database.

## Prerequisites

- Web server with PHP support (e.g., Apache, Nginx)
- MySQL database

## Setup Instructions

1. **Database Configuration:**
   - Ensure that you have a MySQL database server set up.
   - Update the database connection details in the PHP script (`index.php`). Modify the following lines with your database credentials:

     ```php
     $server = "localhost";
     $username = "root";
     $password = "";
     ```

2. **Database Schema:**
   - Create a database named `trip` on your MySQL server.
   - Use the following SQL query to create the necessary table:

     ```sql
     CREATE TABLE `trip` (
         `id` INT AUTO_INCREMENT PRIMARY KEY,
         `name` VARCHAR(255) NOT NULL,
         `age` INT NOT NULL,
         `gender` VARCHAR(10) NOT NULL,
         `email` VARCHAR(255) NOT NULL,
         `phone` VARCHAR(15) NOT NULL,
         `other` TEXT,
         `dt` TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```

3. **Web Server Configuration:**
   - Make sure your web server is configured to execute PHP scripts.
   - Place the PHP script (`index.php`) and the CSS file (`style.css`) in the appropriate directory accessible by your web server.

4. **Access the Application:**
   - Open a web browser and navigate to the URL where your application is hosted.
   - For example, if hosted locally: `http://localhost/path/to/index.php`

## Styling

The application uses a simple and responsive design with CSS. The styling is defined in the `style.css` file. Feel free to customize the styles based on your preferences.

## Usage

1. Participants can fill out the form with their details, such as name, age, gender, email, phone, and additional information in the textarea.
2. Upon submitting the form, the data is inserted into the MySQL database, and a success message is displayed.
3. If there is an error during the database connection or insertion process, an error message will be shown.

## Feedback

Participants will receive a confirmation message upon successful form submission, thanking them for joining the IIT Kharagpur US Trip.

Feel free to adapt and extend this application based on your specific requirements.
