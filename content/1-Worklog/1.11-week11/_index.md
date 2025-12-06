---
title: "Worklog Week 11"
date: ""
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives

- **Chat Service:** Implement core APIs (get chat rooms, message history).
- **Program Service:** Refine business logic (Slip/Relapse) and add administrative features.

### Tasks for this week

| Day | Task                                                                                                                                                                                                 | Start Date | Completion Date | Reference                                                                                         |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------------------------------------- |
| 2   | - **Chat Service:** Implemented `ChatController` and the `GET /api/v1/chat-rooms/me` API to get a user's chat rooms.                                                                                   | 17/11/2025 | 17/11/2025      | —                                                                                                 |
| 3   | - **Chat Service:** Implemented the `GET /api/v1/chat-rooms/{roomId}/messages` API with pagination and sorting. <br>- **Chat Service:** Implemented the internal `POST /internal/api/v1/chat-rooms` API. | 18/11/2025 | 18/11/2025      | —                                                                                                 |
| 4   | - **Program Service:** Implemented the logic to differentiate between **Slip** (immediate recovery) and **Relapse** (hard reset). <br>- **Program Service:** Added Flyway to manage schema changes.     | 19/11/2025 | 19/11/2025      | <https://flywaydb.org/>                                                                           |
| 5   | - **Program Service:** Built Admin APIs (CRUD) for `Quiz Templates`. <br>- **Program Service:** Optimized the reset counter logic (max 3 recoveries).                                                  | 20/11/2025 | 20/11/2025      | —                                                                                                 |
| 6   | - **Program Service:** Developed the `@Scheduled` job for Weekly Assessments. <br>- **Testing:** Used Postman to test the new Chat Service APIs.                                                       | 21/11/2025 | 21/11/2025      | <https://spring.io/guides/gs/scheduling-tasks/>                                                   |

### Week 11 Outcomes

- **Chat Service:**
  - Core APIs for retrieving chat rooms and message history are functional.
  - The internal API for creating chat rooms is ready for other services to call.
- **Program Service:**
  - The **Slip vs Relapse** logic is complete, allowing the system to handle failure scenarios flexibly.
  - The **Admin Module** allows for independent management of Quiz content.
  - The **Weekly Assessment** system is automated.

**Key Learnings:**

- **API Pagination Design:** The importance of implementing effective pagination for APIs that return large lists (message history).
- **Scheduling:** Using Spring Scheduler is an efficient way to run periodic jobs without complex configurations.
- **Task Switching:** Shifting focus between services within a sprint/week helps maintain balanced progress for the entire system.
