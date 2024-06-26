# Ezflights :airplane:

## Desktop view
![Pc view](https://github.com/Sauvic016/Ezflights/blob/main/Pc_view.gif)
## Mobile view
![Mobile_view](https://github.com/Sauvic016/Ezflights/blob/main/mobile_view.gif)

## **[Frontend](https://github.com/Sauvic016/Ezflights-frontend)** : 
The Frontend allows flights search by making api calls to flight-search service through api gateway.Users are required to authenticate themselves , User data are stored in localstorage and managed by context api. Once the required flights are selected with no. of passengers the flight is booked and the user receives a confirmation message ,the same is then sent to his/her email address.The Frontend has debouncing on Search, pagination for flights listing page, modals for signin and signup & sucess and errors notifications.

## Backend : 
The has a microservice based architecture . It consists of several services that work together to provide a comprehensive solution. The main services are:
- Flights-search service
- Authentication service
- Booking service
- Reminder service
- API Gateway

The project uses RabbitMQ as a message queue and API calls to communicate between services. Services are deployed in AWS EC2 instance. 

### **[Flights-search service](https://github.com/Sauvic016/FlightsAndSearchService)** :mag:

This service allows users to search for flights based on the city. Additionally, it allows the admin to add, update, and delete flights, cities, and airports.

### **[Authentication service](https://github.com/Sauvic016/AuthService)** :closed_lock_with_key:

This service provides user authentication for the system. Users can sign up and sign in, and must verify themselves via email before being granted access. The admin can grant roles to other users, such as admin or airline business.This service is secure and scalable, and it uses JWT tokens for authentication.

### **[Booking service](https://github.com/Sauvic016/AirticketBookingService)** :calendar:

This service allows users to book flights and sends an immediate success email upon booking. The user also receives a reminder email 12 hours before the departure time.

### **[Reminder service](https://github.com/Sauvic016/ReminderService)** :alarm_clock:

This service checks for emails to be sent via cron and sends reminder emails to users 12 hours before the departure time. The booking service communicates with the reminder service through the message queue.

### **[API Gateway](https://github.com/Sauvic016/API_Gateway)**  ⛩️

The API Gateway manages incoming request calls to all the services. It handles all the traffic and routes the requests to the appropriate service. This service is designed to be scalable and reliable.

### **Technologies used** 👨‍💻

- Express.js
- Node.js
- ReactJs
- TailwindCss
- Cron
- RabbitMQ
- MySQL
- Sequelize
- Nodemailer
- AWS
- PM2
