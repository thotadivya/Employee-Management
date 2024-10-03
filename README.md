# Employee Management System (Java, Spring Boot)

## Project Overview
This Employee Management System (EMS) is a Java-based web application built using Spring Boot for backend operations. The system allows users to perform CRUD (Create, Read, Update, Delete) operations on employees' data, which is stored in memory using a list. It includes features for adding new employees, updating employee details, viewing employee lists, and deleting employee records.

The application follows a modular approach, where each functionality is separated into different classes for better organization, maintainability, and scalability.

## Features

### Add New Employee:
- Allows users to add a new employee by providing details such as employee ID, first name, last name, email, and title.
- The employee data is stored in an in-memory list during the runtime of the application.

### View Employee List:
- Users can view the complete list of employees stored in memory.
- The system retrieves employee data and displays it in a tabular format.

### Update Employee Details:
- Allows users to update an existing employee’s information (e.g., name, email, title).
- The system checks if the employee ID exists and updates the relevant data in the in-memory list.

### Delete Employee:
- Users can delete an employee record by providing the employee's ID.
- The system verifies if the employee exists and deletes the entry from the in-memory list.

## Technologies Used
- **Java**: The core programming language used for business logic and handling requests.
- **Spring Boot**: Java framework used for building the backend API with features like dependency injection and RESTful services.
- **HTML, JavaScript**: Used for frontend development to interact with the backend API.
- **Bootstrap**: Frontend framework for designing responsive pages.
- **Postman**: Tool used for testing API endpoints.

## Application Flow

### Start the Application:
- The application starts with an in-memory list of employees.
- The main page displays the employee management homepage with options to view, add, update, and delete employees.

### User Interactions:
- Users can interact with the system through the frontend pages. Buttons on the UI trigger actions like viewing the employee list, adding a new employee, or deleting an employee record.
- RESTful endpoints handle user requests, and data is sent/received in JSON format.

### Data Storage:
- The application uses an in-memory `ArrayList` to store employee data. Each operation updates this list.
- When the application is restarted, the data is reset as it is not persisted in a database.

### Result Handling:
- After each operation (e.g., adding or updating an employee), the user receives a success or failure message. These messages are displayed either in the UI or as API responses (when tested via Postman).

## Code Structure

### `EmployeeManagementApplication.java`:
- Entry point of the application. It sets up Spring Boot and initializes the entire system.

### `Employee.java`:
- This is the model class that represents the employee entity. It contains fields like `employee_id`, `first_name`, `last_name`, `email`, and `title`.

### `EmployeeController.java`:
- This class handles all the HTTP requests (GET, POST, PUT, DELETE). It provides endpoints for managing employee data such as viewing, adding, updating, and deleting employees.

### `EmployeeService.java`:
- This class contains the business logic for the system. It defines methods for retrieving, creating, updating, and deleting employees.

### `Employees.java`:
- This class stores the employee data in an in-memory list. It provides methods to access and manipulate the employee list.

## Setup Instructions

To set up and run the Employee Management System on your local machine, follow the steps below:

### Prerequisites
- Java Development Kit (JDK) 8 or later
- Maven
- IDE (e.g., IntelliJ IDEA, Eclipse)
- Postman (for API testing)

### Steps to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/employee-management-system.git
   cd employee-management-system
2. **Build and Run the Application:**:
   Using Maven 
   mvn clean install
   mvn spring-boot:run
3. **Access the Application:**:
   Open the browser and navigate to http://localhost:8080.
   Use Postman to test the API endpoints, or navigate through the frontend.
