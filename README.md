# Project Management Application

![Project Management Application Logo](https://pm-s3-images1234.s3.eu-north-1.amazonaws.com/Screenshot+2025-03-11+at+4.45.01%E2%80%AFPM.png)

This is a full-stack project management application built with Next.js for the client side and Express.js for the server side. The application utilizes AWS services for authentication, storage, and deployment.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Environment Variables Setup](#environment-variables-setup)
- [Client Side](#client-side)
- [Server Side](#server-side)
- [Deployment](#deployment)

## Features

-   **User Authentication**: Utilizes AWS Cognito for secure user authentication.
-   **Image Storage**: Uses AWS S3 for storing user profile images and other media.
-   **Drag and Drop Functionality**: Implemented for task management, allowing users to easily organize tasks.
-   **Responsive Design**: The application is designed to be fully responsive, providing a seamless experience on both desktop and mobile devices.
-   **Real-time Updates**: Leveraging Redux Toolkit for state management, ensuring that the UI updates in real-time as data changes.

## Technologies Used

-   **Frontend**:
    -   Next.js
    -   React
    -   Redux Toolkit
    -   Tailwind CSS
    -   Lucide Icons
-   **Backend**:
    -   Node.js
    -   Express.js
    -   Prisma ORM
    -   PostgreSQL (hosted on AWS RDS)
-   **AWS Services**:
    -   AWS Cognito for authentication
    -   AWS S3 for image storage
    -   AWS EC2 for hosting the server
    -   AWS RDS for database hosting.

## Getting Started

To get started with this project, follow these steps:

1.  **Clone the Repository**:

    ```bash
    git clone [https://github.com/subhpaul123/project-managemeent.git](https://github.com/subhpaul123/project-managemeent.git)
    cd project-managemeent
    ```

2.  **Install Dependencies**:

    For both the client and server, run the following command:

    ```bash
    npm install
    ```

## Environment Variables Setup

Before running the application, you need to set up environment variables for both the client and server.

**Client Side (`client/.env`)**:

Create a `.env` file in the `client` directory and add the following variables:

* `NEXT_PUBLIC_API_BASE_URL=http://localhost:8000`
* `NEXT_PUBLIC_COGNITO_USER_POOL_ID="your user pool id here"`
* `NEXT_PUBLIC_COGNITO_USER_POOL_CLIENT_ID="your client id here"`



Replace `"your user pool id here"` and `"your client id here"` with your actual AWS Cognito User Pool ID and Client ID.

**Server Side (`server/.env`)**:

Create a `.env` file in the `server` directory and add the following variables:

* `PORT=8000`
* `DATABASE_URL="your database url here"`

Replace `"your database url here"` with your actual PostgreSQL database URL.

## Client Side

To run the client side of the application, navigate to the `client` directory and start the development server:

```bash
cd client
npm run dev
```

Open your browser and go to http://localhost:3000 to view the application.

### Server Side
To run the server side of the application, navigate to the server directory and start the development server:

```bash
cd server
npm run dev
```

The server will run on http://localhost:8000 (or the port specified in your .env file).

### Deployment
The application is deployed using AWS Amplify, which provides a seamless CI/CD pipeline for the frontend. The backend is hosted on AWS EC2, and the database is hosted on AWS RDS, ensuring scalability and reliability.

### Conclusion
This project management application is designed to help teams manage their projects efficiently. With features like user authentication, drag-and-drop task management, and real-time updates, it provides a robust solution for project management needs.
