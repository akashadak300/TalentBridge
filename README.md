# TalentBridge

TalentBridge is a full-stack job portal web application designed to connect job seekers (students) and recruiters. It provides a seamless experience for users to search, apply, and manage job applications, while recruiters can post jobs, manage companies, and shortlist applicants.

## Features

### For Students
- **Signup/Login:** Register and login as a student.
- **Profile Management:** Update profile, upload resume, add skills and bio.
- **Browse Jobs:** Search and filter jobs by keyword, location, industry, and salary.
- **Apply for Jobs:** Apply for jobs directly from the portal.
- **Track Applications:** View status of applied jobs (pending, accepted, rejected).

### For Recruiters
- **Signup/Login:** Register and login as a recruiter.
- **Company Management:** Create and update company profiles.
- **Post Jobs:** Add new job postings for your company.
- **Manage Jobs:** View and filter jobs posted by you.
- **Shortlist Applicants:** View applicants for each job and update their application status.

## Tech Stack

- **Frontend:** React, Redux Toolkit, TailwindCSS, Radix UI, Sonner (notifications), Axios, Vite
- **Backend:** Node.js, Express, MongoDB (Mongoose), JWT Authentication, Multer (file uploads), Cloudinary (file storage)
- **Other:** Redux Persist, Framer Motion, Embla Carousel

## Project Structure

```
TalentBridge/
├── backend/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── index.js
│   └── package.json
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── hooks/
    │   ├── redux/
    │   ├── utils/
    │   └── main.jsx
    ├── public/
    ├── index.html
    ├── package.json
    └── tailwind.config.js
```

## How It Works

1. **Authentication:** Users can sign up as either a student or recruiter. JWT tokens are used for authentication and session management.
2. **Students:** After logging in, students can browse jobs, filter/search, view job details, and apply. They can also manage their profile and view the status of their applications.
3. **Recruiters:** Recruiters can create companies, post jobs, and view/manage applicants for each job. They can update the status of applications (accept/reject).
4. **File Uploads:** Profile photos, company logos, and resumes are uploaded using Multer and stored on Cloudinary.
5. **State Management:** Redux Toolkit is used for global state management, with Redux Persist for session persistence.

## Getting Started

### Prerequisites

- Node.js & npm
- MongoDB (local or Atlas)
- Cloudinary account (for file uploads)

### Backend Setup

1. Navigate to the `backend` folder:
   ```sh
   cd backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file with the following variables:
   ```
   MONGO_URI=your_mongodb_connection_string
   SECRET_KEY=your_jwt_secret
   CLOUD_NAME=your_cloudinary_cloud_name
   API_KEY=your_cloudinary_api_key
   API_SECRET=your_cloudinary_api_secret
   PORT=8000
   ```
4. Start the backend server:
   ```sh
   npm run dev
   ```

### Frontend Setup

1. Navigate to the `frontend` folder:
   ```sh
   cd frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the frontend development server:
   ```sh
   npm run dev
   ```
4. Open [http://localhost:5173](http://localhost:5173) in your browser.

## API Endpoints

- **User:** `/api/v1/user/register`, `/api/v1/user/login`, `/api/v1/user/logout`, `/api/v1/user/profile/update`
- **Company:** `/api/v1/company/register`, `/api/v1/company/get`, `/api/v1/company/get/:id`, `/api/v1/company/update/:id`
- **Job:** `/api/v1/job/post`, `/api/v1/job/get`, `/api/v1/job/getadminjobs`, `/api/v1/job/get/:id`
- **Application:** `/api/v1/application/apply/:id`, `/api/v1/application/get`, `/api/v1/application/:id/applicants`, `/api/v1/application/status/:id/update`

## Customization

- **UI:** TailwindCSS and Radix UI components for easy customization.
- **State:** Easily extend Redux slices for new features.
- **Backend:** Modular controllers and routes for scalability.

## License

This project is licensed under the MIT License.

---

**TalentBridge** – Empowering careers,