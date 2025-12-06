---
title: "Worklog Week 9"
date: ""
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives

- **Dual-Service Kick-off:** Scaffold both **Program Service** and **Chat Service** using Java 25 and Spring Boot.
- **DB Design:** Design and implement the database schemas for both services.
- **Initial Logic:** Build the Assessment & Recommendation flow for the Program Service and apply a shared security layer.

### Tasks for this week

| Day | Task                                                                                                                                                                                                 | Start Date | Completion Date | Reference                                                             |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------------------------------- |
| 2   | - **Program Service:** Initialized Spring Boot project and designed ERD for `Programs`, `Quizzes`. <br>- **Chat Service:** Designed ERD for `ChatRooms`, `Messages`.                                  | 03/11/2025 | 03/11/2025      | <https://start.spring.io/>                                            |
| 3   | - **Program Service:** Implemented `MeQuizController` to classify addiction levels. <br>- **Chat Service:** Initialized Spring Boot project and created Entity classes (`ChatRoom`, `Message`).       | 04/11/2025 | 04/11/2025      | —                                                                     |
| 4   | - **Program Service:** Seeded `ProgramTemplates` data and developed the Recommendation Engine. <br>- **Database:** Applied schemas for both services using Flyway.                                    | 05/11/2025 | 05/11/2025      | <https://flywaydb.org/>                                               |
| 5   | - **Program Service:** Built the User Enrollment API. <br>- **Shared Security:** Integrated a reusable JWT authentication filter for both services.                                                   | 06/11/2025 | 06/11/2025      | <https://spring.io/guides/gs/securing-web/>                           |
| 6   | - **Testing:** Used Postman to test the Assessment & Enrollment flow of the Program Service. <br>- **Review:** Code review of both project structures, ensuring consistency.                          | 07/11/2025 | 07/11/2025      | —                                                                     |

### Week 9 Outcomes

- **Successfully scaffolded both services:** `Program Service` and `Chat Service`.
- **Completed Database Schema implementation** for both services in PostgreSQL, managed by Flyway.
- **Program Service:** A functional Assessment & Recommendation system is operational, allowing user classification and program suggestions.
- **Security:** A JWT security layer has been integrated and is ready to protect future APIs.

**Key Learnings:**

- **Microservices Architecture:** Understood how to set up and manage multiple services within the same system.
- **DB Schema Management:** Using Flyway makes managing and deploying database changes safe and automated.
- **Reusability:** Designing shared components (like the security layer) that can be applied across multiple services to avoid code duplication.
