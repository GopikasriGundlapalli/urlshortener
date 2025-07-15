# 🔗 URL Shortener — Spring Boot + HTML/CSS

![Java](https://img.shields.io/badge/Backend-SpringBoot-green.svg)
![Frontend](https://img.shields.io/badge/Frontend-HTML%2FCSS-blue.svg)
![Database](https://img.shields.io/badge/Database-MariaDB-lightgrey)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A full-stack, secure, and beautifully modern **URL Shortener** built with **Spring Boot** and **vanilla HTML/CSS*, featuring JWT authentication and user-specific URL tracking — no NPM or frontend frameworks needed.

---

## ✨ Features

- 🔐 Secure Login & Registration with JWT
- 🔗 Shorten long URLs instantly
- 📋 List user’s shortened URLs (with pagination)
- ⚡ Fast redirection using `/r/{shortUrl}`
- 💾 Database-backed (MariaDB)
- 🎨 Clean, responsive, modern UI with zero dependencies

---

## 📷 Preview

| Login / Register | User Dashboard |
|------------------|----------------|
| ![Login](https://via.placeholder.com/300x200?text=Login+Screen) | ![Dashboard](https://via.placeholder.com/300x200?text=User+Dashboard) |

---

## 🔧 Tech Stack

- **Backend:** Spring Boot (Java 17), Spring Security, Spring Data JPA
- **Frontend:** HTML5 + CSS3 (no JS frameworks)
- **Database:** MariaDB
- **Security:** JWT-based authentication
- **Other:** HikariCP, REST APIs, Pagination

---

## 🚀 Run Locally

### ✅ Prerequisites
- Java 17+
- Maven
- MariaDB

### 🔌 Backend Setup

git clone https://github.com/your-username/url-shortener.git
cd url-shortener
./mvnw spring-boot:run
  Ensure application.properties contains your database config.

🌍 Frontend Access
bash
Copy
Edit
http://localhost:8080/index.html
No Node.js, no NPM, no bundlers needed!

📡 API Endpoints
Method	Endpoint	Function
POST	/api/auth/register	Register new user
POST	/api/auth/login	Login and receive token
POST	/api/url	Shorten URL (authenticated)
GET	/api/url/user	View your shortened URLs
GET	/r/{shortUrl}	Redirect to original URL


text
Copy
Edit


+------------------------+
|      User Visits       |
|    index.html (UI)     |
+------------------------+
             |
             v
+------------------------+
|   Choose Login/Register|
+------------------------+
     |           |
     v           v
+--------+   +-----------+
| Login  |   | Register  |
+--------+   +-----------+
     |           |
     |  POST /api/auth/* (JWT)   
     v           v
+----------------------------+
| Spring Boot Backend        |
| AuthController + JwtService|
| → Generate JWT             |
+----------------------------+
             |
             v
+----------------------------+
| Store JWT in localStorage |
+----------------------------+
             |
             v
+------------------------------+
| Show URL Dashboard (form)   |
+------------------------------+
             |
             v
+-----------------------------+
| User submits long URL       |
| via POST /api/url           |
+-----------------------------+
             |
             v
+------------------------------+
| Backend (UrlService)        |
| → Validates + shortens URL  |
| → Saves with user ID in DB  |
+------------------------------+
             |
             v
+------------------------------+
| Returns short URL           |
| → Display /r/abc123         |
+------------------------------+
             |
             v
+------------------------------+
| User Dashboard Options:     |
|  → Load My URLs             |
|  → Delete a URL             |
+------------------------------+
             |
             v
+------------------------------+
| GET /api/url/user?page=0    |
| → Return paginated user URLs|
+------------------------------+
             |
             v
+------------------------------+
| DELETE /api/url/{shortUrl}  |
| → Validate ownership        |
| → Delete from DB            |
+------------------------------+
             |
             v
+------------------------------+
| Visit Short URL (/r/abc123) |
| → Redirects to long URL     |
+------------------------------+


📂 Project Structure
swift
Copy
Edit
|
📦 url-shortener/
├── src/main/java/com/example/urlshortener/
│   ├── controller/
│   ├── entity/
│   ├── dto/
│   ├── service/
│   ├── repository/
│   └── ...
└── src/main/resources/static/index.html
|
👤 Author: Gowtham Reddy
Feel free to connect or contribute!

🛡️ License
© 2025 Gowtham Reddy. No rights reserved ( JK I made the Project my self).

Simplicity, speed, and security — in one place.


---

### ✅ To Use:
- Save this content as `README.md` in your project root.
- Replace the image URLs with real screenshots (if available).
- Update the repo URL in the clone command.
