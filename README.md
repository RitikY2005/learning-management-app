# Learning management platform(lms)

[![Live Site](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge)](https://lms-deploy-frontend.onrender.com)

Full-stack e-learning platform designed to manage courses, enable student enrollments via single platform subscription

---

## Overview

[LMS](https://lms-deploy-frontend.onrender.com) is a production-ready Learning Management System built using the MERN stack. It offers a comprehensive solution for educators to host content and for students to engage in self-paced learning. This app is a simple clone of websites like udemy and coursera .

---

---

## Screenshots

![Screenshot 3](https://lh3.googleusercontent.com/u/0/d/1KCzSzbeeXEQmCI6Ru8KAUdlDcUfEzgtf)

![Screenshot 2](https://lh3.googleusercontent.com/u/0/d/11kyCD29G9ZlByD85Xu2hvDUQ2h3GzNUT)




---



## Features

### Authentication & Profiles
* **Secure Auth:** Integrated JWT for seamless, multi-role user authentication (Admin, Student)
* **Role-Based Dashboards:** Unique interfaces tailored to user permissions—students see their progress, while instructors manage their curriculum.

### Course & Content Management
* **Multimedia Support:** Admin can upload videos 
* **Asset Hosting:** Powered by Cloudinary image and video hosting

### Enrollment & Progress
* **Subscription Management:** Secure payment gateways (Razorpay) for handling course subscription purchase



---

## Tech Stack

| Component | Technology |
| :--- | :--- |
| **Frontend** | React.js, Tailwind CSS, Redux,Axios |
| **Backend** | Node.js, Express.js, Mongoose |
| **Database** | MongoDB |
| **Security** | Express Rate Limiter, JWT |
| **Payments** | Razorpay |

---

## Project Structure

```text
MithiVerse/
├── client/   # React.js frontend
└── server/   # Node.js backend

```

---

---

## Installation and Setup
> [!NOTE]
> KEEP the .env file in the root folder

Frontend Setup

```
cd client
npm install
npm run dev
```
Frontend env variables -
```
VITE_BASE_URL=api 

```
Backend Setup

```
cd server
npm install
npm run dev
```

Backend env variables -
```
FRONTEND_URL=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
RAZORPAY_KEY_ID=
RAZORPAY_SECRET=
PORT=
MONGODB_URI=
CONTACT_US_EMAIL=
RAZORPAY_PLAN_ID=
NODE_ENV=
JWT_SECRET=
JWT_EXPIRY=
SMTP_SERVICE=
SMTP_USERNAME= 
SMTP_PASSWORD= 
SMTP_FROM_EMAIL= 

```
---
## API Endpoints

### Authentication & User
* `POST /api/v1/user/register` - Register a new user
* `POST /api/v1/user/login` - User login
* `GET /api/v1/user/logout` - Clear session cookies
* `GET /api/v1/user/me` - get current user info
* `POST /api/v1/user/reset` - send a request for password reset
* `POST /api/v1/user/reset/:resetToken` - verify the reset password
* `POST /api/v1/user/change-password` - change user password
* `PUT /api/v1/user/update/:id` - update user information

### Courses
* `GET /api/v1/courses/` - Fetch all courses
* `POST /api/v1/courses/` - Create a new course (Admin)
* `DELETE /api/v1/courses/` - delete a lecture from course  (Admin)
* `GET /api/v1/courses/:id/` - fetch lectures in a course
* `POST /api/v1/courses/:id/` - upload a video in course
* `PUT /api/v1/courses/:id/` - update course information
* `DELETE /api/v1/courses/:id/` - delete course by id

### Payments & Emails
* `GET /api/v1/payments/razorpay-key` - fetch Razorpay key
* `POST /api/v1/payments/subscribe` - purchase course subscription
* `POST /api/v1/payments/verify` - verify subscription payment
* `POST /api/v1/payments/unsubscribe` - Cancel course subscription
* `GET /api/v1/payments/` -  Fetch all payment details on platform

### Extra Routes
* `POST /api/v1/contact-us` - send contact us details
* `POST /api/v1/admin/stats/user` - get user status for admin

---



