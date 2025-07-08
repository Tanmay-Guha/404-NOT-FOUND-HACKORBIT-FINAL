# 404-NOT-FOUND-HACKORBIT-FINAL

## Full Stack Tour Feedback System with Admin Panel ✨

A complete web application for collecting tour package feedback with a secure admin dashboard.

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

## 🛢️ PostgreSQL Table Schema:

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

# NEXT DAY PLAN:-
IMPLEMENT BACKEND

MAKE CONNECTION BETWEEN FRONTEND-BACKEND-DATABASE

INSTALL DEPENDENCIES

RUN FULL PROJECT

CHECK FULL WORKING PROCESS

FINAL README UPDATE
