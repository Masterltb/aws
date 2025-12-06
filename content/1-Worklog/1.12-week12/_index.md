---
title: "Worklog Week 12"
date: ""
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives

- **System-Wide Quality Assurance:** Conduct Unit & Integration Testing for both `Program Service` and `Chat Service`.
- **Performance Optimization:** Analyze and optimize PostgreSQL queries across both services.
- **Finalization & Handover:** Complete API documentation and prepare for system handover.

### Tasks for this week

| Day | Task                                                                                                                                                                                                 | Start Date | Completion Date | Reference                                                                                         |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------------------------------------- |
| 2   | - **Program Service:** Wrote Unit Tests for `StreakService` and `QuizService`. <br>- **Chat Service:** Wrote Unit Tests for `ChatService` to verify message retrieval logic.                           | 24/11/2025 | 24/11/2025      | <https://site.mockito.org/>                                                                       |
| 3   | - **Program Service:** Wrote Integration Tests for the "Smoke Event -> Recovery" flow. <br>- **Chat Service:** Wrote Integration Tests for the "Get Chat Rooms -> Get History" flow.                  | 25/11/2025 | 25/11/2025      | —                                                                                                 |
| 4   | - **Optimization:** Used `EXPLAIN ANALYZE` to analyze and add indexes to tables in both services, especially on foreign keys and columns used for sorting.                                            | 26/11/2025 | 26/11/2025      | <https://www.postgresql.org/docs/current/using-explain.html>                                      |
| 5   | - **Documentation:** Updated `api-docs.md` with complete and accurate details for all APIs of both services. <br>- **Reporting:** Finalized the internship report, describing the microservices architecture. | 27/11/2025 | 27/11/2025      | <https://swagger.io/>                                                                             |
| 6   | - **Review:** Final code cleanup, checked configurations and environment variables. <br>- **Presentation:** Prepared a demo and presentation of the overall architecture of both services for the mentor. | 28/11/2025 | 28/11/2025      | —                                                                                                 |

### Week 12 Outcomes

- **System Quality:** Both services have good test coverage, ensuring the stability and correctness of business flows.
- **Performance Optimized:** Query performance for both services has been improved, ready for production load.
- **Complete Documentation:** Delivered unified and clear API documentation for the entire system.
- **Completion:** Successfully built and delivered a complete microservices backend system.

**Overall Internship Reflection:**
Over the last 4 weeks, I have designed and implemented a microservices system from scratch, including a `Program Service` and a `Chat Service`. I have applied professional software development principles from design, implementation, testing, and optimization to documentation, and successfully translated complex business requirements into a functional software product.
