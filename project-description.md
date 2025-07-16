# Test Project Outline – Module B – Restaurant Owners' Hub

## Competition time

4 hours

## Introduction

**DineEase**, a small startup based in Hungary, initially made waves in the restaurant industry with their innovative restaurant software. Now, they are expanding their horizons with a brand new service that aims to revolutionize how people discover, explore, and engage with restaurants. Introducing DineEase, the all-in-one portal and progressive web application designed to enhance the dining experience. Visitors can choose between restaurants, view the full menu of any restaurant, read reviews from previous guests about the restaurant service and food. They can also book a table at the restaurant of their choice and order and pay through the website or the app.

## General Description of Project and Tasks

In this module you will develop a server-side rendered administration page where restaurant owners can easily manage their restaurant profiles and data. This hub empowers restaurant owners to update menus, respond to reviews, and keep their information up-to-date, ensuring a seamless and engaging experience for customers.

Choose a suitable server-side framework from the available options in the provided Infrastructure List. Carefully review the provided detailed description of the dynamic website's account management functionalities. Understand the various tasks and actions that users need to perform within their accounts.

## Requirements

The goal of this project is to create a comprehensive restaurant management system that enables restaurant owners to efficiently manage their business operations through a secure, server-side rendered web application. The system must support user authentication, role-based access control, and provide intuitive interfaces for managing restaurant data, menus, reservations, and customer reviews.

### Database Design

Design a robust and efficient database schema to accommodate user accounts and related data.
Identify the necessary tables, relationships, and fields required for account management.
Ensure proper normalization and data integrity in the database design.
Utilize the provided example CSV files to import initial data into the database. CSV files can be found in the assets/module-B/initial-data folder.
Develop a script or mechanism to parse and import CSV data into relevant database tables.
Address any data normalization challenges that may arise from the provided CSV data.

### User Authentication and Security

- Implement a secure user authentication system to enable users to create and access accounts.
  Utilize encryption and hashing techniques to store and manage user passwords securely. Implement account locking mechanisms to enhance account security.
- Design a system that supports two user roles: "dineEasyAdmin" and "restaurantAdmin". DineEasy admins will have access to the entire system, while restaurant administrators will have access only to their respective restaurant's data.
- Develop a user registration mechanism for restaurant administrator roles. Capture essential information, including email address (as username), password, name, restaurant name, type and location. Implement appropriate validation for email address field. Enable the uploading of image for restaurant logo.
- Create a login form that authenticates users based on their role. Administrators should be redirected to the admin dashboard, while restaurant administrators should be directed to their respective restaurant's dashboard upon successful login.
- Implement a mechanism to lock user accounts after three failed login attempts. Determine 30 seconds duration for which the account should be locked out. Users should be notified about the account lockout and provided with information about the lock out duration.
- Configure protected routes that are accessible only after successful user authentication. Implement role-based access control to restrict certain actions to authorized users. Ensure that sensitive account information is accessible only to the respective account owner and dineEasy admins.
- Create two sample user for both roles:

| email                    | name        | role            | restaurantId | password |
| ------------------------ | ----------- | --------------- | ------------ | -------- |
| ferenc.kis@sze.hu        | Ferenc Kis  | restaurantAdmin | 1            | 12345678 |
| laszlo.nagy@dineeasy.com | Laszlo Nagy | dineEasyAdmin   |              | 12345678 |

- When the authenticated user click on the Logout link they will be logged out and redirected to the login page.

### Restaurant Dashboard

Create user-friendly interfaces where restaurant admin user can view and edit their respective restaurant's data.
Follow the provided wireframe in implementing the dashboard. All the subpages of the dashboard should contain a "Back to the dahboard" and a "Logout" link.

#### Edit Profile
When the restaurant admin click on the "Edit profile" button they will be redirected to the Edit profile page. On that page all the profile data can be modified and saved.

#### Menu Management
Design the interface for restaurant owners to manage their menus.
Implement CRUD operations for menu items, including adding, updating, and deleting dishes.
Allow the inclusion of dish names and prices.

#### Reservation Handling
It will be the page for a reservation system with the following features:
- Restaurant owners can manage incoming reservations
- Displaying a list of reservations with relevant details like date, time, party size, and contact information
- Enable the confirmation or cancellation of reservations

#### Review Management
Implement a feature for restaurant owners to manage customer reviews.
Display customer feedback along with ratings and comments.
In the near future the page will also allow restaurant owners to post thoughtful responses to reviews, but you do not need to implement this feature right now.

### Security Implementation (OWASP Guidelines)

Implement security measures to protect against common web vulnerabilities (OWASP guidelines).
Sanitize and validate user inputs to prevent SQL injection and cross-site scripting (XSS) attacks.
Implement CSRF (Cross-Site Request Forgery) protection to ensure secure form submissions.

## Assessment

The solution will be evaluated using the following methods and tools:

- **Functionality Testing**: Testing of all implemented features including user authentication, database operations, and user interfaces
- **Security Assessment**: Evaluation of security measures against common web vulnerabilities
- **Code Quality Review**: Assessment of code structure, documentation, and best practices
- **Browser Testing**: Testing across different browsers to ensure compatibility
- **Database Design Review**: Evaluation of database schema design and data integrity

## Mark distribution

| WSOS SECTION | Description                            | Points |
|--------------|----------------------------------------|--------|
| 1            | Work organization and self-management  | 3      |
| 2            | Communication and interpersonal skills | 2      |
| 3            | Design Implementation                  | 4      |
| 4            | Front-End Development                  | 6      |
| 5            | Back-End Development                   | 10     |
| **Total**    |                                        | **25** |
