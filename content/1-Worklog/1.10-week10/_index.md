---
title: "Worklog Week 10"
date: ""
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives

- **Program Service:** Implement core logic (Daily Routine, Streak Tracking, Smoke Events).
- **Chat Service:** Prepare the Data Access Layer.

### Tasks for this week

| Day | Task                                                                                                                                                                                                 | Start Date | Completion Date | Reference                                                                                         |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ------------------------------------------------------------------------------------------------- |
| 2   | - **Program Service:** Implemented logic to generate 4 daily steps for users. <br>- **Chat Service:** Created `ChatRoomRepository` and `MessageRepository` interfaces.                                 | 10/11/2025 | 10/11/2025      | —                                                                                                 |
| 3   | - **Program Service:** Built APIs for step completion and implemented the `StreakService`. <br>- **Chat Service:** Wrote custom JPQL queries to find messages by chat room with pagination.            | 11/11/2025 | 11/11/2025      | —                                                                                                 |
| 4   | - **Program Service:** Developed the "Smoke Event" trigger and "Soft Reset" logic (Status: PENDING_RECOVERY).                                                                                          | 12/11/2025 | 12/11/2025      | —                                                                                                 |
| 5   | - **Program Service:** Implemented the recovery logic: assign a "Recovery Quiz" and handle the outcome (max 3 attempts).                                                                               | 13/11/2025 | 13/11/2025      | —                                                                                                 |
| 6   | - **Program Service:** Wrote Unit Tests for `StreakService` and performed integration testing for the entire flow.                                                                                     | 14/11/2025 | 14/11/2025      | <https://junit.org/junit5/>                                                                       |

### Week 10 Outcomes

- **Program Service:**
  - The **Daily Routine** engine and **Streak System** are fully functional.
  - The **Recovery Mechanism** successfully handles "Smoke Events" in a humane way.
- **Chat Service:**
  - The **Data Access Layer (Repository)** has been defined and is ready for implementation in the next week.

**Key Learnings:**

- **Complex State Management:** Handling user states (Active, Pending Recovery) requires a robust state machine logic.
- **Focusing on One Service:** Dedicating the majority of time to a complex service ensures quality and progress, while still allowing for preparatory work on other services.
- **JPQL for Custom Queries:** Using JPQL is a powerful way to write complex queries that are not automatically supported by Spring Data JPA.
