# 404-NOT-FOUND-HACKORBIT-FINAL

## Full Stack Tour Feedback System with Admin Panel ✨

A complete web application for collecting tour package feedback with a secure admin dashboard. Built with **Node.js, Express, PostgreSQL, and EJS**.

## **Features** 🌟
- **User-Friendly Feedback Form** (with validation)
- **Admin Dashboard** (view all submissions)
- **Secure Authentication** (username/password protected)
- **Responsive Design** (works on mobile/desktop)

---

## **Prerequisites** 📋
1. **Node.js** (v14+)
2. **PostgreSQL** (installed and running)
3. **Git** (optional)

---

## **Setup Instructions** 🛠️

### **1. Install Dependencies**
```bash
npm install **OR** npm install express body-parser cors pg ejs
```

### **2. Start the Server**
```bash
node index.js
```
The server will run at:  
🌐 **Main Site**: [http://localhost:5000](http://localhost:5000)  
🔐 **Admin Panel**: [http://localhost:5000/admin/login](http://localhost:5000/admin/login)  

---

## **Usage Guide** 📖

### **1. Submit Feedback**
- Visit [http://localhost:5000](http://localhost:5000)
- Fill out the form and submit.

### **2. Access Admin Dashboard**
- Go to [http://localhost:5000/admin/login](http://localhost:5000/admin/login)
- **Default Credentials**:
  - **Username**: `admin`
  - **Password**: `admin123`
- View all feedback submissions in the dashboard.

### **3. Logout**
- Click **"Logout"** in the admin panel to return to the login page.

---

## **Project Structure** 📂
```
tour-feedback-system/
├── public/            # Static files (HTML, CSS, JS)
│   ├── index.html     # Feedback form
│   └── privacy.html   # Privacy Policies
├── views/             # EJS templates
│   ├── login.ejs      # Admin login page
│   └── dashboard.ejs  # Admin dashboard
├── index.js           # Backend server
├── package.json       # Dependencies need to install by step 1
└── README.md          # This file
```

---

## **License** 📜
MIT License - Free for personal and educational use.

---

## **Credits** 🙌
- Built with ❤️ by **404 NOT FOUND**
- **Tailwind CSS** for styling
- **Font Awesome** for icons

---

### **Enjoy using the Tour Feedback System!** 🚀
---
# EACH FILE DETAILS:-

## 📝 User Feedback System (index.html):

Elegant UI using Tailwind CSS and Font Awesome for modern design.

Feedback Form collects:

Full Name, Email, Phone

Selected Tour Package

Star Rating (1–5)

Optional Comments

Form Validation with JavaScript to ensure all required fields are filled.

Interactive Elements include glowing hover/click effects for buttons, inputs, and labels.

Responsive Navigation Bar for desktop and mobile views.

Admin Panel Link included for feedback management (/admin/login).

About Us & Contact Section to build trust and provide easy communication

## Privacy Policy Page (privacy.html) explains:

What data is collected

How it is used and stored

User rights (view/update/delete data)

No third-party sharing

Session-based cookies only

## 🔒 Admin Login Panel (login.ejs):
Simple and clean login form with:

▪ Username & Password input

▪ Error message handling via <%= error %> in EJS

Back button to return to the main website.

Styled with user-friendly CSS and form responsiveness.

## 📊 Admin Feedback Dashboard (dashboard.ejs):

Displays all feedback in a clean, sortable table:

ID, Name, Email, Phone

Selected Package, Star Rating (★), Comments

Timestamp of Submission

Data populated using EJS with server-side values (feedbacks[])

Logout button redirects securely via tokenized link

## 🛢️ PostgreSQL Table Schema (Database Screenshots) :

```bash
CREATE TABLE feedback (
id SERIAL PRIMARY KEY,
full_name TEXT NOT NULL,
email TEXT NOT NULL,
phone TEXT,
package TEXT NOT NULL,
rating INT NOT NULL,
comments TEXT,
submitted_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

Table Fields:

id: Auto-increment primary key

full_name, email, phone: User details

package, rating, comments: Feedback content

submitted_at: Timestamp (no timezone)

## 💻 Backend Server (index.js):
Built with: Express, EJS, body-parser, pg, and CORS

Endpoints:

POST /submit: Stores feedback in PostgreSQL

GET /admin/login: Render login page

POST /admin/login: Authenticate admin

GET /admin/dashboard: Render dashboard (auth protected)

GET /admin/logout: Invalidate session

Auth:

Token-based in-memory session (authToken)

Middleware requireAuth() to protect dashboard

DB Connection:

Configured using pg.Pool with credentials (user: postgres, db: feedback_db)

Views Directory: /views with EJS templates

Server Runs on: http://localhost:5000
