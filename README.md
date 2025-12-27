# GCETCare Complaint Management System

A digital platform for engineering colleges to manage and resolve campus-related complaints efficiently.

## 🔸 Overview
This system allows students to digitally raise complaints related to hostels, classrooms, laboratories, Wi-Fi, sanitation, and infrastructure. It features role-based access for Students, Admin, and Department Staff.

## 🔹 Modules Description
1. **Student Module**: Register/Login, Submit complaints (with image & priority), Track status, Give feedback.
2. **Admin Module**: Manage users, monitor all complaints via a high-level analytics dashboard.
3. **Staff Module**: View complaints assigned to their specific department, update resolution status.

## 🔹 Technical Stack
- **Frontend**: React.js, Lucide Icons, Modern CSS (Glassmorphism).
- **Backend**: Node.js, Express.js.
- **Database**: SQLite (Relational).
- **Authentication**: JWT (JSON Web Tokens) with Bcrypt password hashing.

## 🔹 System Architecture
- **Tier 1 (UI)**: React Single Page Application.
- **Tier 2 (Logic)**: RESTful API built with Express.
- **Tier 3 (Data)**: SQLite database for persistent storage.

## 🔹 Step-by-Step Execution
1. **Backend**:
   - `cd server`
   - `npm install`
   - `node index.js` (Initializes DB and starts server on port 5000)
2. **Frontend**:
   - `cd client`
   - `npm install`
   - `npm run dev` (Starts Vite dev server)

## 🔹 Testing Strategy
To ensure system reliability, the following testing approach is recommended:
- **Unit Testing**: Test individual API endpoints using Jest or Supertest (e.g., verifying JWT rejection for invalid tokens).
- **Integration Testing**: Verify the flow from Complaint Submission -> Admin Assignment -> Resolution.
- **Frontend Testing**: Use React Testing Library to verify that role-specific components (like "Mark as Resolved" button) only appear for Staff/Admin.
- **Load Testing**: Use tools like JMeter to simulate 500+ concurrent students submitting complaints during peak hours (e.g., after a Wi-Fi outage).

## 🔹 Deployment Guide
- **Backend**: Can be deployed to Heroku, AWS EC2, or Railway. Ensure `JWT_SECRET` is set in environment variables.
- **Frontend**: Perfect for Vercel, Netlify, or AWS S3 + CloudFront.
- **Database**: Since it uses SQLite (file-based), for production, consider migrating to a hosted PostgreSQL/MySQL instance (minimal changes needed in `database.js`).

## 🔹 Admin Credentials (for Demo)
- **Email**: `admin@college.edu`
- **Password**: `admin123`

## 🔹 Real-World Impact
This system reduces the "Cycle Time" of infrastructure repair by:
1. Eliminating physical paperwork.
2. Providing automated routing to relevant departments.
3. Increasing accountability through public (status) tracking.
4. Enabling budget planning through complaint analytics (e.g., if Wi-Fi issues are frequent, it's time for a hardware upgrade).

## 🔹 Conclusion
This system digitizes the manual complaint process, increasing transparency and reducing resolution time. It provides data-driven insights for college management to improve campus infrastructure.
