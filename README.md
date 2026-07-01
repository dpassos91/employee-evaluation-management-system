# 📈 Employee Evaluation Management System

![Java](https://img.shields.io/badge/Java-21-red)
![Jakarta EE](https://img.shields.io/badge/Jakarta_EE-10-orange)
![React](https://img.shields.io/badge/React-19-61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-blue)
![WebSockets](https://img.shields.io/badge/WebSockets-Real--Time-success)
![RBAC](https://img.shields.io/badge/RBAC-Role--Based-blueviolet)

> A full-stack employee evaluation platform built with **Java (Jakarta EE)** and **React**, designed to support performance reviews, training management and internal communication through structured business workflows.

![Dashboard](assets/Dashboard.png)

## 📌 Project Overview

This application centralises employee performance evaluations, training records and organisational workflows into a single platform.

Different user roles (administrators, managers and employees) interact through structured evaluation cycles, training management, real-time communication and configurable system settings.

## ✨ Highlights

- 🔐 Secure role-based authentication
- 📈 Complete employee evaluation workflow
- 👥 Employee lifecycle management
- 🎓 Training & course management
- 💬 Real-time chat using WebSockets
- 🔔 Live notifications
- 📄 CSV & PDF exports
- ⚙️ Configurable application settings

## 📸 Screenshots

A quick look at some of the application's main interfaces.

![Login](assets/Login.png)

![Dashboard](assets/Dashboard.png)

![Evaluation](assets/Evaluation.png)

![Employee Profile](assets/Profile.png)

## 🛠 Tech Stack

### Backend

- Java 21
- Jakarta EE 10
- JAX-RS
- JPA / Hibernate
- WebSockets
- BCrypt
- Log4j2
- Maven
- WildFly
- JUnit
- Mockito

### Frontend

- React 19
- React Router
- Zustand
- react-intl
- Tailwind CSS
- React Toastify

### Database

- PostgreSQL

## 🏗 Architecture

```text
                          React Frontend
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
   React Router              Zustand                 react-intl
   Navigation            State Management        Internationalization
        │                        │                        │
        └────────────────────────┼────────────────────────┘
                                 │
                    REST API + WebSockets
                                 │
                                 ▼
                  Jakarta EE Backend (WildFly)
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
   REST Services             WebSocket              Filters / Config
     (JAX-RS)                 Endpoint          Auth, CORS, Context
        │                        │                        │
        └────────────────────────┼────────────────────────┘
                                 │
                         Business Beans
                                 │
        ┌──────────────┬─────────┼─────────┬──────────────┐
        │              │         │         │              │
      Users       Evaluations  Courses  Messages     Notifications
        │              │         │         │              │
        └──────────────┴─────────┼─────────┴──────────────┘
                                 │
                          DAOs / DTOs
                                 │
                         JPA / Hibernate
                                 │
                                 ▼
                            PostgreSQL
```

The backend follows a layered architecture separating REST resources, business logic, persistence, configuration and real-time communication.

The frontend is organised into reusable pages, components, hooks, stores, API modules and translation files.

## 📂 Project Structure

```text
employee-evaluation-management-system/
│
├── backend/
│   ├── bean/
│   ├── config/
│   ├── dao/
│   ├── dto/
│   ├── entity/
│   ├── filter/
│   ├── service/
│   ├── util/
│   └── websocket/
│
├── frontend/
│   ├── api/
│   ├── components/
│   ├── hooks/
│   ├── pages/
│   ├── stores/
│   ├── translations/
│   ├── utils/
│   └── websocket/
│
└── README.md
```

## 🚀 Installation

### Prerequisites

- Java 21
- Maven
- PostgreSQL
- WildFly
- Node.js
- npm

### Clone the repository

```bash
git clone https://github.com/dpassos91/employee-evaluation-management-system.git
cd employee-evaluation-management-system
```

### Backend

```bash
cd backend
mvn clean package
```

Deploy the generated WAR file to WildFly and configure the datasource:

```text
java:/postgresDS
```

### Frontend

```bash
cd frontend
npm install
npm start
```

## ⭐ Technical Highlights

- Layered Jakarta EE architecture
- RESTful API design
- DTO and DAO patterns
- Role-based authorization
- Token-based authentication
- Password hashing with BCrypt
- WebSocket-based real-time communication
- Evaluation cycle management
- CSV and PDF report generation
- Zustand state management
- Internationalization with react-intl
- PostgreSQL persistence through JPA/Hibernate

## 📚 What I Learned

Building this project challenged me to model a real business domain rather than simply implementing isolated features.

Working with different user roles, evaluation workflows and training management strengthened my understanding of software architecture, domain modelling and full-stack application development using Java and React.

## 🔭 Future Improvements

- Docker support
- CI/CD with GitHub Actions
- OpenAPI / Swagger documentation
- Email notifications
- Analytics dashboard
- Cloud deployment
- Performance optimisation
- Expanded automated testing

---

Originally developed as the final project of the Java Fullstack Development Programme (Acertar o Rumo – University of Coimbra), in collaboration with an industry partner.

