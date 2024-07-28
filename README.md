## Flight Status and Notifications System

This repository contains a full-stack application for providing real-time flight status updates and notifications to passengers. It includes a Vite React frontend with Tailwind CSS for styling and a Node.js backend.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Setup Instructions](#setup-instructions)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Running the Application](#running-the-application)
- [Environment Variables](#environment-variables)
- [License](#license)

## Features

- *Real-time Updates*: Display current flight status (delays, cancellations, gate changes).
- *Push Notifications*: Send notifications for flight status changes via SMS, email, or app notifications.
- *Integration with Airport Systems*: Pull data from airport databases for accurate information.

## Technologies

- *Frontend*: Vite, React.js, HTML, CSS, Tailwind CSS
- *Backend*: Node.js, Express.js
- *Database*: MongoDB
- *Notifications*: Kafka, Nodemailer (for email notifications)

## Setup Instructions

### Backend Setup

1. *Clone the repository*:

    bash
    git clone https://github.com/Ayushkaushik9977/Indigo_hack_2_hire.git
   
    cd Indigo_hack_2_hire/server
    

3. *Install dependencies*:

    bash
    npm install
    

4. *Configure environment variables*:

    Create a .env file in the server directory with the following variables:

    plaintext
    PORT=8080
    MONGODB_URI=your_mongodb_uri
    KAFKA_USERNAME=your_kafka_username
    KAFKA_PASSWORD=your_kafka_password
    EMAIL_USER=your_email@example.com
    EMAIL_PASS=your_email_password
    

5. *Start the server*:

    bash
    npm start
    

### Frontend Setup

1. *Navigate to the client folder*:

    bash
    cd ../client
    

2. *Install dependencies*:

    bash
    npm install
    

3. *Install Tailwind CSS*:

    bash
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init -p
    

4. *Configure Tailwind CSS*:
   
    Update the tailwind.config.js file to include the paths to your template files:
    javascript
    module.exports = {
      content: [
        "./index.html",
        "./src/**/*.{js,ts,jsx,tsx}",
      ],
      theme: {
        extend: {},
      },
      plugins: [],
    }
    

5. *Add Tailwind CSS Directives*:
   
    Add the Tailwind directives to your src/index.css file:
    css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    

6. *Start the Vite development server*:

    bash
    npm run dev
    

## Running the Application

1. *Start the Backend*:

    Navigate to the server folder and start the server:

    bash
    cd server
    npm start
    

2. *Start the Frontend*:

    Navigate to the client folder and start the Vite development server:

    bash
    cd ../client
    npm run dev
    

3. *Access the Application*:

    Open your browser and navigate to http://localhost:3000 to see the frontend, and the backend will be running on http://localhost:8080.

## Environment Variables

The application uses the following environment variables:

- *Backend*:
  - PORT: Port on which the backend server runs.
  - MONGODB_URI: MongoDB connection URI.
  - KAFKA_USERNAME: Kafka username for authentication.
  - KAFKA_PASSWORD: Kafka password for authentication.
  - EMAIL_USER: Email address for sending notifications.
  - EMAIL_PASS: Password for the email address.

- *Frontend*:
  - No specific environment variables are required for the frontend by default.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
