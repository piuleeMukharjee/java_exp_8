🚀 Project Readme

This repository contains a set of Java Servlets, JSP, and HTML files demonstrating basic web application development using Servlets, JSP, and JDBC for database interaction.

📁 File Structure & Purpose
File	Type	Description
AttendanceServlet.java	Servlet	Handles form submission from attendance.jsp and inserts student attendance data (StudentID, Date, Status) into the Attendance table in the studentdb database.
attendance.jsp	JSP	A simple form for users to input Student ID, Date, and Attendance Status (Present/Absent). The form posts data to AttendanceServlet.
EmployeeServlet.java	Servlet	Handles requests from employee.html to fetch and display employee records from the Employee table in the companydb database. Supports searching by EmpID or viewing all employees.
employee.html	HTML	A form providing options to search for an employee by ID or view all employees. The form submits data to EmployeeServlet.
LoginServlet.java	Servlet	Handles form submission from login.html and performs simple hardcoded login validation (Username: admin, Password: 12345).
login.html	HTML	A basic login form that posts credentials to LoginServlet.
database.sql	SQL	Script to create the studentdb database and the Attendance table used by AttendanceServlet.
⚙️ Setup and Configuration
🗄️ Database Setup

Execute the commands in database.sql using your MySQL console to create the studentdb database and Attendance table.

The EmployeeServlet requires a separate database named companydb with an Employee table containing:

EmpID (INT, Primary Key)
Name (VARCHAR)
Salary (DECIMAL)


👉 You will need to create this manually.

🧩 JDBC Driver

Ensure the MySQL Connector/J library (JDBC driver) is included in your web application's classpath (usually in WEB-INF/lib).

🔑 Servlet Credentials

In AttendanceServlet.java and EmployeeServlet.java, update your MySQL credentials:

private static final String JDBC_PASS = "your_password"; // 🔹 Replace with your actual MySQL root password

🌐 Deployment

Deploy the project (Servlets, JSPs, and HTML files) on a Java web server such as Apache Tomcat.

Ensure the project is correctly configured in your web.xml or using annotations (@WebServlet).

🔗 Access Points

Once deployed, you can access the application at:

Feature	URL Path
Attendance Form	/your-app-context/attendance.jsp
Employee Search	/your-app-context/employee.html
Login Page	/your-app-context/login.html
