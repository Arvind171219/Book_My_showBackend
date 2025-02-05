# Book_My_Show_Backend

The **Book_My_Show_Backend** is a robust and scalable web-based application designed to facilitate movie ticket booking for users across various theaters. Built using **Spring Boot**, **Maven**, **JPA Hibernate**, and **MySQL**, the application provides a seamless and user-friendly experience for booking movie tickets, managing shows, and viewing booking history.

---

## **Features**
1. **User Authentication and Authorization**:
   - Users can register and log in to the system.
   - Role-based access control (e.g., Admin, User) ensures that only authorized users can perform specific actions.

2. **Movie and Theater Search**:
   - Users can search for movies by **name**, **genre**, or **language**.
   - Theaters can be searched by **location**, **name**, or **movie availability**.

3. **Show Management**:
   - Admins can add, update, or delete shows for specific movies and theaters.
   - Users can view available shows for a selected movie and theater.

4. **Seat Booking**:
   - Users can view a list of available seats for a selected show.
   - The application highlights selected seats and updates seat availability in real-time.
   - Seats are categorized (e.g., Premium, Standard) with different pricing.

5. **Ticket Booking**:
   - Users can book tickets by selecting a movie, theater, showtime, and seats.
   - The system calculates the total cost based on the number of seats and their categories.
   - Once booked, the user receives a confirmation email with booking details.

6. **Booking History**:
   - Users can view their past bookings, including details like movie name, theater, showtime, seats, and total cost.

7. **Admin Panel**:
   - Admins can manage movies, theaters, shows, and user accounts.
   - Admins can view all bookings and generate reports.

8. **Swagger UI for API Testing**:
   - Developers can test all API endpoints using Swagger UI, which provides a user-friendly interface for sending requests and viewing responses.

9. **Email Notifications**:
   - Users receive confirmation emails after successful bookings.
   - Reminder emails are sent before the showtime.

---

## **Technologies Used**
- **Spring Boot**: Backend framework for building RESTful APIs.
- **Maven**: Dependency management and build automation.
- **JPA Hibernate**: ORM tool for database interaction.
- **MySQL**: Relational database for storing application data.
- **Swagger UI**: API documentation and testing.
- **Email Configuration**: For sending confirmation and reminder emails.

---

## **Database Schema**
The database schema is designed to efficiently manage users, movies, theaters, shows, seats, and bookings. Below is a visual representation of the schema:

![Database Schema](https://user-images.githubusercontent.com/55325380/219963429-39e090b6-2842-4ed1-a383-1a07314e7fd1.jpg)

---

## **API Documentation**
The application features a **Swagger UI** for API documentation and testing. You can access the Swagger UI at:  
[Swagger UI](http://localhost:8080/swagger-ui/index.html#/ticket-controller/bookTicket)

### **API Endpoints**
1. **User Controller API**:
   - Register, login, and manage user profiles.
   ![UserControllerAPI](https://user-images.githubusercontent.com/55325380/219962891-7b73478c-89ea-47f5-813d-d51ee74409bb.jpg)

2. **Ticket Controller API**:
   - Book tickets, view booking history, and cancel bookings.
   ![TicketControllerAPI](https://user-images.githubusercontent.com/55325380/219963094-7763a420-9c17-4165-ad88-cf9cfeab6df1.jpg)

3. **Theater Controller API**:
   - Manage theaters, add new theaters, and update theater details.
   ![TheaterControllerAPI](https://user-images.githubusercontent.com/55325380/219963537-1015e21a-c471-4466-987a-185d1b56ce47.jpg)

4. **Movie Controller API**:
   - Add, update, delete, and search for movies.
   ![MovieControllerAPI](https://user-images.githubusercontent.com/55325380/219963585-18276ea7-d735-48e1-ba8e-da316d9cfe4f.jpg)

5. **Show Controller API**:
   - Manage shows, add new shows, and update show details.
   ![ShowControllerAPI](https://user-images.githubusercontent.com/55325380/219963694-62a1536f-bb9e-4723-b551-2a387c246b9c.jpg)

---

## **Database Screenshots**
Below are screenshots of the MySQL database tables:

1. **User Table**:
   ![User Table](https://user-images.githubusercontent.com/74968170/223021935-26ccb57a-b5a1-4e2d-b5fc-78115bb2b9ca.png)

2. **Movie Table**:
   ![Movie Table](https://user-images.githubusercontent.com/74968170/223022016-cf03407c-b447-4296-ae6d-de7e9c96e913.png)

3. **Theater Table**:
   ![Theater Table](https://user-images.githubusercontent.com/74968170/223022073-aeb7f9e5-6738-4341-b53e-cf423d11d80c.png)

4. **Booking Table**:
   ![Booking Table](https://user-images.githubusercontent.com/74968170/223022311-74608203-c5a2-454b-9241-19fe8c0b3922.png)

---

## **Email Confirmation**
After a successful booking, users receive a confirmation email with their booking details. Below is a sample email confirmation:

![Email Confirmation](https://user-images.githubusercontent.com/74968170/223022869-234de197-00c1-47b4-9080-c43ab550039c.png)

---

## **How to Run the Project**
1. **Prerequisites**:
   - Java JDK 11 or higher.
   - MySQL Server installed and running.
   - Maven installed.

2. **Steps**:
   - Clone the repository:
     ```bash
     git clone https://github.com/Arvind171219/Book_My_Show_Backend.git
     ```
   - Navigate to the project directory:
     ```bash
     cd Book_My_Show_Backend
     ```
   - Update the `application.properties` file with your MySQL credentials:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/bookmyshow
     spring.datasource.username=your-username
     spring.datasource.password=your-password
     ```
   - Build the project using Maven:
     ```bash
     mvn clean install
     ```
   - Run the application:
     ```bash
     mvn spring-boot:run
     ```
   - Access the application at `http://localhost:8080`.

---

## **Future Enhancements**
1. Integration with payment gateways for online payments.
2. Implementation of a recommendation system to suggest movies based on user preferences.
3. Addition of a rating and review system for movies and theaters.
4. Mobile app development using the same backend APIs.
5. Integration with third-party APIs for real-time movie updates and trailers.

---

## **Contributors**
- [Arvind Kumar](https://github.com/Arvind171219)

## **Acknowledgments**
- Special thanks to the Spring Boot and Hibernate communities for their excellent documentation and support.
