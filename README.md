# Job Portal App - Backend

This README provides an overview and setup instructions for the backend of the Job Portal application, built using the MERN stack.

## Technologies Used

The backend is built with the following technologies and packages:

- **Node.js**: The JavaScript runtime environment.
- **Express.js**: A fast, unopinionated, minimalist web framework for Node.js.
- **MongoDB**: A NoSQL database for storing application data.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js.
- **Nodemon**: A utility that monitors for any changes in your source and automatically restarts your server.
- **JSON Web Token (JWT)**: Used for secure authentication.
- **Bcrypt.js**: A library for hashing passwords.
- **Cookie Parser**: Middleware to parse cookies.
- **Dotenv**: For loading environment variables from a .env file.
- **CORS**: Middleware to enable Cross-Origin Resource Sharing.

## Features

The backend handles various functionalities including:

- **User Authentication**: Register and login users with different roles (e.g., recruiter, applicant).
- **User Profile Management**: Update user profiles, including details and profile photos.
- **Company Management**: Create, view, and manage company profiles.
- **Job Management**: Create, view, update, and delete job listings.
- **Application Management**: Handle job applications, including status updates.
- **Data Filtering and Search**: Implement logic for searching and filtering jobs and companies.
- **File Uploads**: Setup Multer for handling file uploads, such as resumes and company logos.

## Setup and Installation

Follow these steps to get the backend up and running:

### Navigate to your backend directory:
Make sure you are in the root directory of your backend project.

### Install dependencies:
Run the following command to install all the required packages listed in your package.json:

```bash
npm install
```

## Create a .env file:
Create a file named .env in your backend's root directory. This file will store your environment variables, which are crucial for the application to run correctly.

Example .env content:
```ini
FRONTEND_URL=your_frontend_url
PORT=3000
MONGO_URI=your_mongo_url
SECRET_KEY=your_secret_key
CLOUD_NAME=your_cloud_name
API_KEY=your_cloud_api
API_SECRET=your_cloud_secret
```

## Connect to MongoDB:

Ensure your MongoDB database is set up and accessible. The application connects to MongoDB using Mongoose.

### Run the backend server:

To start the backend server, use the development script defined in your package.json:

```bash
npm run dev
```
This command typically uses nodemon to automatically restart the server on code changes, facilitating development. The backend server will usually run on http://localhost:3000.

## API Endpoints

The backend exposes various API endpoints for different functionalities. You can test these endpoints using tools like Postman or Insomnia.

### User API Endpoints:

- POST /api/v1/user/register - Register a new user.
- POST /api/v1/user/login - Login a user.
- POST /api/v1/user/logout - Logout a user.
- POST /api/v1/user/profile/update - Update a user.

### Company API Endpoints:

- POST /api/v1/company/register - Register a new company.
- GET /api/v1/company/get - Get all company.
- GET /api/v1/company/get/:id - Get company with id.
- PUT /api/v1/company/update/:id - Update company details.

### Job API Endpoints:

- POST /api/v1/job/post - Post a new job.
- GET /api/v1/job/getall - Get all jobs.
- GET /api/v1/job/getadminjobs - Get admin jobs.
- GET /api/v1/job/get/:id - Get job by id.

### Application API Endpoints:

- POST /api/v1/application/apply/:id - Apply for a job.
- GET /api/v1/application/get - Get application status.
- GET /api/v1/:id/applicants - Get all applicants.
- GET /api/v1/status/:id/update - Update job status.
