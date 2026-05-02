# 🎓 Student Course Management System

A full-stack web application built using **Spring Boot + JSP** to manage Students and Courses with CRUD operations.

---

## 🚀 Features

* ➕ Add Student
* 📖 View all Students
* 🔗 Assign Course to Student
* 🛠 Update Student details *(optional if implemented)*
* 🗄 Database integration using JPA (Hibernate)
* 🎨 Clean and responsive UI using JSP + CSS

---

## 🧱 Tech Stack

* **Backend:** Spring Boot, Spring MVC
* **Database:** H2 (In-Memory)
* **ORM:** Spring Data JPA (Hibernate)
* **Frontend:** JSP (Jakarta), HTML, CSS
* **Build Tool:** Maven

---

## 📂 Project Structure

```
Project/
├── src/
│   ├── main/
│   │   ├── java/com/example/Project/
│   │   │   ├── controller/
│   │   │   ├── service/
│   │   │   ├── repository/
│   │   │   └── entity/
│   │   ├── resources/
│   │   │   ├── application.properties
│   │   │   └── data.sql
│   │   └── webapp/
│   │       └── WEB-INF/views/
│   │           ├── index.jsp
│   │           └── addStudent.jsp
│   └── test/
├── pom.xml
└── README.md
```

---

## 🧠 Entity Relationship Design

* **Student → Course**
* Many Students can belong to one Course
* Implemented using:

```
@ManyToOne
@JoinColumn(name = "course_id")
```

---

## ⚙️ How to Run the Project

### 1. Clone Repository

```
git clone https://github.com/soleilbrulant/SPRING_WITH_JSP.git
```

### 2. Navigate to Project

```
cd Project
```

### 3. Run Application

```
mvnw.cmd spring-boot:run 
OR 
./mvnw spring-boot:run
```

### 4. Open Browser

```
http://localhost:8080
```

---

## 🧪 Sample Data

Courses are automatically inserted using `data.sql`:

* Java Programming
* Spring Boot
* Data Structures

---

## 🛠 Implementation Details

### 🔹 Create Operation

* JSP form to add student
* Controller handles form submission
* Data saved using JPA repository

### 🔹 Read Operation

* All students displayed in a table
* Course details shown using JOIN

### 🔹 Update Operation

* *(If implemented)* Edit existing student details

---

## ⚠️ Challenges Faced

### ❌ Issue 1: JSP not binding nested objects

* `${course.id}` was not properly mapped

### ❌ Issue 2: Hibernate error

```
unsaved transient instance
```

### ❌ Issue 3: NullPointerException

* Course object was null while saving

---

## ✅ Solutions

* Used `@RequestParam("courseId")` instead of nested binding
* Fetched Course manually from DB before saving
* Added validation checks to avoid null values

---

## 📸 Screenshots

*(Add these for better marks)*
w
* Add Student Form
* Student List Page
* Course Dropdown

---

## 🔗 GitHub Repository

👉 https://github.com/soleilbrulant/SPRING_WITH_JSP

---

## 👨‍💻 Author

**Shashwat Verma**

---

## 🎯 Conclusion

This project demonstrates:

* Spring Boot MVC architecture
* JPA entity relationships
* JSP form handling and data binding
* Full CRUD flow implementation

---

🔥 *This project can be extended with Edit, Delete, and REST API integration.*
