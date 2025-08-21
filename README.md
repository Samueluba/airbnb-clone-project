# airbnb-clone-project
This is my First Project
This is my first Alx project on GitHub 
This project is tailored to enhance my expertise in modern software development practices. By completing these tasks, I will:

Master collaborative team workflows using GitHub.
Deepen my understanding of backend architecture and database design principles.
Implement advanced security measures for API development.
Gain proficiency in designing and managing CI/CD pipelines for efficient deployment.
Strengthen their ability to document and plan complex software projects effectively Develop an understanding of integrating technologies like Django, MySQL, and GraphQL in a unified ecosystem.

 Table of Contents
1. [Project Description](#project-description)
2. [Team Roles](#team-roles)
3. Technology stack
4. [License](#license)

5. Team Roles :
 Business analyst (BA): Understands customer’s business processes, Translates customer business needs into requirements
Product owner (PO): Makes sure the final product meets customer requirement
Project manager (PM): Manages and motivates the software development team
UI/UX designer: Creates user journeys for the best user experience and highest conversion rates
Software architect: Selects appropriate tools and platforms to implement the product vision
Software developer: solves any technical problems emerging during the development lifecycle
Quality assurance (QA) engineer: Spots functional and non-functional defects
Test automation engineer:Writes and maintains test scripts for automated testing
DevOps engineer: Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery

## Technology Stack

This project utilizes the following technologies:

- **Django**: A high-level Python web framework used for building the RESTful API.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **PostgreSQL**: A powerful relational database used for data storage.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Celery**: For handling asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

- Certainly! Here's the full **entities and relationships** description formatted in **Markdown**:

```markdown
## Entities and Relationships

### 1. User
**Important Fields:**
- `id`: Unique identifier for the user  
- `name`: Full name of the user  
- `email`: Used for login and communication  
- `password_hash`: Securely stored password  
- `role`: E.g., guest, host, admin  

**Relationships:**
- A **user** can create **multiple properties** (if host).
- A **user** can make **multiple bookings**.
- A **user** can leave **multiple reviews**.

---

### 2. Property
**Important Fields:**
- `id`: Unique property ID  
- `user_id`: References the host (user)  
- `title`: Name of the property  
- `location`: Address or coordinates  
- `price_per_night`: Cost to book per night  

**Relationships:**
- A **property** belongs to one **user** (host).
- A **property** can have multiple **bookings**.
- A **property** can have multiple **reviews**.

---

### 3. Booking
**Important Fields:**
- `id`: Unique booking ID  
- `user_id`: The guest who made the booking  
- `property_id`: The property being booked  
- `start_date`: Booking start  
- `end_date`: Booking end  
- `status`: E.g., pending, confirmed, cancelled  

**Relationships:**
- A **booking** belongs to one **user** (guest).
- A **booking** belongs to one **property**.
- A **booking** may have one or more **payments**.

---

### 4. Payment
**Important Fields:**
- `id`: Unique payment ID  
- `booking_id`: Associated booking  
- `amount`: Total amount paid  
- `payment_method`: E.g., credit card, PayPal  
- `status`: Paid, failed, refunded  

**Relationships:**
- A **payment** is linked to one **booking**.
- A **booking** can have **one or more payments**.

---

### 5. Review
**Important Fields:**
- `id`: Unique review ID  
- `user_id`: Reviewer (guest)  
- `property_id`: Property being reviewed  
- `rating`: Numeric rating (e.g., 1–5)  
- `comment`: Text feedback  

**Relationships:**
- A **review** belongs to one **user**.
- A **review** belongs to one **property**.
- A **property** can have **multiple reviews**.

---

## Entity Relationship Summary

- A **User** can:
  - List **multiple properties**
  - Make **multiple bookings**
  - Leave **multiple reviews**

- A **Property**:
  - Belongs to one **user** (host)
  - Has many **bookings**
  - Has many **reviews**

- A **Booking**:
  - Is made by one **user**
  - Is for one **property**
  - Has one or more **payments**

- A **Payment**:
  - Belongs to one **booking**

- A **Review**:
  - Is written by one **user**
  - Is for one **property*


