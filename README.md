## Description

The Digital Banking Application provides functionality to manage different types of bank accounts. There are two types of accounts: Current Account and Saving Account. Each account has a unique ID and specific attributes based on its type. Current Accounts have an Overdraft attribute, while Saving Accounts have an Interest Rate attribute.

In addition to the account details, each bank account maintains a list of operations performed on it. An operation includes an ID, operation date, amount, description, and type (debit, credit, or transfer). The account history keeps track of the account balance after each operation.

Customers are registered in the system and have the following attributes: ID, name, and email address. Customers can have multiple bank accounts associated with their profile.

## Backend

The backend of the Digital Banking Application is built with Spring Boot. It provides RESTful APIs to perform various operations on bank accounts and customers. The backend architecture follows a layered approach, consisting of the following components:

### Security

The backend implements security using JWT (JSON Web Token) to ensure secure authentication and authorization. When a user logs in successfully, the backend generates a JWT token containing the user's roles (user or admin) as claims. This token is then returned to the frontend and stored securely in the browser.

### Controllers

The controllers handle incoming requests and delegate the processing to the appropriate services. They are responsible for mapping API endpoints and validating request parameters.

### Services

The services contain the business logic of the application. They handle the core functionality, such as creating bank accounts, performing operations, retrieving account details, and managing customer information.

### Repositories

The repositories interact with the database to perform CRUD (Create, Read, Update, Delete) operations. They provide an abstraction layer between the application and the underlying data storage.

### Entities

The entities represent the domain objects of the application. They are mapped to database tables and define the structure of the data.

### Data Transfer Objects (DTOs)

DTOs are used to transfer data between the backend and frontend. They encapsulate the necessary information and provide a structured representation of the data.

## Frontend

The frontend of the Digital Banking Application is developed using Angular. It provides a user-friendly interface for interacting with the application.

### Security

In the frontend, the JWT token received from the backend is securely stored in the browser, either in local storage or session storage. Angular route guards are implemented to control access to different routes based on user roles. The route guards check for the presence of a valid JWT token and the required role before allowing access to specific routes. An HTTP interceptor is set up to automatically attach the JWT token to outgoing API requests, ensuring that only authenticated and authorized users can access protected backend routes.

### Components

Components are responsible for rendering the user interface and handling user interactions. They encapsulate specific functionalities and can be reused across different pages.

### Services

Services in the frontend handle communication with the backend APIs. They make HTTP requests to fetch data and update the user interface accordingly.

### Models

Models represent the data structures used in the frontend. They mirror the backend DTOs and provide a consistent data format for the application.

![Screenshot 2024-06-23 013216](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/c9c0dc36-6a3c-47ad-b763-3af22bb47bff)

![Screenshot 2024-06-23 013409](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/68fff97f-c8de-4bb2-90bd-b4663767a833)

![Screenshot 2024-06-23 013229](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/487ff112-f4b8-47d7-8bce-f1f34b77dfdd)

![Screenshot 2024-06-23 013135](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/936d4b15-f302-4b4c-91bb-83f5dc99c3dd)
![Screenshot 2024-06-23 013421](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/1a42ec17-c47d-4b61-a9c7-44caa91bafc8)


![Screenshot 2024-06-23 013315](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/4b08541b-4820-4cf6-9755-f69947fd280d)

![Screenshot 2024-06-23 013330](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/a704b75f-9409-4f1d-840f-38cd8961536a)

![Screenshot 2024-06-23 013247](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/6a6072ae-cfbd-415c-9262-007a7919ca22)


![Screenshot 2024-06-23 013342](https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/54e1d3af-ddc4-4a0f-aa72-5cdd42684921)





https://github.com/SoufianeChahir/DigitalBanking/assets/165385691/f5d28173-301b-4d22-b3da-aa7a6a7a7634

