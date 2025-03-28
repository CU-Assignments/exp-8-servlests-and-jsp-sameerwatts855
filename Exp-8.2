import java.io.*;
 import java.sql.*;
 import javax.servlet.*;
 import javax.servlet.http.*;
 
 public class EmployeeManagementServlet extends HttpServlet {
     // Database connection configuration
     private static final String DB_URL = "jdbc:mysql://localhost:3306/employeedb";
     private static final String DB_USER = "root";
     private static final String DB_PASSWORD = "password";
 
     // Handling GET request to display employee list and search form
     protected void doGet(HttpServletRequest request, HttpServletResponse response) 
             throws ServletException, IOException {
         response.setContentType("text/html");
         PrintWriter out = response.getWriter();
 
         out.println("<!DOCTYPE html>");
         out.println("<html>");
         out.println("<head>");
         out.println("<title>Employee Management</title>");
         out.println("<style>");
         out.println("table { border-collapse: collapse; width: 100%; }");
         out.println("table, th, td { border: 1px solid black; padding: 5px; }");
         out.println("</style>");
         out.println("</head>");
         out.println("<body>");
         out.println("<h2>Employee Management System</h2>");
 
         // Employee Search Form
         out.println("<h3>Search Employee by ID</h3>");
         out.println("<form action='EmployeeManagementServlet' method='post'>");
         out.println("Employee ID: <input type='text' name='employeeId'>");
         out.println("<input type='submit' value='Search'>");
         out.println("</form>");
 
         // Display All Employees
         try {
             // Load JDBC driver
             Class.forName("com.mysql.jdbc.Driver");
             
             // Establish database connection
             Connection conn = DriverManager.getConnection(DB_URL, DB_USER, DB_PASSWORD);
             
             // Create statement to fetch all employees
             Statement stmt = conn.createStatement();
             ResultSet rs = stmt.executeQuery("SELECT * FROM employees");
 
             out.println("<h3>Employee List</h3>");
             out.println("<table>");
             out.println("<tr><th>ID</th><th>Name</th><th>Department</th><th>Salary</th></tr>");
 
             // Iterate through result set and display employees
             while (rs.next()) {
                 out.println("<tr>");
                 out.println("<td>" + rs.getInt("id") + "</td>");
                 out.println("<td>" + rs.getString("name") + "</td>");
                 out.println("<td>" + rs.getString("department") + "</td>");
                 out.println("<td>$" + rs.getDouble("salary") + "</td>");
                 out.println("</tr>");
             }
 
             out.println("</table>");
 
             // Close database resources
             rs.close();
             stmt.close();
             conn.close();
 
         } catch (ClassNotFoundException e) {
             out.println("<p>JDBC Driver not found: " + e.getMessage() + "</p>");
         } catch (SQLException e) {
             out.println("<p>Database Error: " + e.getMessage() + "</p>");
         }
 
         out.println("</body>");
         out.println("</html>");
     }
 
     // Handling POST request to search employee by ID
     protected void doPost(HttpServletRequest request, HttpServletResponse response) 
             throws ServletException, IOException {
         response.setContentType("text/html");
         PrintWriter out = response.getWriter();
 
         // Get employee ID from search form
         String employeeId = request.getParameter("employeeId");
 
         out.println("<!DOCTYPE html>");
         out.println("<html>");
         out.println("<head>");
         out.println("<title>Employee Search Result</title>");
         out.println("<style>");
         out.println("table { border-collapse: collapse; width: 50%; }");
         out.println("table, th, td { border: 1px solid black; padding: 5px; }");
         out.println("</style>");
         out.println("</head>");
         out.println("<body>");
         out.println("<h2>Employee Search Result</h2>");
 
         try {
             // Load JDBC driver
             Class.forName("com.mysql.jdbc.Driver");
             
             // Establish database connection
             Connection conn = DriverManager.getConnection(DB_URL, DB_USER, DB_PASSWORD);
             
             // Prepare statement to search employee by ID
             PreparedStatement pstmt = conn.prepareStatement("SELECT * FROM employees WHERE id = ?");
             pstmt.setInt(1, Integer.parseInt(employeeId));
 
             // Execute query
             ResultSet rs = pstmt.executeQuery();
 
             if (rs.next()) {
                 out.println("<table>");
                 out.println("<tr><th>Detail</th><th>Information</th></tr>");
                 out.println("<tr><td>ID</td><td>" + rs.getInt("id") + "</td></tr>");
                 out.println("<tr><td>Name</td><td>" + rs.getString("name") + "</td></tr>");
                 out.println("<tr><td>Department</td><td>" + rs.getString("department") + "</td></tr>");
                 out.println("<tr><td>Salary</td><td>$" + rs.getDouble("salary") + "</td></tr>");
                 out.println("</table>");
             } else {
                 out.println("<p>No employee found with ID: " + employeeId + "</p>");
             }
 
             // Add link to go back to employee list
             out.println("<br><a href='EmployeeManagementServlet'>Back to Employee List</a>");
 
             // Close database resources
             rs.close();
             pstmt.close();
             conn.close();
 
         } catch (ClassNotFoundException e) {
             out.println("<p>JDBC Driver not found: " + e.getMessage() + "</p>");
         } catch (SQLException e) {
             out.println("<p>Database Error: " + e.getMessage() + "</p>");
         } catch (NumberFormatException e) {
             out.println("<p>Invalid Employee ID: " + employeeId + "</p>");
         }
 
         out.println("</body>");
         out.println("</html>");
     }
 }
