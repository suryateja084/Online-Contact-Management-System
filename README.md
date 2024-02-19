# Online-Contact-Management-System

User Table

1. User_id (Primary Key) 
2. Name
3. Phone Number
4. Email

The UserController class is responsible for handling HTTP requests and responses for the user-related endpoints. It uses the UserServices class to interact with the database and perform CRUD (Create, Read, Update, Delete) operations on user data.

The @Entity annotation specifies that this class is a JPA entity and should be mapped to a database table. The @Id annotation specifies that the userId attribute is the primary key of the table and should be auto-generated.

The JpaRepository interface provides many built-in methods for CRUD operations on the entity class. Since this interface does not specify the entity class type, it is necessary to provide the UserTable entity class as a generic type argument to the JpaRepository interface.

Endpoints

1. POST /api/v1/users – Add Users
The @PostMapping annotation maps the saveUser() method to the '/api/v1/users' endpoint and expects a JSON request body containing user data. It calls the saveUser() method in the UserServices class to create a new user and returns the saved user data as a JSON response.

2. GET /api/v1/users/{id} – Get User Details
The @GetMapping annotation maps the getUserById() method to the '/api/v1/users/' endpoint and expects a user ID path variable. It calls the getUserById() method in the UserServices class to retrieve user data by ID and returns it as a JSON response.

3. PUT /api/v1/users/{id} – Update User
The @PutMapping annotation maps the updateUser() method to the '/api/v1/users/' endpoint and expects a user ID path variable and a JSON request body containing updated user data. It calls the updateUser() method in the UserServices class to update the user data and returns the updated user data as a JSON response.

4. DELETE /api/v1/users/{id} – Delete User
The @DeleteMapping annotation maps the deleteUserById() method to the '/api/v1/users/' endpoint and expects a user ID path variable. It calls the deleteUserById() method in the UserServices class to delete the user data and returns an empty response.


