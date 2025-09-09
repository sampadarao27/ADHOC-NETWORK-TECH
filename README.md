# ADHOC-NETWORK-TECH
JAVA FULL STACK DEVELPOMENT INTERN

Java Full-Stack Programming — Registration Project

Short-Term Internship Project
Student: Sampada Rao Laxmi (III BCA)
College: Kakinada Aditya Women’s Degree College — Dept. of BCA
Project: Registration — a simple Java Full-Stack web application (JSP / Servlets / MySQL).
(Project report and details provided in the uploaded internship document.)

Table of Contents
Project Overview
Features
Tech Stack
Project Structure
Prerequisites
Installation & Setup
Database Setup
Add Required JARs
Running the Project
Screenshots
Conclusion
Author & Acknowledgements

Project Overview

This is a short-term internship project titled "JAVA FULL STACK PROGRAMMING".
The repo contains a simple registration/login web application built using JSP, Servlets, and MySQL. It demonstrates core Java web concepts (JSP pages, Servlets, JDBC, form handling) and basic project set up in NetBeans with Tomcat and MySQL. The full internship report and details are available in the submitted document.

Features
User registration (store name, username, email, password)
User login authentication
Error page for invalid login
Sample Servlets: register and login
Simple MySQL DB integration (JDBC)
Instructional guide on setting up NetBeans, Tomcat, and MySQL included in the internship doc.

Tech Stack
Java (Servlets)
JSP (view pages)
Apache Tomcat (web server)
NetBeans IDE (project development)
MySQL (database)
JDBC (MySQL Connector)
Libraries (JARs): mysql-connector-java, cos-multipart, gson, java-mail (as used in the report).

Project Structure (example)

Registration/                 # project root
├─ src/
│  └─ Controller/
│     ├─ register.java
│     └─ login.java
├─ web/
│  ├─ index.html
│  ├─ register.jsp
│  ├─ login.jsp
│  └─ error.jsp
├─ lib/                       # add JARs here (or configure via NetBeans)
├─ README.md
└─ docs/
   └─ Internship_Report.docx  # (optional) full report

Prerequisites

Java JDK (8 or above)
NetBeans IDE (or any Java EE-capable IDE)
Apache Tomcat (7 / 8 / 9)
MySQL Server
MySQL Query Browser or Workbench (optional)
The JARs listed in Add Required JARs section.

Installation & Setup
1. Clone the repo
git clone <your-repo-url>
cd Registration
2. Open in NetBeans
File → Open Project and choose the project folder.
3. Ensure Tomcat is configured
In NetBeans: Tools → Servers → Add Apache Tomcat (if not already).
4. Configure project to use Tomcat
Right click project → Properties → Run → select Tomcat server.
5. Add required JARs (see next section).
Database Setup
Open MySQL client (or Workbench) and execute:
-- 1. Create database
CREATE DATABASE registration;
-- 2. Use database
USE registration;
-- 3. Create register table
CREATE TABLE register (
  id INT UNSIGNED NOT NULL AUTO_INCREMENT,
  fullname VARCHAR(45) NOT NULL DEFAULT '',
  username VARCHAR(45) NOT NULL DEFAULT '',
  email VARCHAR(45) NOT NULL DEFAULT '',
  password VARCHAR(45) NOT NULL DEFAULT '',
  confirmpassword VARCHAR(45) NOT NULL DEFAULT '',
  PRIMARY KEY (id)
) ENGINE=InnoDB;

To view data:
SELECT * FROM registration.register;
To delete all rows and reset auto increment:
DELETE FROM registration.register;
ALTER TABLE registration.register AUTO_INCREMENT = 1;
(DB commands and schema are taken from the internship report.)

Add Required JARs
Download and add the following jar files to your project lib/ (or add via NetBeans Libraries → Add JAR/Folder):
mysql-connector-java-5.1.23-bin.jar (or a recent MySQL connector)
cos-multipart.jar
gson-2.2.2.jar
java-mail-1.4.4.jar

> In NetBeans: Right-click Libraries → Add JAR/Folder → select downloaded jars and add them. Steps and example links are provided in the internship doc.
How to Run
1. Start MySQL server and ensure database registration exists.
2. Build the project in NetBeans (Clean and Build).
3. Run the project on Tomcat:
Right click project → Run (or Deploy).
4. Open browser and go to:
http://localhost:8080/<context-path>/index.html
5. Register new user via Register and then Login with registered credentials.

Notes & Security (Important)
Passwords are stored in plaintext in this demo. Do not use this approach for production. Use hashing (bcrypt / PBKDF2) and secure transport (HTTPS).
The project demonstrates core concepts suitable for learning and internship submissions.
For production: add input validation, prepared statements (already used), secure session management, and password hashin

Screenshots 
![adoch 2](https://github.com/user-attachments/assets/0c40ef10-f8e9-473b-82fe-16f81fba4f98)
![adhoc](https://github.com/user-attachments/assets/23779672-1213-4f98-8c3c-843bfc3dd819)

Conclusion
This short-term internship project successfully demonstrates essential Java full-stack skills (JSP, Servlets, JDBC, MySQL) and provides step-by-step setup instructions to reproduce the Registration application locally. 

Author
Sampada Rao Laxmi — III BCA
Kakinada Aditya Women's Degree college.

Acknowledgements
Thanks to the internship guide and the Adhoc Network Tech Company for resources and mentorship as mentioned in the internship report.
